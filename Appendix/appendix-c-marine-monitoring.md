## Marine monitoring

### Monitoring for oil slick in coastal seas

#### A \- General Definitions:

| Item | description |
| :---- | :---- |
| Application Area | Monitoring coastal waters for oil slick occurrence |
| Goal | Detection of oil slicks within the Exclusive Economic Zone (EEZ) from satellite data, providing either warning of a developing spill event or long-term monitoring to assess trends in smaller spill occurrence. |
| Method | Machine Learning (Random Forest, multi-layer perceptron) |
| Scope | Service co-development with national marine pollution monitoring entities |
| Input | \- |
|   Input Data Sets | Sentinel-1, Capella Space VV |
|   Data Governance and Compliance  |  |
| Output | \- |
|   Output | Estimated oil slick location and area within each scene |
|   Data Governance and Compliance |  |
| Verification | \- |
|   Verification Data sets | Publications, SkyTruth, USCG National Response Center |
|   Data Governance and Compliance |  |
| Data collection processes | Data is provided by Copernicus and processed in python |
| Version Control | N/A |
| Lineage Information | N/A |
| Infrastructure | On-premise HPC, python (scikit-learn), java (WEKA) |
| Environment Management | Singularity, conda |
| Monitoring |  |
| Logging |  |
| Security and Privacy |  |
| Documentation |  |

#### B \- MLOps related definitions / sections:

| Item | Description |
| :---- | :---- |
| Data Collection | Sentinel-1A/B data, VV channel Capella Space constellation data, VV mode |
| Data Indexing | Acquisition date and time stamp |
| Data Labelling |  |
| Data preprocessing | Speckle noise reduction, pixel spatial resolution reduction (Capella) mask land area Produce candidate objects with dark object clustering |
| Feature engineering | Creation of training data for oil slick detection |
| Data Verification | N/A |
| Data Splitting | 50/50 percent testing/training |

 

### Coastal and transitional water quality

#### A \- General Definitions:

| Item | description |
| :---- | :---- |
| Application Area | Nearshore and transitional water quality indicator parameters |
| Goal | Provide regional high quality monitoring data from satellite on chlorophyll-a (indicator of algal activity) and total suspended matter (indicator of sedimentation in the water) |
| Method | Machine Learning (fuzzy c-mean clustering) |
| Scope | Cooperative research with regional transitional water system (deltas, estuaries, lagoons, etc) research experts and monitoring entities |
| Input | \- |
|   Input Data Sets | Sentinel-2, Sentinel-3 |
|   Data Governance and Compliance  |  |
| Output | \- |
|   Output | Improved estimation of chlorophyll-a and total suspended matter for brackish water systems |
|   Data Governance and Compliance |  |
| Verification | \- |
|   Verification Data sets | In-situ samples collected by field teams or installed sensors on buoys, bridges, etc. |
|   Data Governance and Compliance |  |
| Data collection processes | Data is provided by Copernicus and processed in python |
| Version Control | yes |
| Lineage Information | N/A |
| Infrastructure | Either on-premise or cloud HPC, python (scikit-learn, xarray) |
| Environment Management | Singularity, cylc rose-suite, conda |
| Monitoring |  |
| Logging |  |
| Security and Privacy |  |
| Documentation |  |

#### B- MLOps related definitions / sections: 

| Item | Description |
| :---- | :---- |
| Data Collection | Sentinel-2A/B, Sentinel-3A/B |
| Data Indexing | Acquisition date and time stamp |
| Data Labeling |  |
| Data preprocessing | Atmospheric correction with POLYMER or blended POLYER/ACOLITE |
| Feature engineering | Data normalization using log and PCA Pan-regional cluster creation built sequentially from separate regional analyses over six European transitional water systems |
| Data Verification | Comparison with in-situ field data |
| Data Splitting | 40/60 percent testing/training where water quality indicator candidate algorithms are recalibrated per fuzzy clustering Optical Water Type (OWT) class |
