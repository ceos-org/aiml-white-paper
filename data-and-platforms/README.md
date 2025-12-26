[Previous](/hot-topics_new-topics/llms.md) | [Table of contents](/README.md) | [Next](/challenges-&-limitations-of-ai4eo/README.md)

***

# 7\. Data and platforms

This section introduces data and platforms used with machine learning and AI by CEOS/WGISS agencies indicated in the section 5\.

## 7.1. Data for AI/ML data interoperability

### 7.1.1. ESIP’s checklist

ESIP Data  Readiness Cluster developed the checklist to promote AI-readiness and Open Environmental Datasets. Data providers can evaluate their dataset for AI by this checklist and the results support understanding by AI application developers.  
The checklist consists 5 sections;   
- Part 1 \- General Info  
- Part 2 \- Data Quality  
- Part 3 \- Data Documentation  
- Part 4 \- Data Access  
- Part 5 \- Data Preparation

[Are Your Data Ready? Take Stock With ESIP’s New AI-Ready Checklist \- ESIP](https://www.esipfed.org/checklist-ai-ready-data/)  
[https://doi.org/10.6084/m9.figshare.19983722.v1](https://doi.org/10.6084/m9.figshare.19983722.v1)

### 7.1.2. CEOS-ARD

CEOS and the member organizations provide their data as Analysis Ready Data(ARD).  
CEOS‑ARD (CEOS Analysis‑Ready Data) is a framework and was developed by the Committee on Earth Observation Satellites (CEOS) to provide satellite observation data.  
They are pre-processed and standardized for immediate analysis.  
Additionally, CEOS‑ARD also includes "Product Family Specifications (PFS)" for various data types, such as optical, SAR (Synthetic Aperture Radar), surface reflectance over water, and nighttime lights, ensuring data quality and compatibility.  
They are used for disaster management and coastal monitoring including DE Africa.  
To use the data asAI/ML, they almost cover ESIP’s checklist without Part 4 and 5\. However CEOS ARDs provides Landing pages and there is related information about Part 4 and 5\. 

[CEOS Analysis Ready Data](https://ceos.org/ard/)

### 7.1.3. Pre-trained dataset

#### 7.1.3.1. BigEarthNet

BigEarthNet is a large-scale benchmark dataset, supporting deep learning (DL) studies for remote sensing image analysis. The recently released version of BigEarthNet (BigEarthNet v2.0) is made up of 549,488 pairs of Sentinel-1 and Sentinel-2 image patches acquired over 10 European countries \[[148](/references.md#ref.148)\].  
Each pair of patches in BigEarthNet is associated with a pixel-level reference map and scene-level multi-labels provided by the CORINE Land Cover (CLC) map of 2018\. To pay more justice to the properties of BigEarthNet image pairs, its developers introduced a new class-nomenclature by modifying the labels extracted from the CLC 2018\. To this end, the CLC Level-3 nomenclature is interpreted and arranged in a new nomenclature of 19 classes \[[149](/references.md#ref.149)\].  
The complete dataset, the code for constructing it in a reproducible manner and also the weights of several pre-trained models (which are: i) ResNet; ii) vision transformer; iii) MLP-Mixer; iv) ConvMixer; v) MobileViT; and vi) ConvNeXt-v2) using BigEarthNet are publicly available at [https://bigearth.net](https://bigearth.net).  
We would like to note that the public availability of the code developed for its construction allows all its users not only to reproduce the dataset but also to extend it to any geographical area of interest. Moreover, a software tool (called as rico-hdl) that converts the dataset into a DL-optimized data format has been recently released by its developers to minimize the DL model training time. For details, we refer the Reader to the dataset webpage [https://bigearth.net](https://bigearth.net).

### 7.1.4 Benchmark

#### 7.1.4.1. PhilEO Bench

PhilEO Bench is a benchmark framework to evaluate Foundation Models(FMs) and it is considered fair and reproducible.  
It provides a testbed and can be used for building density estimation, road segmentation and land cover classification. It provides 400 GB Sentinel-2 data with label.\[[150](/references.md#ref.150)\]

#### 7.1.4.2. PANGEA

PANGEA is a benchmark to evaluate Foundation Models(FMs) fairly.  
It uses various datasets;Opticals(Sentinel-2, Geofen-2, SPOT-6, Maxar, Planet), Radar(Sentinel-1) and Harmonized data(Harmonized Landsat and Sentinel-2).  
And it can be used for many tasks; Land cover, Forest monitoring, Disaster response, Wildfire detection, Flood detection, Marine monitoring and Agriculture monitoring.  
PANGAEA is also flexible, so it can be used for future research and new applications.\[[151](/references.md#ref.151)\]

## 7.2. Geospatial AI Platforms

Geospatial AI platforms are cloud-based computational systems that combine satellite imagery, remote sensing data, and geographic information with artificial intelligence and machine learning capabilities. These platforms provide researchers, government agencies, and private organizations with the tools to process and analyze large volumes of spatial data efficiently. By leveraging cloud computing infrastructure, users can perform complex geospatial analyses such as land cover classification, change detection, and environmental monitoring without requiring extensive local computational resources. The integration of AI algorithms enables automated pattern recognition, predictive modeling, and time-series analysis across diverse applications including urban planning, agricultural management, climate research, and natural resource monitoring. These platforms have become essential tools for evidence-based decision-making in fields that require spatial and temporal analysis of Earth observation data.  
Some of the commonly used platforms (not an exhaustive listing) in this category are listed in this section for reference and further exploration.

Table 6.2-1 Geospatial AI Platforms

| Platform | URL | Description & Capabilities | Key Features | Typical Datasets |
| :---- | :---- | :---- | :---- | :---- |
| **Google Earth Engine (GEE)** | **https://[earthengine.google.com](https://earthengine.google.com/)** | Cloud-based large-scale geospatial analysis platform with petabyte archives. | ML-ready APIs, Python ,scalable image analysis, visualization. | Landsat, Sentinel, MODIS, VIIRS, climate, hydrology, land cover. |
| **Microsoft Planetary Computer** | **https://[planetarycomputer.microsoft.com](https://planetarycomputer.microsoft.com/)** | Combines massive environmental datasets with Azure-scale compute. | STAC API, JupyterHub integration, Python/xarray/geopandas support. | Sentinel, Landsat, NAIP, ERA5, CMIP6, biodiversity (GBIF). |
| **NASA Earthdata (ESDS)** | **https://[earthdata.nasa.gov](https://earthdata.nasa.gov/)** | Gateway to NASA’s ≥60 PB Earth science archive, models, reanalyses. | Cloud-based APIs, DAACs for science domains, Giovanni visualization. | MODIS, VIIRS, SMAP, TRMM, CERES, atmospheric & ocean records. |
| **ESA Climate Change Initiative (CCI)** | **https://[climate.esa.int](https://climate.esa.int/en/esa-climate/)** | Long-term harmonized climate datasets, focus on Essential Climate Variables. | Curated ECVs, benchmarks for EO+AI through ESA AI4EO. | Land cover, greenhouse gases, soil moisture, ocean color, fire, glaciers. |
| **Radiant Earth MLHub** | **https://radiant.earth/** | Open ML training data hub for geospatial AI benchmarks. | STAC-compliant labeled datasets, benchmarks for competitions. | Sentinel-2, Landsat with ground-truth, agricultural & disaster labels. |
| **Euro Data Cube (EDC)** | **https://[eurodatacube.com](https://eurodatacube.com/)** | EU-based hosted analytics environment for Earth Observation datasets. | Access to Sentinel, Landsat, custom cubes; Notebook environment; service marketplace. | Sentinel-1, Sentinel-2, Sentinel-3, Landsat, Copernicus services. |
| **AI4EO (ESA AI for Earth Observation Initiative)** | [**ai4eo.eu**](https://ai4eo.eu/) | ESA-supported initiative advancing AI/ML for EO with challenges and tools. | Benchmarks, data challenges, ML datasets for research. | Sentinel, Copernicus open datasets, thematic AI challenge datasets. |
| **IBM Environmental Intelligence Suite** | [**ibm.com/products/environmental-intelligence-suite**](https://www.ibm.com/products/environmental-intelligence-suite) | Enterprise solution for climate risk and environmental intelligence. | Climate/Weather risk dashboards, supply chain integration, AI forecasting. | Weather Company data, climate models, EO data integrations. |
| **AWS Earth on Open Data / Amazon SageMaker Geospatial Capabilities** | [**registry.opendata.aws**](https://registry.opendata.aws/) **& [aws.amazon.com/sagemaker/geospatial/](https://aws.amazon.com/sagemaker/geospatial/)** | Petabyte-scale open geospatial datasets and AI/ML integration in cloud. | Registry of open Earth data, scalable analytics, SageMaker ML integration. | Landsat, Sentinel, DEMs, climate reanalysis, aerial imagery, OpenStreetMap |
| **VEDAS by ISRO** | **https://vedas.sac.gov.in/** | Large scale resource monitoring and analysis for Indian region | Data visualization, Analytics with API access and prepared Catalogues | Resourcesat, Sentinel, Cartosat datasets  |

***

[Previous](/hot-topics_new-topics/llms.md) | [Table of contents](/README.md) | [Next](/challenges-&-limitations-of-ai4eo/README.md)


The key advantage of using established geospatial AI platforms over self-developed infrastructures is their ability to drastically reduce technical, computational, and financial barriers to large-scale Earth observation analysis. These platforms provide immediate access to petabyte-scale, analysis-ready datasets—such as satellite constellations, climate reanalysis models, and labeled training archives—eliminating the immense effort required to collect, preprocess, and store such data independently. They offer cloud-based computing environments, integrated AI/ML workflows, and standardized APIs, which allow researchers to focus on scientific inquiry and innovation rather than infrastructure management. Importantly, the low barrier of entry—often through free tiers, open-access datasets, or academic licensing—empowers researchers, NGOs, and governments alike, enabling cutting-edge environmental monitoring and decision-making capabilities even for institutions with limited resources. In essence, these platforms democratize access to planetary-scale intelligence, making impactful geospatial AI research both more efficient and more inclusive. The platforms also aid in reproducible research as the experiments can be exactly explained along with the environment and the data used.
