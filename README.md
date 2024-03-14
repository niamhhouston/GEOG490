# Creating a Normalized Difference Vegetation Index Using R
### Winter 2024 : Niamh Houston


Normalized Difference Vegetation Index (NDVI) is a remote sensing technique that quanifies and visualizes vegetation health. It works by measuring the difference between the reflectance of near-infrared (NIR) and visible red light. Healthy vegetation typically absorbes more visible light and reflects more NIR light, resulting in higher NDVI values. NDVIs can be particularly helpful for crop momotiring and management, identifying drought, land cover classification, ecosystem monitoring and climate change studies. An NDVI can be preformed using Rscript relatively simply using sattelite imagery. 

K-Means classification is an unsupervised classification method that operates by dividing data into clusters based on similarity and proximity to calculated centroids. This classification method can be useful to classify land cover and preform change detrections. In the context of this analysis however, the K-menas plot aids in data comprehension. 

# Code
The workflow, as follows, uses a geoTIF data file of Sentinel 2 imagery from the Loch Tay area of Scotland. The file used has been cropped and undergone an atmospheric correction to make it easier to import. 

## Loading Packages 
<img width="623" alt="Screenshot 2024-03-13 at 11 11 44 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/11edb3f7-cb43-45d3-9a26-d96bd92012e3">

## Loading Data 
<img width="271" alt="Screenshot 2024-03-13 at 11 14 20 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/587462ed-5f40-4c2e-8036-f9b4043ec789">

## Creating Individual Rasters for Each Band
<img width="286" alt="Screenshot 2024-03-13 at 11 15 02 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/e37e14f0-e140-43a6-bf36-d887ead76df0">

## Visualizing Spectral Bands
<img width="602" alt="Screenshot 2024-03-13 at 11 16 01 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/26a8b360-0320-4092-94cd-09cce298903d">

## Raster Plots 
<img width="229" alt="Screenshot 2024-03-13 at 11 19 27 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/7e8d43f0-8f88-470a-b5d8-f9fe042a422d">

<img width="1141" alt="Screenshot 2024-03-13 at 11 34 18 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/89488ce3-6bf3-4cbe-96aa-b89ae17f3bfb">

Each raster layer from this output represent how much solar radiation is reflected at a particular wavelength bandwidth. 

## NDVI and K-Means Classification 
<img width="371" alt="Screenshot 2024-03-13 at 11 21 36 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/4c30a5be-94d9-4549-b79e-7f99ce282832">
<img width="587" alt="Screenshot 2024-03-13 at 11 22 34 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/f3c2c139-b166-4c29-86b3-9b2683b98511">
<img width="578" alt="Screenshot 2024-03-13 at 8 50 22 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/5dffcefd-0224-438f-a66c-3aa7449f8d4a">

## Plotting a histogram 
<img width="515" alt="Screenshot 2024-03-13 at 11 24 10 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/005e7872-8afb-4c9b-9968-ce40523e1d46">
<img width="660" alt="Screenshot 2024-03-13 at 11 24 37 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/66cd5078-2f95-4609-89df-5f9f14769238">

The histogram is strongly skewed twoards the high NDVI values which indicates a highly vegetated area. We can now mask any pixels less than 0.4 because they are less likely to be vegetated. 

## Masking Cells 
<img width="738" alt="Screenshot 2024-03-13 at 11 27 16 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/383ff543-3fcd-4f6e-9f5e-ef974c0899b1">
<img width="663" alt="Screenshot 2024-03-13 at 11 27 40 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/0f441a79-f3d6-4260-89d7-9622b8f015a5">

## K-Means Classification 
<img width="719" alt="Screenshot 2024-03-13 at 11 29 52 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/83d6cc61-c445-40fd-9c6c-3d1342fddb9f">

## Make dimensions same as NDVI
<img width="403" alt="Screenshot 2024-03-13 at 11 31 25 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/f8226b36-38c9-4675-917a-16cd58424af0">

## Final Plot of NDVI and K-means 
<img width="470" alt="Screenshot 2024-03-13 at 11 32 20 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/514ddc5a-319f-4f22-9053-e05bc994cc42">
<img width="895" alt="Screenshot 2024-03-13 at 9 39 28 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/96c68471-70bc-4dd5-9906-a0e9ba6606a3">
