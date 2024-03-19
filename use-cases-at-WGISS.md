[Previous](usage-methods-of-ml-and-ai-for-eo.md) | [Table of contents](README.md) | [Next](data-and-platform.md)

***

# 6. Use cases at agency joined WGISS
This section indicates use cases of machine learning and AI conducted by CEOS/WGISS agencies. Application areas, Data, AI methods for each case are summarized in Table 5-1.

## 6.1. Agriculture
### 6.1.1. Estimated paddy rice planted area

#### A- General Definitions: 
- Application Area:Estimated paddy rice planted area
- Goal:Rice acreage is estimated from satellite data in July, before the USDA (U.S. Department of Agriculture) releases its rice acreage for the year in October. 
- Methode: Machine Learning(RandomForest)
- Scope: Cooperative research with private companies
- Data Sets:
  - Input Data Set: ALOS-2 PALSAR-2
    - HH,  HV
  - Output: [required]Estimated image of paddy rice cropping area
  - Verification Data set: [required]USDA CDL(Cropland Data Layer) https://www.nass.usda.gov/Research_and_Science/Cropland/Release/index.php
- Data is collected by Python Program
- Version Control and Lineage information: NA
- Infrastructure and Environment Management: on-premise、Keras、Python Cloud etc.,

#### B- MLOps related definitions / sections:
- Data Collection: ALOS-2 data used from JAXA AUIG2
- Data Indexing:Date and time of data point added for time series analysis?
- Data Labeling:automated by Python Program
- Data preprocessing: 
- Speckle noise reduction by MedianFilter
- Normalized to 25m => 30m resolution to match resolution with training data
- Feature engineering: Creation of training data for drought
- Data verification: NA
- Data splitting: 50/50 percent testing/training,

## 8.2. Marine monitoring
### 8.2.2. Sea ice-covered area

#### A - General Definitions: 

- Application Area: Sea ice-covered area
- Goal: Thin ice thickness of <20 cm is estimated from AMSR2 L1B data.
- Methode: Machine Learning (CNN)
- Scope: 
- Data Sets:
  - Input Data Set: AMSR2
  - Horizontal and vertical polarized brightness temperatures at 19, 23, 36 and 89 GHz
  - Output: Estimated thin ice thickness
  - Verification Data set:Thin ice thickness calculated from MODIS data. (2.5 km) 
- Data is collected by Python Program
- Version Control and Lineage information: NA
- Infrastructure and Environment Management: on-premise、Python (Tensorflow, Keras, scikit-learn)

#### B- MLOps related definitions / sections:

- Data Collection: AMSR2 data in JAXA G-portal.
- Data Indexing: Horizontal and vertical polarized brightness temperatures at 19, 23, 36 and 89 GHz, their polarization and gradient ratios, and thin ice thickness. 
- Data Labeling: For the MODIS thin ice thickness dataset, cloud-covered pixels are manually excluded by using QGIS.
- Data preprocessing: 
- Detected sea-ice area using AMSR-E sea ice concentration data.
- Applied a resolution enhancement method.
- Feature engineering: Calculated polarization and gradient ratios.
- Data verification:  
- Data splitting: 30/70 percent testing/training

## 8.3. Climate

### 8.3.3. Precipitation data

#### A - General Definitions: 

- Application Area: Precipitation data
- Goal: Bias correction of precipitation data from numerical weather prediction (MSM/GPV) by JMA in Japan
- Method: Support vector machine (SVM) regression with quantile-based bias correction (Yin et al., 2022)
- Scope:  For the use in hydrological prediction by Today’s Earth – Japan
- Data Sets:
  - Input Data Set: 
    - Radar-AMeDAS precipitation data by JMA
      - MSM/GPV precipitation data by JMA
  - Output: Bias corrected precipitation data
  - Verification Data set: Radar-AMeDAS precipitation data by JMA 
- Version Control and Lineage information: Classifier used for bias correction is updated approximately once in a year
- Infrastructure and Environment Management: on-premise, SciKit-Learn, Python

#### B- MLOps related definitions / sections:

- Data Collection: Radar-AMeDAS & MSM/GPV precipitation data from JMA
- Data Indexing: Date and time, lat/lon
- Data Labeling: Automated by Python Program
- Data preprocessing: 
- Divided into 5 regions to process in parallel. 
- Feature engineering: Bias correction with downscaling 
- Data verification:  
- Data splitting: 2007-2019 data for training, 2020 data for testing

## 8.x. Flood

## 8.x. Disaster

***
[Previous](usage-methods-of-ml-and-ai-for-eo.md) | [Table of contents](README.md) | [Next](data-and-platform.md)
