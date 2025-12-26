## Appendix D. [Surface Reflectance (Optical)](https://github.com/ceos-org/ceos-ard/blob/main/Specifications/Surface-Reflectance/README.md)

### Data Preparation

| Have null values/gaps been filled? | Requirements \-\>Per-Pixel Metadata 2.2 No Data Pixels that do not correspond to an observation (‘empty pixels’) are flagged. |
| :---- | :---- |
| Have outliers been identified? | I couldn't find the description about range for values in CEOS ARD. |
| Is the data single-source or aggregated from several sources? | Requirements \-\>General Metadata 1.2 Metadata Machine Readability Metadata is provided in a structure that enables a computer algorithm to be used consistently and to automatically identify and extract each component part for further use |
| Has the data been gridded (regularized in space and time) or is it in the originally sampled resolution? | Requirements \-\>General Metadata 1.3 Data Collection Time 1.6 Map Projection 1.7 Geometric Correction Methods 1.8 Geometric Accuracy of the Data Probably, ARD satisfies the requirements by those requirements |
| Have targets been identified and labeled (i.e. can this be used as a training dataset for supervised learning techniques)? | This require comes from AI/ML aspect, so CEOS ARD doesn't include this requirement. |

### Data Quality

| Have measures been taken to ensure completeness? | Requirements \-\>Per-Pixel Metadata 2.3 Incomplete Testing The metadata identifies pixels for which the per-pixel tests (below) have not all been successfully completed. Note 1: This may be the result of missing ancillary data for a subset of the pixels. |
| :---- | :---- |
| Are there automated processes to monitor consistency? | Requirements \-\>General Metadata 1.15 Processing Chain Provenance (desired) Information on processing chain provenance should be available in the metadata as a single DOI landing page containing detailed description of the processing steps used to generate the product, including the versions of software used, giving full transparency to the users. |
| Have measures been taken to reduce bias? | This require comes from AI/ML aspect, so CEOS ARD doesn't include this requirement. |
| What is the timeliness of the data? (Near real-time,1 week, 1 month, 1 year, more than 1 year) | I couldn't find this requirement at CEOS ARD, but data provider might show timeliness with dataset. |
| Is there a difference between raw near real-time access vs fully quality-controlled data that has an additional delay? | I couldn't find this requirement at CEOS ARD, but data provider might show timeliness with dataset. |
| Are there quantitative measures of uncertainty? | Requirements \-\>General Metadata 1.17 Overall Data Quality (desired) Machine-readable metrics describing the overall quality of the data are included in the metadata, at minimum the cloud cover extent, i.e.: \- Proportion of observations over land (c.f. ocean) affected by non-target phenomena, e.g., cloud and cloud shadows |
| Is there quantitative information about data resolution in space and time? | Requirements \-\>General Metadata 1.8 Geometric Accuracy of the Data. (desired) The metadata includes metrics describing the assessed geodetic accuracy of the data, expressed units of the coordinate system of the data. Accuracy is assessed by independent verification (as well as internal model-fit where applicable). Uncertainties are expressed quantitatively, for example, as root mean square error (RMSE) or Circular Error Probability (CEP90, CEP95), etc. Note 1: Information on geometric accuracy of the data should be available in the metadata as a single DOI landing page. 1.12 Radiometric Accuracy (desired) The metadata includes metrics describing the assessed absolute radiometric uncertainty of the version of the data or product, expressed as absolute radiometric uncertainty relative to appropriate, known reference sites and standards (for example, pseudo-invariant calibration sites, rigorously collected field spectra, PICS, Rayleigh, DCC, etc.) Note 1: Information on radiometric accuracy should be available in the metadata as a single DOI landing page. |
| Are there published data quality procedures or reports? (Link to reports) | Requirements \-\>General Metadata 1.17 Overall Data Quality (desired) Machine-readable metrics describing the overall quality of the data are included in the metadata, at minimum the cloud cover extent, i.e.: \- Proportion of observations over land (c.f. ocean) affected by non-target phenomena, e.g., cloud and cloud shadows |
| Is the provenance tracked and documented? | Requirements \-\>General Metadata 1.15 Processing Chain Provenance (desired) Information on processing chain provenance should be available in the metadata as a single DOI landing page containing detailed description of the processing steps used to generate the product, including the versions of software used, giving full transparency to the users. |
| Are there checksums / other checks for data integrity? | I can't find this requirement in CEOS ARD. |
| How big is the dataset? Depending on the resource, this might be total data volume, dimensionality, number of images, data files, table rows, image size, etc. | I couldn't find this requirement at CEOS ARD, but data provider might show related information to support users can estimate. |
| Is this essentially raw data or a derived/processed data product? | I couldn't find this requirement at CEOS ARD, but data provider might show related information to support users can estimate. |
| Is this observational data or simulation/model output? | ALL of the CEOS ARD may be the observational data. |
| Has the data been peer-reviewed? | Requirements \-\>General Metadata 1.13 Algorithms (desired) As threshold, but only algorithms that have been published in a peer-reviewed journal. Note 1: It is possible that high quality corrections are applied through non-disclosed processes. CEOS-ARD does not per-se require full and open data and methods. Note 2: Information on algorithms should be available in the metadata as a single DOI landing page. |
| Has it been down-sampled to reduce resolution, or is it raw? If so, are the raw data available? | I couldn't find this requirement at CEOS ARD, but data provider might show related information to support users can estimate. |

### Data Documentation

| Does the dataset have metadata? | Requirements \-\>General Metadata Requirements \-\>Per-Pixel Metadata |
| :---- | :---- |
| Is the dataset metadata standardized? | by CEOS ARD |
| Is the dataset metadata machine-readable? | Requirements \-\>General Metadata 1.2 Metadata Machine Readability |
| Does it include details on the spatial and temporal extent? | Requirements \-\>General Metadata 1.3 Data Collection Time The data collection time is identified in the metadata, expressed in date/time, to the second, with the time offset from UTC unambiguously identified. 1.4 Geographical Area The surface location to which the data relates is identified, typically as a series of four corner points, expressed in an accepted coordinate reference system (e.g., WGS84). |
| Is there a comprehensive data dictionary/codebook to describe parameters? | I can't find this requirement in CEOS ARD. But there is the requirement for Traceability and it includes DOI/LP. It will be described information about data. |
| Is the data dictionary standardized? | I can't find this requirement in CEOS ARD, and I don't know the standard for DOI/LP. |
| Is the data dictionary machine-readable? | I can't find this requirement in CEOS ARD, and I don't know the machine readable standard. |
| Do the parameters follow a defined standard? | I can't find this requirement in CEOS ARD. |
| Are parameters crosswalked in an ontology or common vocabulary (e.g. NIEM)? | I can't find this requirement in CEOS ARD. |
| Does the dataset have a unique persistent identifier,e.g. DOI? | Requirements \-\>General Metadata 1.1 Traceability |
| Is there contact information for subject-matter experts? | I couldn't find this requirement at CEOS ARD, but CEOS ARD defines about Metadata such like ISO-19115 and it includes point of contact. |
| Is there a mechanism for user feedback and suggestions? | I can't find this requirement in CEOS ARD. |
| Are there example codes / notebooks / toolkits available showing how the data can be used? | I can't find this requirement in CEOS ARD. |
| Is there a clear data license? | I can't find this requirement in CEOS ARD. |
| Is the license standardized and machine-readable (e.g. Creative Commons)? | I can't find this requirement in CEOS ARD. |
| Has this dataset already been used in AI or ML activities? Link to publications / reports. | I can't find this requirement in CEOS ARD. |
| Are there recommendations on the intended use of the data, and uses that are not recommended? | I can't find this requirement in CEOS ARD. |

### Data Access

| What is the file format? | I couldn't find this requirement at CEOS ARD, but data provider might show related information to support users can estimate. |
| :---- | :---- |
| Is it machine-readable? | Requirements \-\>General Metadata 1.16 Data Access Information on data access should be available in the metadata as a single DOI landing page. Note 1: Manual and offline interaction action (e.g., login) may be required. |
| Is it available in at least one open, non-proprietary format? | ALL of the CEOS ARD may be the open, non-proprietary format such like geotiff, hdf5 [https://ceos.org/ard/](https://ceos.org/ard/) |
| Is it available in several different file formats? | I can't find this requirement in CEOS ARD. |
| Data delivery: | Requirements \-\>General Metadata 1.16 Data Access Information on data access should be available in the metadata as a single DOI landing page. Note 1: Manual and offline interaction action (e.g., login) may be required. |
| Direct file download or ordering? | Requirements \-\>General Metadata 1.16 Data Access Information on data access should be available in the metadata as a single DOI landing page. Note 1: Manual and offline interaction action (e.g., login) may be required. |
| Is there an API? | I can't find this requirement in CEOS ARD. |
| Custom-developed or open, standard protocol? | I can't find this requirement in CEOS ARD. |
| For restricted data, have measures been taken to provide some access while still applying appropriate protection for privacy and security? | I can't find this requirement in CEOS ARD. |
| Has the data been aggregated to reduce granularity? | I can't find this requirement in CEOS ARD. |
| Has the data been anonymized / de-identified? | I can't find this requirement in CEOS ARD. |
| Is there secure access to the full dataset for authorized users? | I can't find this requirement in CEOS ARD. |
