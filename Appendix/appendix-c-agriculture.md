
## Agriculture

### Estimated paddy rice planted area

#### A \- General Definitions:

| Item | description |
| :---- | :---- |
| Application Area | Estimated paddy rice planted area |
| Goal | Rice acreage is estimated from satellite data in July, before the USDA (U.S. Department of Agriculture) releases its rice acreage for the year in October. |
| Method | Machine Learning(RandomForest) |
| Scope | Cooperative research with private companies |
| Input | \- |
|   Input Data Sets | ALOS-2 PALSAR-2 HH, HV |
|   Data Governance and Compliance  |  |
| Output | \- |
|   Output | Estimated image of paddy rice cropping area |
|   Data Governance and Compliance |  |
| Verification | \- |
|   Verification Data sets | USDA CDL(Cropland Data Layer) https://www.nass.usda.gov/Research\_and\_Science/Cropland/Release/index.php |
|   Data Governance and Compliance |  |
| Data collection processes | Data is collected by Python Program |
| Version Control | N/A |
| Lineage Information | N/A |
| Infrastructure | on-premise、Python (Tensorflow, Keras, scikit-learn) |
| Environment Management |  |
| Monitoring |  |
| Logging |  |
| Security and Privacy |  |
| Documentation |  |

#### B- MLOps related definitions / sections:

| Item | Description |
| :---- | :---- |
| Data Collection | ALOS-2 data used from JAXA AUIG2 |
| Data Indexing  | Date and time of data point added for time series analysis |
| Data Labeling | automated by Python Program |
| Data preprocessing | Speckle noise reduction by MedianFilter Normalized to 25m \=\> 30m resolution to match resolution with training data |
| Feature engineering | Creation of training data for drought |
| Data Verification | N/A |
| Data Splitting | 50/50 percent testing/training, |
