# Creating a Normalized Difference Vegetation Index Using R
### Winter 2024 : Niamh Houston


Normalized Difference Vegetation Index (NDVI) is a remote sensing technique that quanifies and visualizes vegetation health. It works by measuring the difference between the reflectance of near-infrared (NIR) and visible red light. Healthy vegetation typically absorbes more visible light and reflects more NIR light, resulting in higher NDVI values. NDVIs can be particularly helpful for crop momotiring and management, identifying drought, land cover classification, ecosystem monitoring and climate change studies. An NDVI can be preformed using Rscript relatively simply using sattelite imagery. 

![000010](https://github.com/niamhhouston/GEOG490/assets/162380093/eede7c88-c9bd-42a8-b5ad-b9a9ca093eda)

K-Means classification is an unsupervised classification method that operates by dividing data into clusters based on similarity and proximity to calculated centroids. This classification method can be useful to classify land cover and preform change detrections. In the context of this analysis however, the K-menas plot aids in data comprehension. 

<img width="895" alt="Screenshot 2024-03-13 at 9 39 28 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/c276fe9b-3b97-4a3c-a96d-fabbbf4fb307">



## Code
The workflow, as follows, uses a geoTIF data file of Sentinel 2 imagery from the Loch Tay area of Scotland. The file used has been cropped and undergone an atmospheric correction to make it easier to import. 

### Loading Packages and Data 

# Set the working directory (replace with your own file path)
setwd("R:/GEOG493_593_25793_Winter2024/Student_Data/niamhh/R/FCC/CC-spatial-master")

# Load packages
# Install packages if needed
# Example:install.packages("sp")

install.packages("sp")
install.packages("raster")
install.packages("ggplot2")
install.packages("viridis")
install.packages("rasterVis")

library(sp)
library(raster)
library(ggplot2)
library(viridis)
library(rasterVis)

# Set the working directory (replace with your own file path) setwd("R:/GEOG493_593_25793_Winter2024/Student_Data/niamhh/R/FCC/CC-spatial-master") # Load packages # Install packages if needed # Example:install.packages("sp") install.packages("sp") install.packages("raster") install.packages("ggplot2") install.packages("viridis") install.packages("rasterVis") library(sp) library(raster) library(ggplot2) library(viridis) library(rasterVis)

### Creating Individual Rasters for Each Band

### Visualizing Spectral Bands 

### Visualizing Raster Plots 

#### Each raster layer from this output represent how much solar radiation is reflected at a particular wavelength bandwidth. 

### NDVI and K-Means Classification 
