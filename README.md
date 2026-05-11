[Next](01_Introduction.md)

***
# State of AI4EO CEOS Whitepaper

[Technology Exploration Interest Group of CEOS-WGISS](https://ceos.org/ourwork/workinggroups/wgiss/technology-exploration/)

Doc. Ref.: CEOS/WGISS TEIG(Technology Exploration Interest Group)

## Issue 
Version 1.2 | Date: December 2025

----
## Citation recommendation

If you wish to cite any part of the document, you may use the following:
```
@article{teig2025ai4eo,
  title={State of AI4EO CEOS Whitepaper},
  author={Ikehata, Yousuke and Bayaraa, Maral and Strobl, Peter and Rossi, Cristian and Meoni, Gabriele and Keary, Hayret Abdula and Gupta, Ashutosh and Dube, Nitant and Borges, David and Newman, Douglas and Albayrak, Rustem Arif and Redmon, Rob and Rao, Yuhan Douglas and Moffat, David and Knappett, Diane and McKinstry, Alastair and Demir, Begum and Leith, Alex and Kalaitzis, Freddie and Ramage, Steven and Kotani, Rui and Su, Wenying and Taravat, Alireza and Schumann, Guy and Uriburu Quirno, Marcelo and Rodríguez Suquet, Raquel and Straka, William and Shen, Xinyi and Corey, Rebecca and Odgers, Michelle and Fletcher, Rob and Awty-Carroll, Katie and Sohre, Tom and Makoto, Natsuisaka and Nakata, Kazuki and Yamamoto, Kosuke}, journal={Committee on Earth Observation Satellites (CEOS)},year={2025}}
```
```
Ikehata, Y., Bayaraa, M., Strobl, P., Rossi, C., Meoni, G., Keary, H.A., Gupta, A., Dube, N., Borges, D., Newman, D., Albayrak, R.A., Redmon, R., Rao, Y.D., Moffat, D., Knappett, D., McKinstry, A., Demir, B., Leith, A., Kalaitzis, F., Ramage, S., Kotani, R., Su, W., Taravat, A., Schumann, G., Uriburu Quirno, M., Rodríguez Suquet, R., Straka, W., Shen, X., Corey, R., Odgers, M., Fletcher, R., Awty-Carroll, K., Sohre, T., Makoto, N., Nakata, K. and Yamamoto, K. (2025) State of AI4EO CEOS Whitepaper. Committee on Earth Observation Satellites (CEOS).
```

----
## Table of Contents

- [**1\. Introduction**](01_Introduction.md)
  - [1.1. Preface by the co-chairs](01_Introduction.md)
  - [1.2. TEIG Contributors](https://github.com/ceos-org/aiml-white-paper/blob/main/01_Introduction.md#1.2)
- [**2\. Background**](02_Background.md)
  - [2.1. Overview of Earth Observation](02_Background.md)
  - [2.2. Core ideas in Deep Learning](https://github.com/ceos-org/aiml-white-paper/blob/main/02_Background.md#2.2)
- [**3\. Research trends in AI4EO**](03_Research-trends-in-ai4eo.md)
  - [3.1. Venues of cross-disciplinary research](https://github.com/ceos-org/aiml-white-paper/blob/main/03_Research-trends-in-ai4eo.md#3.1)
  - [3.2. From sensing to applications](https://github.com/ceos-org/aiml-white-paper/blob/main/03_Research-trends-in-ai4eo.md#3.2)
  - [3.3. The future of AI4EO research](https://github.com/ceos-org/aiml-white-paper/blob/main/03_Research-trends-in-ai4eo.md#3.3)
  - [3.4. MLOps Life cycle and tasks](https://github.com/ceos-org/aiml-white-paper/blob/main/03_Research-trends-in-ai4eo.md#3.4)
  - [3.5. AI/ML Tasks and use cases](https://github.com/ceos-org/aiml-white-paper/blob/main/03_Research-trends-in-ai4eo.md#3.5)
- [**4\. Programs and Initiatives**](04_Programs_and_Initiatives.md)
  - [4.1. CEOS EO-GPT & CEOS-GPT)](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.1)
  - [4.2. GEO](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.2)
  - [4.3. NASA (ESDIS, IMPACT)](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.3)
  - [4.4. NOAA/NCAI](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.4)
  - [4.5. Indian Space Research Organization (ISRO)](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.5)
  - [4.6. European Space Agency φ-lab](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.6)
  - [4.7. UKSA Initiative in AI and ML for Earth Observation](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.7)
- [**5\. Demonstrative use-cases**](05_Demonstrative_use_cases.md)
  - [5.1. Climate](https://github.com/ceos-org/aiml-white-paper/blob/main/05_Demonstrative_use_cases.md#5.1)
  - [5.2. Disaster](https://github.com/ceos-org/aiml-white-paper/blob/main/05_Demonstrative_use_cases.md#5.2)
  - [5.3. Infrastructure Monitoring](https://github.com/ceos-org/aiml-white-paper/blob/main/05_Demonstrative_use_cases.md#5.3)
  - [5.4. Precipitation](https://github.com/ceos-org/aiml-white-paper/blob/main/05_Demonstrative_use_cases.md#5.4)
  - [5.5. Sustainable Finance](https://github.com/ceos-org/aiml-white-paper/blob/main/05_Demonstrative_use_cases.md#5.5)
- [**6\. Hot topics/New topics**](06_Hot_topics_new_topics.md)
  - [6.1. Foundational Models](https://github.com/ceos-org/aiml-white-paper/blob/main/06_Hot_topics_new_topics.md#6.1)
  - [6.2. LLMs](https://github.com/ceos-org/aiml-white-paper/blob/main/06_Hot_topics_new_topics.md#6.2)
- [**7\. Data and platforms**](07_Data_and_Platforms.md)
- [**8\. Challenges & Limitations of AI4EO**](08_Challenges_and_Limitations_of_AI4EO.md)
- [**Appendix A. Glossary**](/Appendix/appendix-a-glossary.md)
- [**Appendix B Related Standards and Principles**](/Appendix/appendix-b-related-standards-and-principles.md)
- [**Appendix C. Templates for use case**](/Appendix/appendix-c-templates-for-use-case.md)
- [**Appendix D. AI Ready data checklist**](/Appendix/appendix-d-ai-ready-data-checklist.md)
- [**Reference**](/reference.md)



***

# 1\. Introduction

## 1.1. Preface by the co-chairs<a id='1.1'></a> 

Satellite Earth Observation (EO) technologies allow us to 'look back in time' as far as the 1970s[^1], offering valuable insights into the state of the natural environment and the impacts of human activities. This long-term, global coverage provides a unique perspective for measuring, monitoring and understanding environmental dynamics that are critical to addressing today’s greatest challenges, particularly in advancing the sustainability agenda. Even Antarctic glaciers have recently been named after their ‘satellite heroes’[^2], acknowledging the role of EO in revealing the effects of human activities and a changing climate on these fragile landscapes.

The challenge lies in making sense of the vast volumes of satellite data. Artificial Intelligence and Machine Learning (AI/ML) are uniquely positioned to (1) share the cognitive load, scaling the automation of repetitive analytical tasks. (2) Detect complex or subtle patterns often beyond human perception, from hyperspectral signatures of minerals to the changing signals of an infected crop field. (3) Complement human intuition, recognising that automation and information extracting alone are not enough. An effective human \- AI synergy is essential to transform raw data into actionable insights. Together, EO and AI/ML offer a scalable, global perspective on Earth’s complex processes, opening the door to innovative solutions that advance the UN Sustainable Development Goals. 

This document presents an overview of AI/ML initiatives led by the global space agencies that make up CEOS, highlighting recent advancements in applying these technologies to EO. To frame this landscape, it includes a brief introduction to EO sensor data, key AI/ ML concepts and illustrative applications that integrate AI/ML with EO. Emerging and cutting-edge topics, such as the move from task-specific AI models to foundation models are also briefly explored. 

This document is not intended to be exhaustive. Instead, it serves as a living document, a central reference point for tracking the rapidly evolving intersection of EO and AI/ML. Contributions from the community are warmly encouraged and welcomed: if you would like to expand or update any section, please share your suggestions or content via [GitHub](https://github.com/ceos-org/aiml-white-paper) repository or [contribution form](https://forms.gle/UiCNXoENw24f1gFG6). All inputs will be considered for review alongside analysis of key developments in EO and AI/ML. The document is intended to be updated annually to reflect the latest advancements.   
We especially encourage contributions from space agencies and institutions in the Global South to help ensure diverse perspectives and equitable representation across the global EO and AI/ML community. In future editions, in addition to incorporating community contributions and highlighting major EO and AI/ML developments, we aim to organise dedicated workshops to capture a coordinated roadmap and concrete recommendations on how CEOS agencies can strengthen collaboration in this rapidly evolving domain.

TEIG co-chairs

## 1.2. TEIG Contributors<a id='1.2'></a> 

This document has been developed by the members of the Technology Exploration Interest Group (TEIG) of Committee on Earth Observation Satellites (CEOS) Working Group on Information Systems and Services (WGISS). 

**Co-chairs**

- Yousuke Ikehata | Japan Aerospace Exploration Agency (JAXA)


- Maral Bayaraa | Satellite Applications Catapult representative of the UK Space Agency (UKSA)

**Project Members**

- European Commission (EC)
  - Peter Strobl
- European Space Agency (ESA)
  - Cristian Rossi
  - Gabriele Meoni
  - Hayret Abdula Keary
- Indian Space Research Organisation (ISRO)
  - Ashutosh Gupta
  - Nitant Dube
- National Aeronautics and Space Administration (NASA)
  - David Borges
  - Douglas Newman
  - Rustem Arif Albayrak
- National Oceanic and Atmospheric Administration (NOAA)
  - Rob Redmon
  - Yuhan “Douglas” Rao
- United Kingdom 
  - David Moffat (PML)
  - Diane Knappett (STFC)
- Irish Centre for High-End Computing (ICHEC)
  - Alastair McKinstry
- Technische Universitat - Berlin
  - Begum Demir
- Auspatious
  - Alex Leith
- Aspia Space
  - Freddie Kalaitzis

**Acknowledgements**

- CEO of the Committee on Earth Observation Satellites (CEOS)
  - Steven Ramage
- The Group on Earth Observations (GEO)
  - Rui Kotani
- WGClimate
  - Wenying Su(NASA)
- WGDisasters
  - Alireza Taravat (ESA)
  - Guy Schumann(RSS Hydro)
  - Marcelo Uriburu Quirno (CONAEWMO)
  - Raquel Rodríguez Suquet(CNES)
  - William Straka(CIMSS/SSEC)
  - Xinyi Shen(University of Wisconsin Milwaukee)
  - Alessandro Novellino (British Geological Survey)
  - Claire Dashwood (British Geological Survey)
- United Kingdom
  - Rebecca Corey (UKSA)
  - Michelle Odgers(UKSA)
  - Rob Fletcher (Airbus)
  - Katie Awty-Carroll(PML)
- United States Geological Survey (USGS)
  - Tom Sohre
- Japan Aerospace Exploration Agency (JAXA)
  - Natsuisaka Makoto
  - Kazuki Nakata
  - Kosuke Yamamoto

[Previous](/README.md) | [Table of contents](/README.md) | [Next](02_Background.md)


[^1]: First civilian EO satellite Landsat-1 launched in 1972. https://landsat.gsfc.nasa.gov/satellites/landsat-1/
[^2]: https://www.bbc.com/news/science-environment-48547803 


[Next](01_Introduction.md)
