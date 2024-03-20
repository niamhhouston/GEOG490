# Creating a Normalized Difference Vegetation Index Using R
### Winter 2024 : Niamh Houston

<img width="895" alt="Screenshot 2024-03-13 at 9 39 28 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/96c68471-70bc-4dd5-9906-a0e9ba6606a3">


Normalized Difference Vegetation Index (NDVI) is a remote sensing technique that quanifies and visualizes vegetation health. It works by measuring the difference between the reflectance of near-infrared (NIR) and visible red light. Healthy vegetation typically absorbes more visible light and reflects more NIR light, resulting in higher NDVI values. NDVIs can be particularly helpful for crop momotiring and management, identifying drought, land cover classification, ecosystem monitoring and climate change studies. An NDVI can be preformed using Rscript relatively simply using sattelite imagery. 

K-Means classification is an unsupervised classification method that operates by dividing data into clusters based on similarity and proximity to calculated centroids. This classification method can be useful to classify land cover and preform change detrections. In the context of this analysis however, the K-menas plot aids in data comprehension. 

The workflow, as follows, uses a geoTIF data file of Sentinel 2 imagery from the Loch Tay area of Scotland (taycrop.tif). The file used has been cropped and undergone an atmospheric correction to make it easier to import. To replicate this analysis, download taycrop.pdf from the repository, note thee file path you download it to and follow the code workflow from NDVI.HTML linked in the repository or from 
[NDVI3.pdf](https://github.com/niamhhouston/GEOG490/files/14609665/NDVI3.pdf)
