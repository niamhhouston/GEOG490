# Creating a Normalized Difference Vegetation Index Using R
### Winter 2024 : Niamh Houston


Normalized Difference Vegetation Index (NDVI) is a remote sensing technique that quanifies and visualizes vegetation health. It works by measuring the difference between the reflectance of near-infrared (NIR) and visible red light. Healthy vegetation typically absorbes more visible light and reflects more NIR light, resulting in higher NDVI values. NDVIs can be particularly helpful for crop momotiring and management, identifying drought, land cover classification, ecosystem monitoring and climate change studies. An NDVI can be preformed using Rscript relatively simply using sattelite imagery. 

![000010](https://github.com/niamhhouston/GEOG490/assets/162380093/eede7c88-c9bd-42a8-b5ad-b9a9ca093eda)

K-Means classification is an unsupervised classification method that operates by dividing data into clusters based on similarity and proximity to calculated centroids. This classification method can be useful to classify land cover and preform change detrections. In the context of this analysis however, the K-menas plot aids in data comprehension. 

<img width="895" alt="Screenshot 2024-03-13 at 9 39 28 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/c276fe9b-3b97-4a3c-a96d-fabbbf4fb307">



## Code
The workflow, as follows, uses a geoTIF data file of Sentinel 2 imagery from the Loch Tay area of Scotland. The file used has been cropped and undergone an atmospheric correction to make it easier to import. 

### Loading Packages 
<img width="623" alt="Screenshot 2024-03-13 at 11 11 44 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/11edb3f7-cb43-45d3-9a26-d96bd92012e3">

### Loading Data 
<img width="271" alt="Screenshot 2024-03-13 at 11 14 20 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/587462ed-5f40-4c2e-8036-f9b4043ec789">

### Creating Individual Rasters for Each Band
<img width="286" alt="Screenshot 2024-03-13 at 11 15 02 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/e37e14f0-e140-43a6-bf36-d887ead76df0">

### Visualizing Spectral Bands
<img width="602" alt="Screenshot 2024-03-13 at 11 16 01 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/26a8b360-0320-4092-94cd-09cce298903d">

### Raster Plots 
<img width="229" alt="Screenshot 2024-03-13 at 11 19 27 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/7e8d43f0-8f88-470a-b5d8-f9fe042a422d">





#### Each raster layer from this output represent how much solar radiation is reflected at a particular wavelength bandwidth. 

### NDVI and K-Means Classification 
