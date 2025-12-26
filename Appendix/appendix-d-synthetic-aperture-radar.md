## Appendix D. [Synthetic Aperture Radar](https://github.com/ceos-org/ceos-ard/blob/main/Specifications/Synthetic-Aperture-Radar/README.md)

### Data Preparation

| Have null values/gaps been filled? | Requirements \-\>Per-Pixel Metadata 2.2 Data Mask Image Threshold (Minimum) Requirements Mask image indicating: \- Valid data \- Invalid data \- No data File format specifications/ contents provided in metadata: \- Sample Type \[Mask\] \- Data Format \[Raw/GeoTIFF/NetCDF, …\] \- Data Type \[Int, ...\] \- Bits per Sample \- Byte Order \- Bit Value Representation |
| :---- | :---- |
| Have outliers been identified? | I couldn't find the description about range for values in CEOS ARD. |
| Is the data single-source or aggregated from several sources? | Requirements \-\>General Metadata 1.2 Metadata Machine Readability Threshold (Minimum) Requirements Metadata is provided in a structure that enables a computer algorithm to be used consistently and to automatically identify and extract each component part for further use. |
| Has the data been gridded (regularized in space and time) or is it in the originally sampled resolution? | Requirements \-\>General Metadata 1.3 Data Collection Time 1.6 Map Projection 1.7 Geometric Correction Methods 1.8 Geometric Accuracy of the Data Probably, ARD satisfies the requirements by those requirements |
| Have targets been identified and labeled (i.e. can this be used as a training dataset for supervised learning techniques)? | This require comes from AI/ML aspect, so CEOS ARD doesn't include this requirement. |

### Data Quality

| Have measures been taken to ensure completeness? | I couldn't find this requirement at CEOS ARD. |
| :---- | :---- |
| Are there automated processes to monitor consistency? | I couldn't find this requirement at CEOS ARD. |
| Have measures been taken to reduce bias? | This require comes from AI/ML aspect, so CEOS ARD doesn't include this requirement. |
| What is the timeliness of the data? (Near real-time,1 week, 1 month, 1 year, more than 1 year) | I couldn't find this requirement at CEOS ARD, but data provider might show timeliness with dataset. |
| Is there a difference between raw near real-time access vs fully quality-controlled data that has an additional delay? | I couldn't find this requirement at CEOS ARD, but data provider might show timeliness with dataset. |
| Are there quantitative measures of uncertainty? | Requirements \-\>PerPixel Metadata 2.14 InSAR Phase Uncertainty Image (desired) Estimate of uncertainty in InSAR phase is provided, such as finite signal to noise ratio, quantization noise, or DEM error. Identification of which error sources are included will be provided as DOI/URL reference or brief description. It represents statistical variation from known noise sources only. File format specifications/ contents provided in metadata: \- Sample Type \[Angle\] \- Data Format \[Raw/GeoTIFF/NetCDF, …\] \- Data Type \[Float, ...\] \- Bits per Sample \- Byte Order |
| Is there quantitative information about data resolution in space and time? | Requirements \-\>General Metadata 4.3 Geometric Accuracy of the Data. (desired) Accurate geolocation is a prerequisite to radar processing to correct for terrain and to enable interoperability between radar sensors. The absolute geolocation error (ALE) for a sensor is typically assessed through analysis of Single Look Complex (SLC) imagery and measured along the slant range and azimuth directions (case A: SLC ALE). The end-to-end “ARD” ALE of the final CEOS-ARD product could be measured directly in the final image product in the chosen map projection, i.e., in the map coordinate directions: e.g., Northing and Easting (case B: ARD ALE). Providing accuracy estimates based on measurements following at least one scheme (A or B or both) meets the threshold requirement. Estimates of the ALE is provided as a bias and a standard deviation, with (Case A) SLC ALE expressed in slant range and azimuth, and (Case B) ARD ALE expressed in map projection dimensions. Note 1: This assessment is often made through comparison of measured corner reflector positions with their projected location in the imagery. In some cases, other mission calibration/validation results may be used. Note 2: The ALE is not typically assessed for every processed image, but through an ALE assessment by the data processing team characterizing all or (usually a subset) of the generated products. 3.5 Radiometric Accuracy (desired) Uncertainty (e.g., bounds on γ⁰ or σ⁰) information is provided as document referenced as URL or DOI. SI traceability is achieved. |
| Are there published data quality procedures or reports? (Link to reports) | I couldn't find this requirement at CEOS ARD. |
| Is the provenance tracked and documented? | I couldn't find this requirement at CEOS ARD. |
| Are there checksums / other checks for data integrity? | I can't find this requirement in CEOS ARD. |
| How big is the dataset? Depending on the resource, this might be total data volume, dimensionality, number of images, data files, table rows, image size, etc. | I couldn't find this requirement at CEOS ARD, but data provider might show related information to support users can estimate. |
| Is this essentially raw data or a derived/processed data product? | I couldn't find this requirement at CEOS ARD, but data provider might show related information to support users can estimate. |
| Is this observational data or simulation/model output? | ALL of the CEOS ARD may be the observational data. |
| Has the data been peer-reviewed? | Requirements \-\>PerPixel Metadata 2.15 Atmospheric Phase Correction Image 2.16 Ionospheric Phase Correction Image Radiometrically Corrected Measurements 3.3 Noise Removal 3.4 Radiometric Terrain Correction Algorithm Geometric Corrections 4.1 Geometric Correction Algorithm |
| Has it been down-sampled to reduce resolution, or is it raw? If so, are the raw data available? | I couldn't find this requirement at CEOS ARD, but data provider might show related information to support users can estimate. |

### Data Documentation

| Does the dataset have metadata? | Requirements \-\>General Metadata Requirements \-\>Per-Pixel Metadata |
| :---- | :---- |
| Is the dataset metadata standardized? | by CEOS ARD |
| Is the dataset metadata machine-readable? | Requirements \-\>General Metadata 1.2 Metadata Machine Readability |
| Does it include details on the spatial and temporal extent? | Requirements \-\>General Metadata 1.5 Data Collection Time Number of source data acquisitions of the data collection is identified. The start and stop UTC time of data collection is identified in the metadata, expressed in date/time. In case of composite products, the dates/times of the first and last data takes and the per-pixel metadata 2.8 (Acquisition ID Image) is provided with the product. 1.7.8 Product Geographical Extent The geometry of the SAR image footprint expressed in WGS84, in a standardised format (e.g., WKT Polygon). |
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
| Is it machine-readable? | Requirements \-\>General Metadata 1.7.1 Product Data Access Processing parameters details of the CEOS-ARD product: \- Processing facility \- Processing date \- Software version \- Location from where CEOS-ARD product can be retrieved, expressed as a URL or DOI. |
| Is it available in at least one open, non-proprietary format? | ALL of the CEOS ARD may be the open, non-proprietary format such like geotiff, hdf5 [https://ceos.org/ard/](https://ceos.org/ard/) |
| Is it available in several different file formats? | I can't find this requirement in CEOS ARD. |
| Data delivery: | Requirements \-\>General Metadata 1.7.1 Product Data Access Processing parameters details of the CEOS-ARD product: \- Processing facility \- Processing date \- Software version \- Location from where CEOS-ARD product can be retrieved, expressed as a URL or DOI. |
| Direct file download or ordering? | Requirements \-\>General Metadata 1.7.1 Product Data Access Processing parameters details of the CEOS-ARD product: \- Processing facility \- Processing date \- Software version \- Location from where CEOS-ARD product can be retrieved, expressed as a URL or DOI. |
| Is there an API? | I can't find this requirement in CEOS ARD. |
| Custom-developed or open, standard protocol? | I can't find this requirement in CEOS ARD. |
| For restricted data, have measures been taken to provide some access while still applying appropriate protection for privacy and security? | I can't find this requirement in CEOS ARD. |
| Has the data been aggregated to reduce granularity? | I can't find this requirement in CEOS ARD. |
| Has the data been anonymized / de-identified? | I can't find this requirement in CEOS ARD. |
| Is there secure access to the full dataset for authorized users? | I can't find this requirement in CEOS ARD. |
