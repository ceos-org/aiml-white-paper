## Climate

### Sea ice-covered area

#### A \- General Definitions:

| Item | description |
| :---- | :---- |
| Application Area | Sea ice-covered area |
| Goal | Thin ice thickness of \<20 cm is estimated from AMSR2 L1B data. |
| Method | Machine Learning (CNN) |
| Scope |  |
| Input |  |
|   Input Data Sets | AMSR2 Horizontal and vertical polarized brightness temperatures at 19, 23, 36 and 89 GHz |
|   Data Governance and Compliance  |  |
| Output |  |
|   Output | Estimated thin ice thickness |
|   Data Governance and Compliance |  |
| Verification |  |
|   Verification Data sets | Thin ice thickness calculated from MODIS data. (2.5 km) |
|   Data Governance and Compliance |  |
| Data collection processes | Data is collected by Python Program |
| Version Control | N/A |
| Lineage Information | N/A |
| Infrastructure | on-premise、Python (Tensorflow, Keras, scikit-learn)  |
| Environment Management |  |
| Monitoring |  |
| Logging |  |
| Security and Privacy |  |
| Documentation |  |

#### B- MLOps related definitions / sections:

| Item | Description |
| :---- | :---- |
| Data Collection | AMSR2 data in JAXA G-portal. |
| Data Indexing  | Horizontal and vertical polarized brightness temperatures at 19, 23, 36 and 89 GHz, their polarization and gradient ratios, and thin ice thickness. |
| Data Labeling | For the MODIS thin ice thickness dataset, cloud-covered pixels are manually excluded by using QGIS. |
| Data preprocessing | Detected sea-ice area using AMSR-E sea ice concentration data. Applied a resolution enhancement method. |
| Feature engineering | Calculated polarization and gradient ratios. |
| Data Verification |  |
| Data Splitting | 30/70 percent testing/training |
