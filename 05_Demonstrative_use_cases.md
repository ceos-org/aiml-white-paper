[Previous](/programs-and-initiatives/gistda.md) | [Table of contents](/README.md) | [Next](climate.md)

***

# 5\. Demonstrative use-cases<a id='5.0'></a> 

　There are numerous AI/ML approaches commonly applied to domains such as computer vision and Satellite Image Processing. In this section, examples of these approaches and how they can be applied to Earth Observation data are presented. This overview highlights example EO applications for various themes and is intended as a guide rather than a comprehensive or exclusive list. 

- [**5\. Demonstrative use-cases**](#5.0)
  - [5.1. Climate](#5.1)
  - [5.2. Disaster](#5.2)
  - [5.3. Infrastructure Monitoring](#5.3)
  - [5.4. Precipitation](#5.4)
  - [5.5. Sustainable Finance](#5.5)

***

## 5.1. Climate<a id='5.0'></a> 

### 5.1.1. Mapping glacier grounding lines {#5.1.1.-mapping-glacier-grounding-lines}

**GOAL:**
AI/ML are becoming integral to climate science, offering new methods to analyze the vast and complex datasets produced by satellites, in-situ measurements, and climate models. For example,  artificial intelligence can improve monitoring of ice-sheet dynamics by automatically mapping grounding lines, which are the boundary where glaciers transition from grounded ice to floating ice shelves (Mohajerani et al. (2021)). Accurate delineation of these lines is crucial for understanding ice-sheet stability and sea level rise.

**AI4EO example:**
Mohajerani et al. (2021) applied a deep learning model to Differential Interferometric Synthetic Aperture Radar (DInSAR) data from the Sentinel-1 A/B satellites, training it to recognize grounding line signatures in complex interferometric phase patterns. Unlike traditional manual delineation or threshold-based techniques, the AI approach processes large datasets quickly and consistently, reducing human error and improving efficiency.

The figure below compares grounding lines derived by the deep learning model against those mapped manually. The AI-generated line (black) closely overlaps with the expert-drawn reference (white line), illustrating the accuracy and reliability of the automated approach. This example highlights the potential of AI/ML to scale up glacier and ice-sheet monitoring for climate studies and sea level rise projections.

![Different steps of the pipeline for (a) a sample interferogram with hand-drawn grounding line in white](/figures/Figure5.1.1-1.png)  
Figure 5.1.1-1 Different steps of the pipeline for (a) a sample interferogram with hand-drawn grounding line in white; (b) output of the neural network in raster format with a variable width that is a measure of uncertainty of the output. The gray mask in the background represents training (white) and testing (gray) sites; (c) Vectorized output and uncertainty contours; (d) zoomed-in region highlighted by the maroon box in panel (c) showing both manual and ML results and uncertainty bars; (e) Comparison of the manual and ML performances in the area outlined in blue in panel (c).

### 5.1.2. Thin ice thickness

**GOAL:**
The application of AI/ML in sea ice research has expanded into a wide range of tasks, including the estimation of sea ice concentration, thickness, and drift, classification of ice types, detection of ice edges, leads, and melt ponds, and seasonal forecasting of sea ice distributions. In particular, most studies have focused on these tasks using SAR and optical sensors with high spatial resolution. On the other hand, passive microwave radiometers such as AMSR2 and SSM/I, which can globally observe Earth’s surface regardless of day/night conditions or cloud cover and have long been utilized for climate monitoring, have also seen progress in AI/ML-based applications. One example is the retrieval of thin ice thickness. In winter, coastal polynyas, thin ice regions surrounded by pack ice and coasts, experience substantial heat loss to the atmosphere, resulting in the formation of large amounts of sea ice. The dense water formed in association with this sea ice production partly intrudes into the subsurface, intermediate, and deep oceans and drives the overturning circulation and material cycles such as CO₂. Information on thin ice thickness is therefore indispensable for estimating sea ice production, and many studies have developed thin ice thickness retrieval algorithms. Most of these algorithms rely on deriving simple empirical equations by comparing ice thickness obtained from thermal infrared sensors with microwave radiometer data. Such empirical formulations can be replaced by AI/ML methods with greater representational power, offering the potential for improved accuracy.

**AI4EO example:**
Nakata et al. (in prep.) employed a NN model to estimate thin ice thickness below 20 cm across the entire Antarctic sea ice region. To construct a highly generalizable retrieval model, a large volume of high-quality training data was required. They used a total of \~200,000 training samples, consisting of accurate thin ice thickness and thin/thick ice types derived from MODIS data. As input, instead of directly using AMSR2 L1B brightness temperature data (18, 36, and 89 GHz; spatial resolutions of 20 km, 10 km, and 5 km, respectively), they used corrected brightness temperatures obtained through the following preprocessing steps. First, the radiometer version of the Scatterometer Image Reconstruction (rSIR) method was applied to downscale the data to grid spacings of 10 km, 5 km, and 2.5 km. Second, a unidirectional variation model was used to remove stripe noise. Furthermore, the influence of atmospheric water vapor was corrected using a simplified radiative transfer model. To address thin ice retrieval, they employed a simple three-layer neural network that outputs both thin ice thickness and thin ice probability, trained with a loss function combining mean squared error for regression and binary cross-entropy for thin ice classification. As a result, the retrieved thin ice thickness dataset demonstrated remarkable improvements compared to previous algorithms. As shown in Figure 1, the comparison between a previous algorithm and the AI/ML approach demonstrates that, with appropriate preprocessing and the use of a neural network, thin ice distribution can be represented with higher accuracy and greater detail.

![Thin ice thickness](/figures/Figure5.1.2-1.png)  
Figure 5.1.2-1\. (a) Thin ice area (yellow regions) derived from the previous algorithm. (b) Pseudo-color composite image derived from the AI/ML approach (Red: thin ice probability, 50–100%; Green: thin ice thickness, 20–0 cm).

***
## 5.2. Disaster<a id='5.2'></a> 

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
## 5.3. Infrastructure Monitoring<a id='5.3'></a> 

**GOAL:** EO for infrastructure management are relatively novel, with emerging applications that integrate satellite-based Synthetic Aperture Radar Interferometry (InSAR) with civil engineering modelling and ground instrumentation for structures such as bridges (e.g. [Selvakumaran et al. (2018)](https://www.sciencedirect.com/science/article/pii/S0303243418303052), [Cusson et al. (2020)](https://link.springer.com/article/10.1007/s13349-020-00446-9)) and mine tailings (e.g. [Bayaraa et al. (2024)](https://www.emerald.com/jgeot/article-abstract/74/10/985/1213047/InSAR-and-numerical-modelling-for-tailings-dam?redirectedFrom=fulltext)). 

In parallel, deep learning approaches have been applied to detect ground deformation over critical infrastructure such as tunnels or gas / water extraction ([Anantrasirichai et al. (2020)](https://ieeexplore.ieee.org/abstract/document/9181454)) and airports ([Ma et al. (2020)](https://www.tandfonline.com/doi/abs/10.1080/2150704x.2019.1692390)). Of particular importance are mine tailings, where early detection of anomalous deformation may help protect the surrounding communities and the environment from catastrophic failures of toxic mine waste ([Bayaraa et al. (2023)](https://www.mdpi.com/2072-4292/15/20/4910))). 

**AI4EO example:** A variety of data science approaches, from deep learning to shallow machine (e.g. random forest) models and probabilistic models such as gaussian process regression have shown promise in detecting anomalous deformation signals from InSAR (e.g. [Bayaraa et al. (2023)](https://www.mdpi.com/2072-4292/15/20/4910)). Example is in Figure 5.3-1.  

![Infrastructure Monitoring](/figures/Figure5.3-1.png)  
Figure 5.3-1: Use of machine learning approaches for detecting anomalous deformation signals from satellite InSAR data. (a) InSAR data visualised spatially over the Cadia tailings dam. © ESA Sentinel-2data and ISBAS InSAR data © Terra Motion. (b) Zoom in to the failed area of the dam. Basemap image copyright © 2021 Maxar Technologies, © CNES/Airbus, © Google Earth. (c) An example of an InSAR measurement showing a typical linear deformation with all test measurements within uncertainty envelope of Gaussian Process Regression. (d) An example of anomalous deformation behaviour, with the last four measurements (in blue) falling significantly outside the uncertainty envelope. Modified with permission from [Bayaraa et al. (2023)](https://www.mdpi.com/2072-4292/15/20/4910). 

***
## 5.4. Precipitation<a id='5.4'></a> 

**GOAL :**
Bias correction of precipitation forecast data from numerical weather prediction (MSM/GPV) by JMA in Japan. Finally aiming at the utilization for hydrological simulation.

**METHOD :**
Assuming a relationship between observed precipitation and the areal precipitation distribution reproduced by numerical weather forecasts, we applied machine learning to correct precipitation bias. Specifically, the target variable was observed precipitation (JMA’s in-situ and ground radar–based observations, Radar-AMeDAS), while the predictor variable was precipitation from the JMA mesoscale numerical forecast model (MSM) 39-hour forecasts. The relationship was trained using data from 2007 to 2020\. Bias correction was then performed by estimating precipitation at the center of the distribution from forecast precipitation distributions not included in training. After correcting the spatial distribution with a support vector machine (SVM), additional quantitative adjustments for precipitation associated with individual convective clouds and squall lines—phenomena that are difficult to capture with machine learning—were made using a statistical method known as cumulative distribution function transform (CDFt).Support vector machine (SVM) regression with quantile-based bias correction For more detail, please refer to (Yin et al., 2022.)  
 [https://doi.org/10.1016/j.jhydrol.2022.128125](https://doi.org/10.1016/j.jhydrol.2022.128125).  
This method is now operationally used in “[Today’s Earth \- Japan](https://www.eorc.jaxa.jp/water/index.html)”, which is terrestrial hydrological simulation system for Japan, developed  by Japan Aerospace Exploration Agency (JAXA) and the University of Tokyo (see the [document](https://www.eorc.jaxa.jp/water/documents/TodaysEarth_20240702_e.pdf) for more detailes).

![Averaged hourly precipitation in January](/figures/Figure5.4-1.png)  
Figure 5.4-1: Averaged hourly precipitation in January from (a) Radar-AMeDAS, (b) MSM-GPV, (c) QM, and (d) CDFt, (e) SVM, (f) SVM-QM, and (g) SVM-CDFt. The  statistical metrics evaluated against Radar-AMeDAS were shown in each subplot, and the units for R, RMSE, and bias are unitless, mm/hr, and mm/hr, respectively. Modified with permission from [Yin et al., 2022](https://doi.org/10.1016/j.jhydrol.2022.128125)

***
## 5.5. Sustainable Finance<a id='5.5'></a> 

**GOAL :**
Leverage the global coverage of satellite data to develop comprehensive datasets that support sustainable finance initiatives. The financial sector often encounter challenges such as incomplete or missing data, particularly when assessing emissions-intensive industries and assets.

**AI4EO example:**
Use of a variety of advanced deep learning approaches with satellite data to find and characterise cement assets (e.g. [Rossi et al. (2022)](https://ieeexplore.ieee.org/abstract/document/9883772) and [Tkachenko et al. 2023](https://www.nature.com/articles/s41597-023-02599-w)).

- Example task 1: cement plant assets identified and characterised through CNNs from high resolution multi-spectral satellite data (e.g. Worldview-4).   
- Example task 2: cement plant assets identified and classified through thermal infra-red satellite data.   
- Example task 3: metadata for cement plant assets are searched through LLMs and webscraping.   

![Use of deep learning and satellite data for characterising global cement assets](/figures/Figure5.5-1.png)  
Figure 5.6-1: Use of deep learning and satellite data for characterising global cement assets. Modified with permission from [Rossi et al. (2022)](https://ieeexplore.ieee.org/abstract/document/9883772).

***


[Previous](/programs-and-initiatives/gistda.md) | [Table of contents](/README.md) | [Next](climate.md)
