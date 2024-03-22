# Creating a Normalized Difference Vegetation Index Using R
### Winter 2024 : Niamh Houston

<img width="895" alt="Screenshot 2024-03-13 at 9 39 28 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/96c68471-70bc-4dd5-9906-a0e9ba6606a3">


Normalized Difference Vegetation Index (NDVI) is a remote sensing technique that quanifies and visualizes vegetation health. It works by measuring the difference between the reflectance of near-infrared (NIR) and visible red light. Healthy vegetation typically absorbes more visible light and reflects more NIR light, resulting in higher NDVI values. NDVIs can be particularly helpful for crop momotiring and management, identifying drought, land cover classification, ecosystem monitoring and climate change studies. An NDVI can be preformed using Rscript relatively simply using sattelite imagery. 

K-Means classification is an unsupervised classification method that operates by dividing data into clusters based on similarity and proximity to calculated centroids. This classification method can be useful to classify land cover and preform change detrections. In the context of this analysis however, the K-menas plot aids in data comprehension. 

The workflow, in RStudio, uses a geoTIF data file of Sentinel 2 imagery from the Loch Tay area of Scotland (taycrop.tif). The file used has been cropped and undergone an atmospheric correction to make it easier to import. To replicate this analysis, download Houston_Data.zip from the repository, note thee file path you download it to and follow the code workflow from NDVI.HTML, NDVI3.Rmd (both are linked in the repository) or from 
[NDVI3.pdf](https://github.com/niamhhouston/GEOG490/files/14609665/NDVI3.pdf). 

###Code:
<img width="1222" alt="Screenshot 2024-03-21 at 5 46 00 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/bdfa1beb-4e80-4566-833e-7ab393e8b73a">
<img width="1222" alt="Screenshot 2024-03-21 at 5 46 23 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/9d2ee2ac-21ea-46b1-93a6-0a136aaad7b1">
<img width="1226" alt="Screenshot 2024-03-21 at 5 47 00 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/e048952d-e31d-49e5-9f6a-229634556935">
<img width="1222" alt="Screenshot 2024-03-21 at 5 47 20 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/c667716d-5497-45e2-b2da-b3e402b06d0b">
<img width="1224" alt="Screenshot 2024-03-21 at 5 47 39 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/df0a76bc-429a-4c43-a34f-707fe4d1bb2e">
<img width="1064" alt="Screenshot 2024-03-21 at 5 49 55 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/7c85c9f9-b098-46be-98de-fa63a498ba3e">

<img width="1060" alt="Screenshot 2024-03-21 at 5 50 53 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/88e3ca91-36ea-4384-aecd-0bbc4ceecf5a">
<img width="785" alt="Screenshot 2024-03-21 at 5 51 05 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/0b994779-9ae7-4bbb-8dc1-7f3e8678f328"<img width="927" alt="Screenshot 2024-03-21 at 5 51 29 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/cb9241b9-907b-4c1b-9714-520f16c8ed22"><img width="927" alt="Screenshot 2024-03-21 at 5 51 43 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/85414b16-79bf-4a43-8296-d9d4552ad121">

>


<img width="921" alt="Screenshot 2024-03-21 at 5 51 56 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/37879be3-fad6-4ab5-b513-829c0e8cb1cb">
<img width="922" alt="Screenshot 2024-03-21 at 5 52 10 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/9ffcce7c-9a68-4303-a87f-9fad0139d3b8">
<img width="908" alt="Screenshot 2024-03-21 at 5 52 32 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/bb5224ea-7af8-49cc-98ce-04d31097ef61">

<img width="922" alt="Screenshot 2024-03-21 at 5 52 47 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/b9918893-85a5-47bb-8858-aeb911ec22ca">
<img width="922" alt="Screenshot 2024-03-21 at 5 53 01 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/325d8599-dabb-44c1<img width="920" 
alt="Screenshot 2024-03-21 at 5 53 34 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/7ce266b6-fbe9-4db0-ab65-36c772d71486">
-b83b-45849f10f17d">

<img width="916" alt="Screenshot 2024-03-21 at 5 53 17 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/334062ce-c887-4f96-8301-138c1fe30c42">
<img width="922" alt="Screenshot 2024-03-21 at 5 54 02 PM" src="https://github.com/niamhhouston/GEOG490/assets/162380093/29733c11-48e9-457a-8444-feb384143e4b">
