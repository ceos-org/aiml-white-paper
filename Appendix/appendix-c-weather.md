## Weather

### A \- General Definitions:

| Item | description |
| :---- | :---- |
| Application Area | Precipitation data |
| Goal | Bias correction of precipitation data from numerical weather prediction (MSM/GPV) by JMA in Japan |
| Method | Support vector machine (SVM) regression with quantile-based bias correction (Yin et al., 2022\) |
| Scope | For the use in hydrological prediction by Today’s Earth – Japan |
| Input |  |
|   Input Data Sets | Radar-AMeDAS precipitation data by JMA MSM/GPV precipitation data by JMA |
|   Data Governance and Compliance  |  |
| Output |  |
|   Output | Bias corrected precipitation data |
|   Data Governance and Compliance |  |
| Verification |  |
|   Verification Data sets | Radar-AMeDAS precipitation data by JMA |
|   Data Governance and Compliance |  |
| Data collection processes |  |
| Version Control | Classifier used for bias correction is updated approximately once in a year |
| Lineage Information | Classifier used for bias correction is updated approximately once in a year |
| Infrastructure | on-premise, SciKit-Learn, Python |
| Environment Management |  |
| Monitoring |  |
| Logging |  |
| Security and Privacy |  |
| Documentation |  |

### B- MLOps related definitions / sections:

| Item | Description |
| :---- | :---- |
| Data Collection | Radar-AMeDAS & MSM/GPV precipitation data from JMA |
| Data Indexing  | Date and time, lat/lon |
| Data Labeling | Automated by Python Program |
| Data preprocessing | Divided into 5 regions to process in parallel. |
| Feature engineering | Bias correction with downscaling |
| Data Verification |  |
| Data Splitting | 2007-2019 data for training, 2020 data for testing |
