# Creating a Normalized Difference Vegetation Index Using R
### Winter 2024 : Niamh Houston

<img width="895" alt="Screenshot 2024-03-13 at 9 39 28 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/96c68471-70bc-4dd5-9906-a0e9ba6606a3">


Normalized Difference Vegetation Index (NDVI) is a remote sensing technique that quanifies and visualizes vegetation health. It works by measuring the difference between the reflectance of near-infrared (NIR) and visible red light. Healthy vegetation typically absorbes more visible light and reflects more NIR light, resulting in higher NDVI values. NDVIs can be particularly helpful for crop momotiring and management, identifying drought, land cover classification, ecosystem monitoring and climate change studies. An NDVI can be preformed using Rscript relatively simply using sattelite imagery. 

K-Means classification is an unsupervised classification method that operates by dividing data into clusters based on similarity and proximity to calculated centroids. This classification method can be useful to classify land cover and preform change detrections. In the context of this analysis however, the K-menas plot aids in data comprehension. 

The workflow, in RStudio, uses a geoTIF data file of Sentinel 2 imagery from the Loch Tay area of Scotland (taycrop.tif). The file used has been cropped and undergone an atmospheric correction to make it easier to import. To replicate this analysis, download Houston_Data.zip from the repository, note thee file path you download it to and follow the code workflow from NDVI.HTML, NDVI3.Rmd (both are linked in the repository) or from 
[NDVI3.pdf](https://github.com/niamhhouston/GEOG490/files/14609665/NDVI3.pdf). 

### Code 
<img width="617" alt="Screenshot 2024-03-21 at 6 00 03 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/941df561-a72f-4268-bffd-9c5c867d3349">
<img width="620" alt="Screenshot 2024-03-21 at 6 00 31 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/e2a2f34f-7854-4f36-ba78-0be2802214aa">
<img width="617" alt="Screenshot 2024-03-21 at 6 04 22 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/3c7f9973-2a1d-415e-baf4-5f87a3a52f2d">
<img width="622" alt="Screenshot 2024-03-21 at 6 05 00 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/2e5cb4f7-34d8-4f6c-bf48-776d675b0ab2">
<img width="620" alt="Screenshot 2024-03-21 at 6 05 16 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/d44fc041-f660-43a5-bd5a-0f021a29f875">
<img width="617" alt="Screenshot 2024-03-21 at 6 05 51 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/1f01b485-da83-4860-97ff-9fb2a93b6457">
<img width="616" alt="Screenshot 2024-03-21 at 6 06 14 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/ac920b53-634e-410a-bdfd-17998da0afd0">
<img width="618" alt="Screenshot 2024-03-21 at 6 06 41 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/19cff623-d9b1-4763-ada1-707b3eec9bf4">
<img width="616" alt="Screenshot 2024-03-21 at 6 07 36 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/090eddb6-624e-4866-ac17-bf1df0b87412">
<img width="616" alt="Screenshot 2024-03-21 at 6 07 50 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/a0a865b5-2a1c-45b6-a68d-705d6b13b2b9">
