[Previous](climate.md) | [Table of contents](/README.md) | [Next](infrastructure-monitoring.md)

***

## 5.2. Disaster

### 5.2.1. SAR Flood Mapping

**GOAL:**
Generative AI shows promising capability in reconstructing flood disaster, as shown by Lowe et al. (2021). Without domain and weather diversified ground truth, Lazin et al. (2024) concluded that no generative model currently shows generalizability, transferability, or explainability. Shen et al. (2019, 2021, 2024\) demonstrate that the high resolution FIMs over vast spatiotemporal domains from SAR satellites, including Sentinel-1, RadarSat, ALOS-1, and RCM can fill this gap.  
   
**AI4EO example:**
The researchers created a 1-dimensional (1D) statistic signature (PDF similarity), to delineate water areas.  By intercomparison with operational 0D method in the Figure below, The 1-D method performs consistently outperforms the 0D method over most types of land cover, and commits significantly lower error  in discerning real water and water-alike areas on radar images.

![SAR Flood Mapping](/figures/Figure5.2.1-1.png)  
Figure.5.2.1-1 Intercomparison of RAPID v2.0 (1D method in dark blue) with GFM (0D method in red) and OPERA (0 D method in light blue). Row 1 shows  RAPID v2.0 against GFM). Row 2 shows RAPID v2.0 against OPERA. And row 3 shows RAPID v2.0 against OPERA and GFM. The last column is the SAR image at VV polarization.

### 5.2.2. Flood Mapping with Optical Satellite Sensors[^1]

#### 5.2.2.1. Machine Learning in Optical Flood Mapping

Floods are among the most devastating natural disasters, yet traditional methods for mapping them often fall short. Machine learning (ML) has introduced a transformative approach, moving beyond manual analysis and simple algorithmic methods to a more dynamic and intelligent system for flood detection and mapping. This is particularly valuable for disaster resilience, as it allows for rapid and automated processing of vast amounts of Earth Observation (EO) data from satellites.

The core innovation lies in the ability of ML models, especially deep learning networks, to "learn" from historical data. By analyzing past flood events and their corresponding satellite imagery, these models can identify subtle patterns and relationships that are difficult for humans or simpler algorithms to detect. This leads to high-accuracy flood detection that is more adaptable to diverse environments and challenging conditions. Instead of relying on a single data type, ML models can fuse information from multiple sources—such as optical images, digital elevation models, and water flow grids—to create a more comprehensive and robust flood map. This fusion of data allows for a more complete picture of a flood's extent, including areas that might be obscured from direct view.

#### 5.2.2.2. The FloodSENS Method: One Possible Method Among Many

FloodSENS, a project developed by RSS-Hydro ([Gaffinet et al., 2023](http://doi.org/10.1109/IGARSS52108.2023.10282274)), exemplifies the power of this ML-driven innovation. It is a machine-learning-powered flood mapping tool that uses a U-Net model, a type of convolutional neural network well-suited for image segmentation tasks. The method's primary focus is on optical satellite imagery, specifically from the Sentinel-2 (S-2) mission.

The central challenge with using optical images for flood mapping is that they are rendered useless by cloud cover, which often accompanies major weather events and floods. The groundbreaking aspect of FloodSENS is its ability to overcome this limitation. The U-Net model is trained on expertly labeled flood images and, crucially, integrates auxiliary datasets. By incorporating digital elevation models (DEMs), which describe the terrain's height and slope, the algorithm learns the correlation between water bodies and low-lying areas. This allows FloodSENS to effectively reconstruct the flood extent beneath cloud cover. The model can identify visible flooded areas in cloud-free parts of an image and, using the topographical data, extrapolate the likely flood extent into the cloud-obscured regions (see abstract representation in Figure 5.2.2.2-1 below).

 ![Machine Learning in Optical Flood Mapping](/figures/Figure5.2.2.2-1.png)

*Figure 5.2.2.2-1: In essence, the machine learning algorithm learns to recognise visible floods and extrapolates their extent below clouds based on terrain features such as slope and land use.*

#### 5.2.2.3. Benefits of Using ML for Flood Mapping on Optical Images

The application of ML to optical imagery for flood mapping provides significant benefits for various stakeholders, from humanitarian agencies to insurance companies.

* Improved Accuracy and Global Transferability: By training the model on a large number of diverse flood events across different biomes, FloodSENS achieves a high degree of accuracy and global transferability (Figure 5.2.2.3-1 below). It can outperform traditional methods and correctly identify complex flood boundaries, such as those defined by debris lines. This ensures consistent and reliable mapping across different geographical locations without needing extensive manual calibration for each new site. When testing locally-trained versus globally transferable models on several individual events against standard index-based mapping approaches, such as the NDWI, a locally trained model achieves excellent performance of an IoU over 90% (Intersection over Union) while the best transferable model achieves an IoU of 80% (Gaffinet et al., 2023).  
  ![Benefits of Using ML for Flood Mapping on Optical Images](/figures/Figure5.2.2.3-1.png)  
  *Figure 5.2.2.3-1: FloodSENS is a living ML-based algorithm that generates accurate flood maps from optical imagery consistently across diverse biomes, providing invaluable up-to-date information at regional, national, and global scales.*  
* Timely and Actionable Information: ML-based models can process satellite data much faster than manual methods, providing timely information crucial for emergency response. The outputs of FloodSENS are not just static maps but are designed to provide actionable intelligence. This includes feeding into 3D visualizations created with free tools like [Blender](https://www.blender.org/features/) or [NVIDIA Omniverse](https://www.nvidia.com/en-us/omniverse/), which allow decision-makers to immerse themselves in a simulated flood scenario. This provides a deeper understanding of flood patterns and potential impacts (illustrated in Figure 5.2.2.3-2 below), supporting better preparedness and resource allocation.  
  ![Benefits of Using ML for Flood Mapping on Optical Images](/figures/Figure5.2.2.3-2.png)  
  *Figure 5.2.2.3-2: A sample 3D scene generation of a FloodSENS S-2 map simulation within NVIDIA’s Omniverse platform. Significant flooding in the urban areas of Brisbane is shown for the 2022 event, with flooded above-ground electricity lines, depicted in the lower right area of the scene.*  
* Enhanced Data Utility: The ability to generate flood maps from cloud-covered optical images significantly increases the amount of usable data. Previously, many valuable images from major flood events were discarded due to cloud obscuration. FloodSENS renders these images usable, building a more accurate and reliable historical record of floods. This long-term data collection is vital for climate change analysis, risk assessment, and urban planning.

### 5.2.3.  FloodML : Flood Extent rapid mapping from EO satellite data[^2]

Written by Raquel Rodríguez Suquet \- CNES, provided to WGDisaster Flood pilot for inclusion.

The [SCO FloodDAM Digital Twin project](https://www.spaceclimateobservatory.org/flooddam-dt) is a demonstrator which provides an automated service to reliably detect, monitor, assess and predict floods at local and global scale within digital twin Franco-American collaboration. The main blocks of the processing chain are (I) flood detection and alert, (II) rapid flood extent mapping, and monitoring of on-going flood events, (III) representation and short-term forecasting of flood surfaces and free-surface elevation maps using high-fidelity hydrodynamic models over local areas, and (IV) real-time and post-event estimation and assessment of flood-related risks and economic impacts. 

FloodDAM-DT produces a near-real time (NRT) flood monitoring product by generating flood extent maps after detecting water level anomalies in the time series of in-situ stations. The goal of the second processing block is the generation of rapid flood extent maps at global scale within less than 11 minutes, once satellite acquisition is realised and provided. This product is produced using the open-source [FloodML](https://github.com/CNES/floodml) algorithm based on a Random Forest algorithm to detect flood extent from EO satellite data (Sentinel 2, Sentinel-1 VV-VH images, Landsat 8&9, Terrasar-X) along with MERIT or COPDEM GLO-30 DEM for SAR data, but also ESA World Cover. FloodML algorithm is trained on Copernicus EMSR cases, using samples for training and validation defined as areas having \>90% water occurrence. This way, the algorithm can train optical and SAR data to detect water either flooded or not in 

Sentinel-1 and Sentinel-2 images. Transfer learning method is then used for application on TerraSAR-X and Landsat products. New EO products might be integrated further on with the future launch of new satellite missions (for instance NISAR or ROSE-L SAR data), improving both time and space cover at a global scale, as well as a better detection of floodwater under vegetated areas.

In order to provide an a priori information of areas where flood might not be directly detected, the ESA World Cover has been integrated into the FloodML algorithm as shown in figure 5.2.3-1 here below with 8 levels of flooded surface classification.

![Flood Extent rapid mapping from EO satellite data](/figures/Figure5.2.3-1.png)  

*Figure 5.2.3-1 FloodML flood extent map from Sentinel-2 data, ESA World Cover and GSWO over the Ohio River flood event on the 27th February 2018*

All data produced within the FloodDAM framework is published on the Hydroweb.Next platform [https://hydroweb.next.theia-land.fr/](https://hydroweb.next.theia-land.fr/) , developed by CNES.

### 5.2.4. Wildfire

**GOAL:** GWSS (Global Wildfire System, OroraTech) is a near-real-time wildfire detection, alerting, and monitoring to support civil protection agencies, utilities, insurers, and asset operators. Provide risk assessment before ignition, early hotspot detection, and continuous situational awareness during incidents.

Expected outcomes, output format etc:   
•	Burn area classification, active fire detection, cloud/smoke detection & masking  
•	Alert feeds (API/SMS/Email), confidence/QA layers, incident dashboards (progressive web app), GeoTIFF rasters and vector perimeters (GeoJSON/GPKG).

**AI4EO example:** 

* Image Segmentation & Multi-sensor Fusion

Fuse thermal-infrared WITH optical detections; apply CNN segmentation (burn scars, severity via NBR/dNBR), active-fire classifiers, and object-based post-processing. Visualize and task via GWSS progressive web app.

* Scope

Problem statement and project scope  
Deliver global coverage with rapid revisit by combining public satellites and OroraTech’s proprietary thermal constellation; provide automated detection/alerts and incident analytics across customer Areas of Interest (AOIs). 

* Output  
  * 2 raster segmented images (GeoTIFF):  
    * Burn area/severity (unburned/low/mod/high)  
    * Active fire probability/intensity, with cloud/smoke mask  
  * Vector fire perimeters \+ incident report (area, severity stats, confidence, time).

* Verification Data sets  
  * CAL FIRE incident catalogue (US), EFFIS (EU), NASA FIRMS/agency reports for cross-checks and after-action review.  
  * Independent mission records for OroraTech satellites (e.g., FOREST-1).

**Documentation**  
Refer the document and doi.

* GWSS project page (ESA Business Applications) and ESA InCubed portfolio entries; mission docs for FOREST satellites;  
* ESA Business Applications – GWSS project page. Overview, objectives, system description. [business.esa.int](https://business.esa.int/projects/gwss)  
* ESA InCubed – OroraTech Wildfire Solution. Multi-sensor approach, PWA, market context. [incubed.esa.int](https://incubed.esa.int/portfolio/ororatechs-global-wildfire-warning/)  
* OroraTech press & product pages. Wildfire Solution capabilities; dedicated thermal constellation launches (2022–2025). [OroraTech](https://ororatech.com/all-products/wildfire-solution)  
* eoPortal mission pages. FOREST-1 satellite technical background and purpose. [eoportal.org](https://www.eoportal.org/satellite-missions/forest)

[^1]: This section was provided by Guy Schumann and is based on FloodSENS ML using Sentinel-2. Main paper is here: https://ieeexplore.ieee.org/document/10282274 for reference.
[^2]: This section was written by Raquel Rodriguez Suquet, and it is based on FloodML algorithm[[147](/references.md#ref.147)]

***

[Previous](climate.md) | [Table of contents](/README.md) | [Next](infrastructure-monitoring.md)
***
