# Appendix C. Templates for use case

The following is a general template. It should be noted that it might need updates, additions etc., depending on the use case in hand. For example in the case of transfer learning flow might need to be adjusted accordingly. 

- [Climate](appendix-c-climate.md)
- [Disaster](appendix-c-disasters.md)
- [Marine Monitoring](appendix-c-marine-monitoring.md)
- [Weather](appendix-c-weather.md)

Note: Following template is summarized from the ITU Data report\[[153](/references.md#ref.153)\]. This report needs to be included in the references. 

**Use case Example:**

## A \- General Definitions:

| Item | description | example |
| :---- | :---- | :---- |
| Application Area | Subject | wildfires |
| Goal | Expected outcomes, output format etc | Burn area classification, Active fire detection, Cloud detection |
| Method | Main point | Image Segmentation |
| Scope | Problem statement and project scope |  |
| Input | \- | \- |
|   Input Data Sets |  | LandSat 8,9 |
|   Data Governance and Compliance  | Governance of compliance requirements specific to your CEOS Agency | Term of use for input dataset. |
| Output | \- | \- |
|   Output |  | 2 raster segmented Images |
|   Data Governance and Compliance | Governance of compliance requirements specific to your CEOS Agency | Term of use for output. |
| Verification | \- | \- |
|   Verification Data sets |  | CAL Fire https://www.fire.ca.gov/incidents |
|   Data Governance and Compliance | Governance of compliance requirements specific to your CEOS Agency | Term of use for output. |
| Data collection processes |  | Data is collected from USGS (Method) Automated |
| Version Control | Track different versions of datasets and ensure that models are trained on specific dataset versions. |  |
| Lineage Information | How data is transformed, aggregated, or derived to identify potential sources of errors or bias in the models. |  |
| Infrastructure | Required infrastructure and cloud platform for running models | AWS, Azure, GCP |
| Environment Management | Software dependencies and libraries needed for model training and deployment | PyTorch, conda,  |
| Monitoring | Key performance metrics to monitor model performance in production. |  |
| Logging | logging practices to capture relevant information for debugging and analysis. |  |
| Security and Privacy | Measures ensuring the confidentiality, integrity, and availability of data in the ML lifecycle, including data encryption, access control, anonymization, and secure storage. | ·       Input and output datasets are encrypted in transit and at rest using TLS and AES-256. ·       Role-based access control (RBAC) enforced for sensitive satellite imagery. ·       Personally identifiable information (PII) is anonymized or excluded. ·       Compliance with GDPR or other regional data protection regulations.  |
| Documentation | Refer the document and doi. | https://doi.org/xxxxxx |

## B- MLOps related definitions / sections:

| Item | Description | Example |
| :---- | :---- | :---- |
| Data Collection | Define data collection processes and data schema. | LandSat data used from cloud |
| Data Indexing  | Create an index or catalog of the available data, describing each dataset's metadata, schema, and data lineage.  | Date and time of data point added for time series analysis |
| Data Labeling | If there is any labeling describe the labeling methods (strategies for manual or automated data labeling). | Semi automated texture analysis |
| Data preprocessing | Define and automate data preprocessing steps, such as normalization, scaling, handling missing values, and outlier detection. | On the fly data normalization,  band resolution adjustment SW channel 60 meter resolution, NIR 30 meter resolution. |
| Feature engineering | Describe how  relevant features from raw data are retrieved in the automated process. Explain if scalability and reproducibility are considered in the flow. | Different channels used for different purposes.  For Example, blue channel used for cloud detection for quality control, NIR, SW1 combination for burned area and fire detection. |
| Data Verification | Verify if data usable by the rest of the process | Automatic data verification: e.g, 70% cloud detected; stop process |
| Data Splitting | How data is divided into training, validation, and testing sets. Split ratios? | 20/80 percent testing/training, 5 fold |
