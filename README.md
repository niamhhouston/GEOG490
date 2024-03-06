# Top R Earth System Science  
## Visualizing Global Urban Light Pollution Using R
###### Winter 2024 : Niamh Houston

## Images

![Minion](https://octodex.github.com/images/minion.png

#### Light pollution can be understood as the excessive use of outdoor artificial light. It is an unfortunate attribute of urbanized living [4]. In addition to observed obstruction to stars and other celestial objects, light pollution has been known to affect human health, plant signaling and wildlife behavior [1,2,3]. Plants growing near artificial light sources are signaled to break buds and flower earlier in the Spring, risking the loss of their reproductive effort from late frost events [2]. For humans, light pollution can disrupt daily circadian rhythms or sleep-wake cycles which has been liked to increased health complications. [1]. Other wildlife may experience delayed signals to hibernate or migrate due to the presence from artificial light [3]. The combined aesthetic and ecological effects of light pollution provide a viable call for mitigation. 

## Code

inline 'code'

### Importing Libraries 

# libraries we need
libs <- c(
  "tidyverse", "sf", "giscoR",
  "mapview", "terra", "terrainr",
  "magick"
)

# install missing libraries
installed_libs <- libs %in% rownames(installed.packages())
if (any(installed_libs == F)) {
  install.packages(libs[!installed_libs])
}

# load libraries
invisible(lapply(libs, library, character.only = T))

### Global Extent Polygon 

# define projections
longlat_crs <- "+proj=longlat +datum=WGS84 +no_defs"
ortho_crs <-'+proj=ortho +lat_0=32.4279 +lon_0=53.688 +x_0=0 +y_0=0 +R=6371000 +units=m +no_defs +type=crs'

### Cropping Extent Polygon 

get_flat_world_sf <- function() {
  world <- giscoR::gisco_get_countries(
    year = "2016",
    epsg = "4326",
    resolution = "10"
  ) %>%
    sf::st_transform(longlat_crs)
  
  world_vect <- terra::vect(world)
  
  return(world_vect)
}

world_vect <- get_flat_world_sf()

### NASA's Nightlight Data 

# 2. NASA DATA
#-------------
get_nasa_data <- function() {
  ras <- terra::rast("/vsicurl/https://eoimages.gsfc.nasa.gov/images/imagerecords/144000/144898/BlackMarble_2016_01deg_geo.tif")
  rascrop <- terra::crop(x = ras, y = world_vect, snap = "in")
  ras_latlong <- terra::project(rascrop, longlat_crs)
  ras_ortho <- terra::project(ras_latlong, ortho_crs)
  return(ras_ortho)
}

ras_ortho <- get_nasa_data()

### Reprojecting on Globe 

r <- ifel(is.na(ras_ortho), 0, ras_ortho)
plot(r)

### Mapping the Data 
# 3. MAP NIGHTLIGHTS
#-------------------
make_nighlights_globe <- function() {
  globe <- ggplot() +
    terrainr::geom_spatial_rgb(
      data = r,
      mapping = aes(
        x = x,
        y = y,
        r = red,
        g = green,
        b = blue
        
      )
    ) +
    theme_minimal() +
    theme(
      plot.margin = unit(
        c(t = -1, r = -1, b = -1, l = -1), "lines"
      ),
      panel.grid.major = element_blank(),
      panel.grid.minor = element_blank(),
      plot.background = element_rect(fill = "black", color = NA),
      panel.background = element_rect(fill = "black", color = NA),
      legend.background = element_rect(fill = "black", color = NA),
      panel.border = element_rect(fill = NA, color = "black"),
    ) +
    labs(
      x = "",
      y = "",
      title = "EARTH AT NIGHT",
      subtitle = "Urban Light Pollution on a Global Distribution",
      caption = "Niamh Houston, 2024 Data: NASA Earth Observatory"
    )
}

globe <- make_nighlights_globe()

ggsave(
  filename = "nightlight_globe.png",
  width = 7, height = 7.5, dpi = 600, device = "png", globe
)

### Annotations 

# 4. ANNOTATE MAP
#----------------
# read image
map <- magick::image_read("nightlight_globe.png")

# set font color
clr <- "#FFFFBC"

# Title
map_title <- magick::image_annotate(map, "Earth at night",
                                    font = "Georgia",
                                    color = alpha(clr, .65), size = 200, gravity = "north",
                                    location = "+0+80"
)
# Caption
map_final <- magick::image_annotate(map_title, glue::glue(
  "©2024 Niamh Houston | ",
  "Data: NASA Earth Observatory"
),
font = "Georgia", location = "+0+50",
color = alpha(clr, .45), size = 50, gravity = "south"
)

magick::image_write(map_final, glue::glue("nightlight_globe_annotated.png"))

Block code "fences"

...
Sample text here...
...

Syntax highlighting

...js
var foo = function (bar) (
  return bar++;
];
console.log(foo(5));
...

## References 
[1] https://www.southamptontownny.gov/DocumentCenter/View/28311/Light-Pollution-Can-Put-Your-Health-at-Risk#:~:text=Circadian%20disruption%20may%20increase%20our,cancers%20and%20other%20health%20problems.

[2]https://www.indefenseofplants.com/blog/2018/8/6/light-pollution-and-plants#:~:text=The%20effects%20of%20artificial%20lighting,threat%20of%20frost%20is%20gone.

[3]https://www.sciencedirect.com/science/article/abs/pii/S0169534722003329#:~:text=Light%20pollution%20can%20affect%20nocturnal,exposure%20to%20sky%20glow%20and

[4] https://darksky.org/resources/what-is-light-pollution/light-pollution-solutions/

##The End!
