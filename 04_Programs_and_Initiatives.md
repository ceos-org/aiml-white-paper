[Previous](/research-trend-in-ai4eo/aiml-tasks-and-use-cases.md) | [Table of contents](/README.md) | [Next](ceos-seo.md)

***
- [**4\. Programs and Initiatives**](#4.0)
  - [4.1. CEOS EO-GPT & CEOS-GPT)](#4.1)
  - [4.2. GEO](#4.2)
  - [4.3. NASA (ESDIS, IMPACT)](#4.3)
  - [4.4. NOAA/NCAI](#4.4)
  - [4.5. Indian Space Research Organization (ISRO)](#4.5)
  - [4.6. European Space Agency φ-lab](#4.6)
  - [4.7. UKSA Initiative in AI and ML for Earth Observation](#4.7)
    
***

# 4\. Programs and Initiatives<a id='4.0'></a> 

The global space agencies that make up CEOS have launched several AI initiatives and programs. This section provides an overview of those efforts.
    
***

## 4.1. CEOS SEO<a id='4.1'></a> 

**Overview**

The CEOS Systems Engineering Office provide leadership and support to CEOS through management and technical services, as well as by developing tools and methods that deliver societal benefit. The SEO also drives innovation and thought leadership in the area of AI/ML applied to the use of Earth Observation (EO) data.

**AI4EO Examples**

The CEOS Systems Engineering Office is pursuing two early-stage research projects which serve as frameworks for experimenting with modern Large Language Model (LLM/AI) research and tooling: EO-GPT and CEOS-GPT. 

1. EO-GPT is a Natural language processing (NLP) interface for processing EO data and answering Earth Observation questions. EO-GPT provides a chat interface for the Earth sciences and remote sensing applications domain. It is an LLM augmented interactive analysis framework. Earth observation analysis is modular by nature. The goal of EOGPT is to create a framework that orchestrates custom analysis flexibly using large language models as the orchestration mechanism. EO-GPT features:  
* A module-based system whereby earth-observation algorithms run as microservices. Modules have natural language outputs (to aid in live execution/parameterization).  
* A large language model orchestrates the execution of these modules.  
* An LLM parameterizes the use of modules based on initial conditions/queries, but also utilizes information given from modules for live parameterization of processing steps.  
* Offers a chat visualization of geospatial assets and content.  
2. CEOS-GPT is an interface to all the information available on the CEOS website (http://www.ceos.org/). CEOS GPT provides a question and answering chatbot that operates on the large volume of CEOS data, with the vision of addressing a wide range of topics including training and meeting information, organizational questions, policy questions, and data availability. CEOS-GPT features:  
* CEOS website and private documents are indexed in a retrieval augmented generative (RAG) system.  
* Mixture of agents architecture with each agent responsible for retrieving some type of information from an index.  
* Private models exist for generating document embeddings and a GPT system exists for synthesizing text.  
* Can ask questions about CEOS through an interactive chat-interface.  
* Improvements are regularly benchmarked and evaluated. Improvements are either heuristic improvements to RAG, or improvements of the core large language models (i.e., fine-tuning embedders or the GPT language model).


The following two approaches are explored for constructing generative systems: (a) AI heuristic-driven, and (b) machine learning-driven. Both approaches improve the quality of the generative system and take a substantial amount of research and experimentation. In the heuristic-driven approach, LLMs are treated as abstracted black boxes. Heuristic structures index and organize the data leveraging the LLMs as tools to aid in search index building, information retrieval and response synthesis. Systems that utilize heuristics would use algorithmic structures built on a large language model. These systems do not aim to modify or optimize an underlying machine learning model, they just utilize them as building blocks for a larger system. The machine learning approach on the other hand, focuses on innovations in the underlying architectures of the models themselves rather than the generative system that's built on them. The machine learning approach would also encompass setting up the feedback mechanism whereby a model can be fine-tuned to user queries.

The CEOS SEO plans to further develop  these early-stage research applications and ultimately release them as tools for the CEOS community.

^Back to the top(#4.0)
***

## 4.2. GEO<a id='4.2'></a> 

**Overview**

[The Group on Earth Observations (GEO)](https://earthobservations.org/index.php) is an intergovernmental partnership that connects governments, academia, organizations, civil society, and the private sector to tackle global challenges through innovative solutions that harness the power of [Earth Intelligence](https://earthobservations.org/resources/what-is-earth-intelligence). Among its founding Participating Organizations is CEOS, whose member space agencies provide critical EO satellite data that drive GEO’s activities worldwide.

One of the five goals of the [GEO Post-2025 Strategy](https://earthobservations.org/resources#AJbe25j1Vo) is to integrate EO, models, and innovative new technologies, including artificial intelligence and machine learning, into the design of services that provide Earth intelligence. In line with this goal, GEO is advancing the use of AI and ML across its [Work Programme](https://earthobservations.org/our-work/geo-work-programme) to address complex global challenges. Many of these activities demonstrate how combining AI/ML techniques with EO data from CEOS agencies can deliver practical, high-impact solutions.

**AI4EO Examples**

To accelerate these developments, GEO Work Programme includes a dedicated Enabling  Mechanism—[AI for Earth Observations (AI4EO)](https://earthobservations.org/groups/artificial-intelligence-for-earth-observations). This  builds a network of AI experts across the GEO community, with scope that includes:  advancing AI applications within the GEO Work Programme, fostering cross-disciplinary collaboration and addressing ethical considerations associated with AI in EO.

The following examples illustrate GEO Work Programme activities that apply AI/ML in combination with EO satellite data provided by CEOS agencies.

**1\. GEO Global Agricultural Monitoring (GEOGLAM) Flagship:**  
GEOGLAM applies AI based methods to integrate EO with in-situ data for near-real-time monitoring of global croplands. Its consensus-based Crop Monitors combine optical and radar time series with ground observations to assess crop condition and drought stress, and to forecast yields. These approaches are implemented both at global and national scales. Examples include the cases in the least developing countries, such as Togo, Uganda and Tanzania as highlighted in boxes J (p.32), H (p. 28\) and D (p.22) in [GEO Supplement to the UNFCCC NAP Technical Guidelines](https://earthobservations.org/documents/cc_wg/GEO_NAP_Supplement_final.pdf). GEOGLAM activities are supported by major space agencies, including NASA, JAXA, ESA and the European Commission, which contribute to the development of AI based crop classification, yield modelling, and EO-based agricultural indicators.  
   
**2\. GEO Global Water Sustainability (GEOGLOWS)** **Flagship:**  
GEOGLOWS offers a worldwide open-sourced web-based tool that provides daily 15-day forecasts and an 85-year historical simulation for every river of the world. The GEOGLOWS v2 river “hydrofabric” is based on the 12-m TanDEM-X DEM from the German Aerospace Center (DLR)**,** used by the U.S. NGA to create TDX-Hydro, a global streams and catchments dataset delineated with TauDEM and refined through conditioning. From this, GEOGLOWS derived a network of about 7 million river segments across 125 watershed clusters. Since the quality and availability of in-situ data are not the same across the globe, GEOGLOWS uses AI/ML to capture similarities in hydrological behaviors in different regions around the world to develop bias correction for global forecasts. Methodologies for bias correction of discharge developed with in-situ data are being investigated to extend to satellite altimetry (water elevation) data. A complete list of publications on GEOGLOWS methodologies, including the bias correction efforts, can be found at the [GEOGLOWS training and information site](https://training.geoglows.org/rfs/publications/.). GEOGLOWS work using AI/ML for developing countries such as Malawi has been presented at major conferences, including COP27 and 28 and the AI for Good Global Summit. 

**3\. Data Integration and Analysis System (DIAS) Enabling Mechanism:**  
DIAS is a data platform which integrates a variety of different data such as satellite and in-situ observations and models, to be analyzed for different application purposes such as forecasting/early warning, real-time monitoring and hindcast for health, biodiversity, flood and drought. In particular, EO satellite observation data includes JAXA's GSMaP. On the DIAS platform, AI/ML/Deep learning has been used to execute models. For example, [applying climate prediction data, DIAS uses deep learning for malaria infection prediction and early warning in the Limpopo province in South Africa](https://diasjp.net/wpr/wp-content/uploads/2022/04/dias_leaflet_malaria.pdf). AI/ML-based Malaria Transmission Prediction model integrates the climate forecast data with the weather forecast data and malaria patient count data from local municipalities and medical institutions. It enables the local health authority to predict malaria transmission for 3-4 months ahead. The resulting information has been distributed to the medical institutions and the public via a Malaria Forecast App for early warning since 2016\. Separately, DIAS implemented a UNESCO project called WADiRe-Africa on flood early warning in 11 West African countries: Benin, Burkina Faso, Cameroon, Chad, Côte d’Ivoire, Ghana, Guinea, Mali, Niger, Nigeria and Togo. This was [listed by UNESCO as its example on the use of AI for DRR in Africa](https://www.unesco.org/en/articles/use-artificial-intelligence-disaster-risk-reduction-africa) and was [presented at ITU\&WMO/UNEP workshop on AI for Natural Disaster Management](https://www.itu.int/en/ITU-T/Workshops-and-Seminars/2021/0623/Documents/Shamila%20Nair-Bedouelle_ITU%20WMO%20UNEP%20Workshop%20powerpoint%20for%20ADG.pdf?csf=1&e=3CQ8Oy) (see p.11). DIAS integrates data that are available, including those provided by CEOS agencies.  
   
**4\. GEO Human Planet Initiative (HPI) :**  
GEO Work Programme activity, HPI, generates global data on populations (growth) and settlements (including urban extent, critical infrastructure) to assess human exposure (people and infrastructure in hazard-prone areas) to the disasters but also increasingly vulnerability (economic values/relative deprivation). AI is used to extract info on built environment from satellite imagery. More specifically, multi-decadal satellite archived imagery collections are processed by algorithms using the latest AI techniques, making sure that the results are consistent across time and space globally. As a second step, multiple data sources are combined together using AI/ML methods to estimate population characteristics across time and space. Examples of such products are [the Global Human Settlement Layer (GHSL)](https://ghsl.jrc.ec.europa.eu/about.php) (with relevant papers such as [this](https://urldefense.com/v3/__https:/www.mdpi.com/2072-4292/8/5/399/html__;!!DOxrgLBm!Aqb0fanHlJFi5Q4isXnWqVLueV-YejTRF7Qt-xZL0fu4OH340--e3t04ItKQgBq4bMdQZ7GjVEbofD0YOMMY_upb$)) and [the High Resolution Settlement Layer (HRSL)](https://urldefense.com/v3/__https:/dataforgood.facebook.com/dfg/docs/methodology-high-resolution-population-density-maps__;!!DOxrgLBm!Fq9WPMxJzUCdYTbyf8DxoeoEdSKOgL4TTt-Jg2jbrD46lrPYcUEFMpDm8EVzil3ubHW1ho8sqqoCtSse5Z7O7qd8$) (in collaboration with facebook/Meta and its Data for Good). HPI provides these global products, which can be downscaled for national/local use.   
   
**5\. Euro GEO (Regional GEO acitivity):**  
[Euro GEO](https://www.eurogeosec.eu/)’s Group for Health, coordinated by BEYOND Centre of Earth Observation Research & Satellite Remote Sensing NOA is harnessing AI technology to prevent vector borne disease in Europe. The success story of system [EYWA (Early Warning for Epidemics)](http://www.beyond-eocenter.eu/index.php/web-services/eywa) (1st HE EIC prize on Epidemics) uses EO data to generate analysis-ready products and indicators that inform the dynamic environmental, ecosystem, meteorological, climatological, and geomorphological conditions at the time and place mosquito collections and human cases of Mosquito-Borne Diseases (MBDs) have been recorded over the years. The computer representations of the Earth are used as input to AI and mathematical models that associate climate and environmental data with the corresponding MBDs cases. The models perform continuous operational predictions for generating entomological and epidemiological risks, which are then used to guide vector control actions, such as larviciding/adulticiding and trap placement, as well as door-to-door awareness raising campaigns deployed by the relevant health authorities. Starting in 2020, the EYWA system provided the first operational predictions in four regions in Greece and one region in Italy. In 2021 the system expanded to include 11 regions in five countries (France, Germany, Greece, Italy, and Serbia), addressing the West Nile Virus and other Mosquito Diseases infection in humans and three genera of mosquitoes, supporting a total of 10,909 municipalities and over 34 million residents. With the support of the [e-shape](https://e-shape.eu/). EuroGEO action and third party Institutions as Bill and Melinda Gates Foundation, and Pharmaceutical Industry – TAKEDA, the EYWA system has expanded its operations in Sub-Sahara countries including Cote d’ Ivoire and Cameroun, as well as in Americas (Argentina). This story is included in the [WMO 2023 State of Climate Services Report Health](https://wmo.int/publication-series/2023-state-of-climate-services-health).  
   
**6\. Global Heat Resilience Service (GHRS) :**  
The [Global Heat Resilience Service (GHRS)](https://earthobservations.org/groups/global-heat-resilience-service) is a collaborative initiative led by the GEO and C40 Cities, with support from the World Meteorological Organization and other partners, that responds to the UN's call for action on extreme heat by providing city leaders with neighborhood-level heat risk insights through high-resolution heat maps and climate projections for 2030 and 2050\. A decision-support tool is currently being developed by IBM-C40 with support from GEO and the Gobal Covernant of Mayors and tested in cities including São Paulo, Rio de Janeiro, Salvador, Belo Horizonte, Caceres, Coxim in Brazil, Bangalore, and Freetown, the digital decision-support tool leverages AI in three key ways:   
The tool will leverage AI in three ways:

1. **downscaling** global climate data to neighborhood level using foundation models to produce 100-meter resolution heat maps.  
2. **data integration** from satellites, censuses, building specs, and socioeconomic indicators to update vulnerability hotspots.  
3. with **scenario planning** to model different intervention strategies \- identifying the most effective combinations of policy, physical and nature-based solutions to address heat risks city-wide.

The testing phase utilizes [Harmonized Landsat and Sentinel-2](https://hls.gsfc.nasa.gov/) satellite data, with AI models performing the downscaling and temporal interpolation necessary to generate long-term time series of high-resolution land surface temperature data.  
   
**7\. Digital Earth Pacific:**  
[Digital Earth Pacific (DE Pacific)](https://digitalearthpacific.org/) is a collaborative programme of the Pacific Community (SPC) and Pacific Island countries and territories focused on ensuring accessible use of Earth observations in the Pacific region by leveraging Analysis Ready Data (ARD) and datacube plus over 30 years of open satellite data (Landsat, Sentinel). DE Pacific supports climate resilience, food security, ecosystems monitoring, disaster risk reduction (DRR) and early warning activities through its products, i.e. coastline change, mangrove, inland wetness, satellite derived bathymetry. Many of DE Pacific's products are built using AI/ML including for cloud masking in coastline change, near shore satellite derived bathymetry, vegetation height and canopy and land cover land use change products. The programme is now investigating the use of foundational models. 

**8\. Digital Earth Africa**  
[Digital Earth Africa (DE Africa)](https://digitalearthafrica.org/en_za/) is an African program that provides access to and capacity development in EO technology for the African continent, with the aim of enhancing the application and uptake of EO in African countries. DE Africa supports climate action in particular through data and analytics addressing food and water security, nature based solutions, ecosystem management, land degradation and coastline change. ARD, such as annual surface reflectance geomedian images derived from Landsat and Sentinel missions, are provided to users alongside examples and guidance on how to incorporate them into ML workflows, such as land use classification, while a selection of DE Africa’s Continental Services (continental scale thematic products) are derived from ML applied to ARD. For example, the DE Africa Cropland Extent map was produced with ML applied to [Sentinel-2 GeoMADs](https://digitalearthafrica.org/en_za/geomad/) as input data. In this way, ARD provided by DE Africa can also be considered as ML-ready. Digital Earth Africa therefore produces and supports user creation of end-to-end ML workflows based on satellite-derived EO data.

***
## 4.3. NASA<a id='4.3'></a> 

**Overview**

National Aeronautics and Space Administration’s Earth Science Division has multiple organisations advancing AI/ML, each contributing to five overarching goals described in  Figure 4.3-1. Division-level strategies guide investments to maximise impact and avoid duplication of effort.  

![NASA Earth Science Division AI focus areas](/figures/Figure4.3-1.png)  
Figure 4.3-1. NASA Earth Science Division AI focus areas

NASA’s [High-End Computing (HEC) program](https://hec.nasa.gov/) has made investments in AI-specific platforms. These platforms include HPC and cloud assets with the latest hardware accelerators and AI specific processors and libraries. The Research & Analysis program supports targeted AI activities, some of which have been realized  through competitive solicitations. Currently, most of their focus has been around modeling and assimilation. 

EOSDIS houses over 100 Petabytes of earth science data in the cloud and is working on ways to make that data easily available to ML practitioners in an Analysis-Ready, Cloud-optimized (ARCO) manner. Improving cloud-based earth science data’s interoperability with ML managed services from major cloud providers is also a high priority for EOSDIS.

These goals address the entire data lifecycle process, including collaborations and building AI capacity and expertise within the program. The data systems program has a number of activities related to AI aligning with NASA’s strategic goals – that includes;

* competitive program and partnership activities  
* augmenting data stewardship tasks such as search and discovery  
* maximizing the use of data. 

ESDS also fosters AI/ML research through NASA's Advancing Collaborative Connections for Earth System Science ([ACCESS](https://www.earthdata.nasa.gov/esds/competitive-programs/access)) program. This competitive program develops and implements technologies to effectively manage, discover, and utilize NASA's archive of Earth observations for scientific research and applications in support of NASA Earth science research goals. The following are the most recent ACCESS projects utilizing AI:

### 4.3.1. Advancing an Open-Access Repository for Earth Observation Training Data and Machine Learning Models

| Name | Landcovernet |
| :---- | :---- |
| **Problem Statement** | Provide a multi-mission global land cover training dataset Develop an Open API for registering and retrieving ML models |
| **Project Scope** | Global spatial coverage Cloud-optimized Geotiff |
| **Data Governance and Compliance** |  |
| **Version Control** | https://mlhub.earth/data/ref\_landcovernet\_af\_v1 Current version 1.0 |
| **Input data provenance** | Sentinel-1 ground range distance (GRD) with radiometric calibration and orthorectification at 10m spatial resolution Sentinel-2 surface reflectance product (L2A) at 10m spatial resolution Landsat-8 surface reflectance product from Collection 2 Level-2 |
| **Required infrastructure** |  |
| **Dependencies** |  |
| **Key performance metrics** |  |
| **Security and Privacy** |  |
| **Documentation** | https://mlhub.earth/docs |

**AI4EO Examples**

Recent ACCESS projects highlight how NASA is applying AI/ML to Earth observation data systems:

* [Developing Passive Satellite Cloud Remote Sensing Algorithms Using Collocated Observations, Numerical Simulation and Deep Learning](https://www.earthdata.nasa.gov/esds/competitive-programs/access/ml-cloud-properties)  
* [GeoWeaver: Building An Open-Source Platform for Enabling Ad Hoc Management, Open Sharing, and Robust Reuse of NASA Earth Data-Driven Hybrid AI Workflows](https://www.earthdata.nasa.gov/esds/competitive-programs/access/geoweaver)  
* [Machine Learning Datasets for the Earth's Natural Microwave Emission](https://www.earthdata.nasa.gov/esds/competitive-programs/access/microwave-emission)  
* [Machine Learning Planet High Resolution Training Data for Medium Resolution Land Cover and Disturbance Mapping](https://www.earthdata.nasa.gov/esds/competitive-programs/access/ml-planet-data)  
* [Pangeo ML: Open Source Tools and Pipelines for Scalable Machine Learning Using NASA Earth Observation Data](https://www.earthdata.nasa.gov/esds/competitive-programs/access/pangeo-ml)  
* [Spatio-Temporal Machine Learning and Cloud Computing for Predicting Dynamics of Global Vegetation Structure from Active Satellite Sensors](https://www.earthdata.nasa.gov/esds/competitive-programs/access/ml-vegetation-structure)  
* [Training Data for Streamflow Estimation](https://www.earthdata.nasa.gov/esds/competitive-programs/access/streamflow-estimation)

***
## 4.4. NOAA<a id='4.4'></a> 

**Overview**

**National Oceanic and Atmospheric Administration** has a long history using AI/ML to support its mission areas, such as deep-sea exploration, habitat characterization, fishery species assessments, environmental modeling, and interpretation of Earth observation data. In 2021, NOAA released its first AI Strategy with five goals:

1. Establish an efficient organizational structure and processes to advance AI across NOAA.  
2. Advance AI research and innovation in support of NOAA’s mission.  
3. Accelerate the transition of AI research to applications.   
4. Strengthen and expand AI partnerships.   
5. Promote AI proficiency in the workforce.   

To achieve these goals, NOAA created a five-year strategic plan with a more coordinated approach across NOAA to embrace AI in support of NOAA’s mission areas through effectively developing the AI-ready data and tools for reliable and efficient processing, interpretation, and utilization of Earth observations.

**AI4EO examples**

Working with scientific fields and offices, NOAA has established the NOAA Center for Artificial Intelligence ([NCAI](https://www.noaa.gov/ai)) to support new and ongoing projects and to propel innovative uses of responsible AI technology to support environmental equity, knowledge, and study.

Since its inception, NCAI has been focused on developing a focal point for NOAA to facilitate the advancement of AI-ready data and workforce development. NCAI is leading the development of community-driven data standards for AI-ready open environmental data through the collaboration with Earth Science Information Partners. The collaboration produced the first AI-readiness checklist for open environmental data ([https://github.com/esipfed/data-readiness](https://github.com/esipfed/data-readiness)) that are currently being used or plan to be used by NOAA, UK Met Office, World Data Systems, and other geoscience data repositories to conduct assessments of the readiness of environmental data including earth observations for AI development. 

![Four groups of characteristics of AI-ready data defined by the Earth Science Information Partners](/figures/Figure4.3-1.png)  
Figure 4.4-1. Four groups of characteristics of AI-ready data defined by the Earth Science Information Partners (https://github.com/esipfed/data-readiness).

At its current stage, the AI-readiness assessment requires data experts to go through the published checklist manually which is difficult to be scaled to more than 60 PBs of environmental datasets at NOAA. Thus, NOAA is investing in a prototype tool using a natural language processing method to automate the AI-readiness assessment process and recommend improvements to existing NOAA datasets for AI development.

NOAA has invested in the improvement of selected datasets for AI applications, such as, [Tropical Cyclone PRecipitation, Infrared, Microwave, and Environmental Dataset (TC PRIMED)](https://rammb-data.cira.colostate.edu/tcprimed/), [NOAA Climate Data Records,](https://www.ncei.noaa.gov/products/climate-data-records) and [water column sonar data](https://www.ncei.noaa.gov/products/water-column-sonar-data). 

Additionally, NOAA is actively seeking public-private partnership to enhance the usability of earth observation data for high-impact AI applications including AI for numerical weather prediction. One specific example is the collaboration between the NOAA Physical Sciences Laboratory and Brigntband to transform the archive of a diverse set of quality-controlled satellite observations to cloud-native data format to support data assimilation (https://techpartnerships.noaa.gov/tpo\_partnership/making-observation-data-ai-ready/). The resulting dataset – NOAA-NASA Joint Archive AI-ready data (NNJA-AI) – is made publicly available via the NOAA Open Data Dissemination program on Google Cloud.


***

## 4.5. ISRO<a id='4.5'></a> 

**Overview**

The Indian Space Research Organisation (ISRO) has increasingly incorporated AI/ML in various facets of Earth observation data processing, marking a transformative shift in data processing technology. AI is playing a pivotal role in automating and enhancing the efficiency of data analysis, enabling ISRO to glean valuable insights from the vast amounts of information gathered by Earth observation satellites. 

**AI4EO Examples**

ISRO’s work in the field of AI can be categorized in three broad domains \- data acquisition related processing, data processing/fusion/augmentation and information extraction. Some key representative tasks in each category, that are being addressed through the use of AI, are shown in Figure 4.5-1. Machine learning algorithms, particularly deep learning models, are being utilized to surpass the classical approaches in each of these domains to improve the overall impact of the Earth observation data collected and processed at ISRO.  

![Broad categorisation of AI/ML related projects at ISRO](/figures/Figure4.5-1.png)  
Figure 4.5-1. Broad categorisation of AI/ML related projects at ISRO.

In the data acquisition related AI processing, the emphasis is on improving the quality of the data which is obtained from various spaceborne/airborne sensors.  Various models developed in this area include data reconstruction, image restoration, thermal resolution improvement as well as models related to compression/decompression of the high-resolution data. 

The second category is for the data processing and augmentation research projects that are focusing on using data from multiple-sources (multimodal, multi-temporal or multi-sensor) to generate enhanced value products through the use of AI. This includes tasks such as spatial or spectral super-resolution, data fusion, image-to-image translation and generation of various types of AI-ready data for downstream tasks. 

The final category of AI related tasks is the information extraction category. The primary objective here is to derive information such as resource maps, land-use land cover classification, specific object detection, content aware image search, as well as onboard intelligence applications. Some of the methods are targeting the time-series and change detection applications. Many models have been built in this category, e.g. cloud-detection, forest-fire detection, solar rooftop potential estimation, building footprint extraction, etc. 

The work related to this aspect is integrated via research and development related to core topics in AI such as development of new models for specific applications, adaptation of cutting edge research for specific use cases, implementation of infrastructure for supporting development and deployment of AI applications, and core AI research such as explainable AI. Work is also being done to integrate and harness the potential of vast amounts of data available from ISRO’s fleet of remote sensing sensors. 

ISRO is also working towards a common framework, where the work related to AI that is taking place across different teams and projects can be synergized. In this direction, some standards have been studied and are planned to be implemented in near future. Some of these models are now being integrated into publicly available web-platforms.

***
## 4.6. European Space Agency φ-lab<a id='4.6'></a> 

**Overview**   
The ESA Φ-lab is the ESA Earth Observation innovation laboratory that aims to accelerate the future of Earth Observation (EO) via transformative innovation and commercialisation actions, thereby strengthening Europe’s global competitiveness. Artificial Intelligence (AI) is a core focus areas for the ESA Φ-lab, as it offers unprecedented capabilities to extract actionable insights from vast amounts of EO data,  enabling novel applications and business models. The ESA Φ-lab covers the whole spectrum of AI development, from ideation to generating tangible impacts in science, technology, or commercial field through its two offices: the **Explore Office** and the **Invest Office**. Additionally, the ESA Φ-lab also engages  at different levels with the development of about 20 satellites, ranging from technology demonstrators to operational or commercial missions, the vast majority of which are AI-powered as shown in the image below.

![Figure4.6-1](/figures/Figure4.6-1.png)  

The [Explore Office](https://philab.esa.int/explore/) conducts R\&D activities on AI for EO by using a *user-driven* approach in exploring the technology from ideation to proof of concept. The office explore technologies and transformative ideas, prove their benefits, builds capacities from validated ideas and finally prepare the impact and uptake by end user. The office also spend a significant effort in growing a large community around Φ-lab. In doing this, the Explore Office mainly works on 3 technological pillars:

1. Innovative computing paradigms  
2. Trustable Augmented Intelligence  
3. ICT revolution

![Figure4.6-2](/figures/Figure4.6-2.png)  

The [Invest Office](https://philab.esa.int/invest/) promotes commercial initiatives through the [InCubed](https://incubed.esa.int/) (Investing in Industrial Innovation) program. InCubed is a Public Private Partnership co-funding program run by the ESA Φ-lab Invest Office, focusing on developing innovative and commercially viable products and services that exploit the value of EO imagery and datasets. The program's broad scope supports everything from building satellites to developing new EO business models. Today, the majority of proposals for downstream activities are AI-related and focus on agriculture, forestry, emergency response, insurance, maritime, carbon monitoring, and asset management and identification. Instead, for upstream activities, it is trendy to bring AI-processing capabilities at-the-edge to address the data downlink bottleneck and reduce data latency for value maximisation. The InCubed programme size is about 225m€ and has 140 activities in the pipeline with about 10 satellite constellations under development.

**AI4EO Examples** 

R\&D activities conducted by the Φ-lab Explore focus on key AI-related technologies and explore their potential for various EO use cases. In particular, the main topics of interest involve:

* *Innovative computing paradigms:* the Φ-lab Explore Office combines AI-related research to the investigation of alternative computing paradigms that could further enhance benefits introduced by AI for specific use cases. Alternative computing paradigms involve:  
  * **Edge Computing:** when moved on board EO satellites, AI could enable the detection of actionable information that could significantly reduce the latency for EO use cases having near-real-time requirements (e.g., civil security applications, operational services for natural disasters management). In addition, it could enable novel acquisition systems. \[[143](/reference.md#ref.143), [144](/reference.md#ref.144)\]. Onboard AI is a central element in the scope of [Φ-Sat-1](https://www.esa.int/Applications/Observing_the_Earth/Ph-sat), [Φsat-2](https://www.esa.int/Applications/Observing_the_Earth/Phsat-2/Introducing_Phsat-2) missions, to which the Φ-lab Explore Office has provided a pivotal contribution.  
  * **Neuromorphic computing:** neuromorphic computing is a brain-inspired asynchronous, event-based, and massively parallel computing paradigm. Among various neuromorphic computing techniques, spiking neural networks have attracted the interest of researchers for their potential energy efficiency, which makes it promising for onboard satellite implementations.  
  * **Quantum Machine Learning:** when combined with quantum computing algorithms, ML could further enhance its capability to process intricate data structures and very large volumes of data. The Φ-lab Explore Office is investigating the potential of quantum and hybrid implementations of ML algorithms for EO use cases\[[145](/reference.md#ref.145)\]  
* *Trustable Augmented Intelligence:* this topic investigates numerous AI branches to augment the capabilities to extract actionable and trusthworthy insights from EO data and take informed decisions. The main AI branches under investigation include:  
  * **Explainable AI:** the goal of explainable AI is to provide transparent and/or interpreatable models for various EO use cases.  
  * **Physics-informed Machine Learning:** physics-informed ML incorporates physics principles into the training process with potential advantages in terms of data efficiency, computational intensity, and robustness to noisy data.  
  * **Foundation models:** Given the scarcity of labeled EO data, foundation models—large-scale models trained on extensive datasets—have the potential to surpass specialized application models while requiring significantly fewer labeled examples. A key contribution from the Φ-lab Explore Office is the creation of the [PhilEO Bench](https://arxiv.org/abs/2401.04464), a benchmark designed for rigourous evaluation of foundation models for EO applications. Research on foundation models is often coupled with the investigation of *self-supervised learning*, which aims to train Machine Learning (ML) models in an unsupervised manner.  
  * **Generative AI:** generative AI has various applications in Earth Observation, including spatial resolution of EO data and automatic generation of synthetic images to augment datasets.  
  * **Digital assistant for EO:** Large Language Models could be used to create an assistant to facilitate the processing and the interaction with EO data by using natural language\[[146](/reference.md#ref.146)\].  
* *User-driven* approach: plethora of R\&D activities in AI for EO characterized by an application-centric methodology, which scrutinizes AI's potential for specific, socially impactful use cases, for example:  
  *   
  * **AI for health:** by using ensemble of ML models to process satellite data, it is possible to predict [dengue fever outbreaks](https://philab.esa.int/%CF%86-lab-and-unicef-joint-dengue-fever-research-receives-further-award/).  
  * **AI for Earth Science:** AI is providing a significant contribution to numerous fields of Earth Science. The Φ-lab Explore Office has investigated the potential of AI for weather modelling, solar forecasting, and other related applications.  
  * **AI for Green and sustainable future:** in the face of escalating climate changes, the urgency for efficient forecasting and response systems for natural disasters has never been greater. AI can play a critical role in processing and fusing in-situ with satellite data for high spatial and temporal resolution forecasting of [global storm surges](https://philab.esa.int/global-storm-surge-forecasting-creating-early-warning-models-with-ai4eo/).  
  * **AI for Destination Earth:** [Destination Earth](https://philab.esa.int/flagship-programmes/destination-earth/) (DestinE) is a European Commission initiative to develop an ambitious AI-driven decision-support system based on a very high accurate digital model of the Earth. This system aims to monitor and simulate natural and human activity, along with developing and validating policy scenarios. ESA participates in the initiative by leading the overall effort in collaboration with EUMETSAT and ECMWF. ESA Member States have initiated a companion programme, the ESA Digital Twin Earth (DTE), to foster the exploitation of DestinE data for Earth observation and innovation. Φ-lab actively supports the activities of DestinE and ESA DTE to bring the demonstrated analysis and reasoning capabilities of AI technologies to the heart of the operations, along with stimulating further exploitation by various user communities. DestinE will use unprecedented observation and simulation products, powered by Europe’s HPC computers and AI power, to push the limits of computing, forecasting, planning, and acting.

In pursuit of these goals, Φ-lab Explore Office extensively on activities aiming at community engagement, dissemination and partnership creation with academic and industrial partners, international organizations, and other ESA divisions. To foster research and use of AI for EO use cases, the Φ-lab Explore Office has contributed to the release of: numerous *datasets* (e.g., [WorldStrat](https://worldstrat.github.io/), [Seeing Beyond the Visible](https://platform.ai4eo.eu/seeing-beyond-the-visible/data), [Major TOM](https://philab.esa.int/hello-major-tom-esa-%CF%86-lab-releases-largest-ml-ready-sentinel-2-dataset-ever-published/), [THRawS](https://zenodo.org/records/7908728), [VSD2Raw](https://zenodo.org/records/7982468), and [DENETHOR](https://openreview.net/pdf?id=uUa4jNMLjrL)) and toolboxes (please consult [ESA-PhiLab GitHub](https://github.com/ESA-PhiLab)).

***
## 4.7. UKSA Initiative in AI and ML for Earth Observation<a id='4.7'></a> 

**Overview**

The UKSA supports thef collaboration and synergy among various organizations and initiatives within the UK's Earth Observation ecosystem. In this regard, the UKSA has established strong partnerships with the UK National Center for Earth Observation (NCEO) and the NERC Earth Observation Data Analysis and AI Service (NEODAAS). 

Artificial Intelligence (AI) is central to the UK Government’s plan to kickstart an era of economic growth, transform public service delivery and boost living standards. The government aims to harness AI to advance its missions and priorities across healthcare, the economy and society. Through the AI Opportunities Action Plan, the UK seeks to build scalable AI sector with global impact, outlining a framework to maximise AI’s benefits across the system. AI  also forms a part of the UK government's development Industrial Strategy, guiding the country’s strategic direction in criticalindustries.

NCEO is a world-leading center of excellence in Earth Observation science and technology, bringing together a network of leading universities and research institutions. The UKSA actively engages with the NCEO to leverage its expertise and capabilities in areas such as satellite data processing, scientific algorithm development, and the application of advanced analytical techniques, including AI and ML. Through joint research projects and technology development initiatives, the UKSA and the NCEO work together to address critical challenges in Earth Observation. This collaboration aims to accelerate the translation of scientific advancements into practical applications and operational services that can benefit society, the economy, and the environment. The UKSA work with NCEO and NEODAAS to develop the UK’s AI and Earth Observation Capacities. NEODAAS hosts the Massive GPU Cluster for Earth Observation (MAGEO) and provides EO Data, AI support and development to UK based researchers working on a range of EO focused domains. This has resulted in numerous successful projects applying advanced ML techniques to EO data.

**AI4EO Examples**

**Key Contributions of UKSA and NCEO**

* Data Processing and Analysis: One of the primary focuses of the UKSA initiative is to improve the processing of EO data. By leveraging AI and ML, NCEO has developed advanced algorithms that can analyze large datasets more quickly and accurately than traditional methods. This is particularly important for time-sensitive applications, such as monitoring natural disasters or tracking climate change impacts.  
* Harmonization and Fusion of Data: The integration of AI and ML has also facilitated the harmonization and fusion of different types of EO data. This means that data from various sources, such as multispectral and hyperspectral sensors, can be combined to provide a more comprehensive view of the Earth's surface. The NCEO has been instrumental in demonstrating how AI can enhance the understanding of land use and land cover (LULC) changes, which is crucial for effective environmental management.  
* Development of Analysis Ready Data (ARD): The initiative has focused on creating Analysis Ready Data (ARD) products that are pre-processed and ready for analysis. For instance, the Sentinel-2 satellite data undergoes atmospheric correction using the Sen2Cor algorithm, which is a proprietary method that ensures the data is suitable for further analysis. This preprocessing step is vital for ensuring the accuracy of AI and ML applications in Earth observation.  
* Applications in Agriculture: AI and ML applications in agriculture have been a significant area of focus. The NCEO has worked on projects that utilize satellite data to monitor crop health, predict yields, and assess the impact of climate variability on agricultural practices. By employing AI techniques, the NCEO can provide farmers and policymakers with actionable insights that can lead to better decision-making and resource management.  
* Super-resolution Techniques: Another innovative approach being explored is the use of super-resolution techniques to enhance the spatial resolution of satellite images. This is particularly beneficial for applications that require detailed imagery, such as urban planning and environmental monitoring. The NCEO is investigating how AI can be used to improve the quality of satellite images, making them more useful for various applications.

**JASMIN support for AI: ORCHID**

The JASMIN platform, managed by the STFC Centre for Environmental Data Analysis (CEDA), has traditionally supported a diverse range of environmental science users, including EO and climate archives alongside large-scale batch computing clusters, a JupyterHub service and private cloud infrastructure. JASMIN now includes a GPU cluster, known as ORCHID, which is tailored towards the needs of AI and ML workflows. A range of different scientific use cases are managed on ORCHID, and additional resources are being tapped to expand the AI-on-JASMIN community.

**NEODAAS AI Service**

The NERC Earth Observation Data Analysis and AI service is funded by NERC, through NCEO to support national EO and AI services. They provide a range of support services, and work with JASMIN to develop their GPU and JupyterHub fasciitis to best support users, and individually support users through AI expertise, training and support, and method implementations. This facility has enabled the acceleration of uptake of AI within the EO community within the UK, by combining EO domain experts and AI domain experts, within the NCEO structure.There are a range of scientific use cases which demonstrate the benefits of this approach through interdisciplinary collaboration.

**Future Directions**  
The collaboration between UKSA and NCEO is set to expand further, with ongoing research into new AI and ML methodologies that can enhance Earth observation capabilities. The focus will likely include:

* Increased Accessibility of Data: Efforts to make Earth observation data more accessible to researchers, policymakers, and the public will continue. This includes developing user-friendly platforms that allow for easy access and analysis of satellite data.  
* Interdisciplinary Research: The initiative will promote interdisciplinary research that combines Earth observation with other fields, such as social sciences and economics, to address complex global challenges like climate change and food security.  
* Capacity Building: Training and capacity building will be essential to ensure that stakeholders can effectively utilize AI and ML tools in their work. This includes workshops, online courses, and collaborative projects that foster knowledge sharing.  
* Interoperability and Platform Integration: With the new Isambard-AI supercomputer coming online soon, NEODASS and CEDA will reach out to the University of Bristol to optimize the integration between their AI analysis platforms.

In conclusion, the UKSA initiative, in collaboration with NCEO, is making significant strides in utilizing AI and ML for Earth observation. Through innovative data processing, harmonization, and application development, they are enhancing our understanding of the Earth and its systems, ultimately contributing to better environmental management and policy-making.

***
## 4.8. GISTDA<a id='4.8'></a> 

The Geo-Informatics and Space Technology Development Agency (GISTDA) is utilizing AI/ML across various fields in Thailand’s Earth observation ecosystem and geospatial intelligence missions. GISTDA’s long-term vision is to leverage AI/ML for space data analysis through the evidence-based Geointelligence LLM platform, in order to support effective decision-making, promote sustainable development, and provide insights to inform national policymaking. Recognizing the importance of AI/ML technology, a five-year AI/ML development roadmap has currently been drafted for GISTDA’s key missions, emphasizing resilience, innovation, and responsiveness to societal needs, as shown in the image below.

![A five-year AI/ML development roadmap established by GISTDA](/figures/Figure4.8-1.png)  
Figure 4.8-1. A five-year AI/ML development roadmap established by GISTDA.

**AI4EO Examples**

**AI for Air Quality and Well-being**  
To support public health awareness and helps citizens make informed decisions to prepare for or respond to pollution, GISTDA developed [Check Phoon](https://pm25.gistda.or.th/), a mobile and web-based application for monitoring PM2.5 at sub-district level resolution. The system integrates in-situ measurements from Thailand’s Pollution Control Department (PCD) with meteorological and satellite data, and applying ML for forecasting 3-hour air quality predictions and accuracy reports.

![Example workflow for the development of GISTDA’s PM2.5 monitoring application](/figures/Figure4.8-1.png)  
Figure 4.8-2. Example workflow for the development of GISTDA’s PM2.5 monitoring application.

**AI for Disaster Risk Reduction**  
Thailand is one of the countries that experience a lot of disaster due to the signature of South East Asia’s climate. To support both local authorities and regional cooperation, GISTDA operates the [Disaster Monitoring and Decision Support Platform](https://disaster.gistda.or.th/landing), This platform integrating flood, wildfire, and drought models at sub-district level resolution. The three models are under development to incorporate AI-driven flood risk forecasting, wildfire spreading prediction, and drought risk analysis.

Figure 4.8-3. Example workflow for the development of GISTDA’s flood monitoring and decision-support application.

**AI for Image Quality and Enhancement**  
Collaborating with Nara Space, GISTDA applies AI-based Super-Resolution technique to THEOS-2 imagery to enhances spatial resolution from 0.5 m to 0.25 m. This processing addresses information gaps by training unpaired datasets across different satellites. This work expands the usability of very-high-resolution imagery for applications such as urban planning, agriculture, national security, and also escalate the chances to combining other AI/ML technique to the analysis such as image detection.

**GeoAgentic AI-LLM Prototype for Urban Governance**  
GISTDA and National Electronics and Computer Technology Center (NECTEC)plan to developing a prototype Digital Twin platform that combines AI/LLM with geospatial data to address urban challenges such as the Urban Heat Island effect then provide actionable policy recommendations. This project aims to contribute to Thailand’s preparedness for climate change and sustainable urban development.

**Impact and Future Directions**  
Through these initiatives, GISTDA is strengthening its foundation in AI and ML for Earth observation and geospatial applications. The continued integration of these technologies will enhance Thailand’s capacity in environmental monitoring, disaster resilience, and space technology development. Looking forward, GISTDA aims to expand its AI/ML capabilities through international collaboration and knowledge exchange under CEOS and GEO frameworks. These efforts reflect GISTDA’s commitment to advancing responsible, explainable, and impactful AI applications that contribute to global sustainability and equitable access to Earth observation benefits.

***

[Previous](/research-trend-in-ai4eo/aiml-tasks-and-use-cases.md) | [Table of contents](/README.md) | [Next](ceos-seo.md)
