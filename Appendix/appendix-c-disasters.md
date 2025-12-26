## Disasters

### A \- General Definitions:

| Item | description |
| :---- | :---- |
| Application Area | Flood extent mapping at global scale |
| Goal | the goal of FloodML algorithm is to detect flood extent at global scale  from EO satellite data (optical and SAR data) |
| Method | Random Forest algorithm trained on Copernicus EMSR past flood event cases, using samples for training and validation defined as areas having \>90% water occurrence. |
| Scope | For the use on operational flood crisis management  |
| Input | Date of flood event ROI preprocessed optical and SAR data   |
|   Input Data Sets | EO SAR data : Sentinel-1 and TerraSAR-X EO optical data : Sentinel-2, Landsat 8&9 DEM : MERIT or COPDEM GLO-30 DEM for SAR Data ESA World Cover for land classification   |
|   Data Governance and Compliance  | Term of use for input dataset. |
| Output | binary flood extent maps flood  flood extent maps with 8 levels of flooded surface classification |
|   Output | 2 rasters (.tiff) |
|   Data Governance and Compliance | Term of use for output dataset. |
| Verification |  |
|   Verification Data sets | flood sites and events from  Copernicus EMSR datasets ([https://mapping.emergency.copernicus.eu/](https://mapping.emergency.copernicus.eu/) ) |
|   Data Governance and Compliance |  |
| Data collection processes | All data produced is accessible in the open hydrological platform [https://hydroweb.next.theia-land.fr/](https://hydroweb.next.theia-land.fr/)  |
| Version Control | v1.1 (cf. open-source FloodML algorithm [https://github.com/CNES/floodml](https://github.com/CNES/floodml) developed by CNES and CLS group) |
| Lineage Information |  |
| Infrastructure | Python, conda |
| Environment Management |  |
| Monitoring |  |
| Logging | to access product using the open hydrological platform [https://hydroweb.next.theia-land.fr/](https://hydroweb.next.theia-land.fr/)  |
| Security and Privacy |  |
| Documentation | open-source FloodML algorithm [https://github.com/CNES/floodml](https://github.com/CNES/floodml) developed by CNES and CLS group DOI : 10.5281/zenodo.16565154 |

### B- MLOps related definitions / sections:

| Item | Description |
| :---- | :---- |
| Data Collection | Sentinel-1&2, Landsat 8&9, TerraSAR-X |
| Data Indexing  | Date and time, lat/lon |
| Data Labeling | The reference data is sourced from the labeled flood extent provided by the Copernicus Emergency Management Service (EMS) Rapid Mapping |
| Data preprocessing | Data preprocessing on Sentinel-2 L2A Data preprocessing on Sentinel-1 using S1tiling ([https://github.com/CNES/S1Tiling](https://github.com/CNES/S1Tiling) ) |
| Feature engineering |  |
| Data Verification |  |
| Data Splitting | data splitting for training, validation and test datasets |
