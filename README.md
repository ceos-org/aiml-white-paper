[Next](01_Introduction.md)

***
# CEOS ML/DL/AI White Paper 

Technology Exploration Interest Group of CEOS-WGISS

Doc. Ref.: CEOS/WGISS TEIG(Technology Exploration Interest Group)

Date: Dec.  2025

Issue: Version 1.0
----
## Table of Contents

- [**1\. Introduction**](01_Introduction.md)
  - [1.1. Preface by the co-chairs]
  - [1.2. TEIG Contributors]
- [**2\. Background**](02_Background)
  - [2.1. Overview of Earth Observation]
  - [2.2. Core ideas in Deep Learning]
- [**3\. Research trends in AI4EO**](03_Research-trends-in-ai4eo.md)
  - [3.1. Venues of cross-disciplinary research]
  - [3.2. From sensing to applications]
  - [3.3. The future of AI4EO research]
  - [3.4. MLOps Life cycle and tasks]
  - [3.5. AI/ML Tasks and use cases]
- [**4\. Programs and Initiatives**](04_Programs_and_initiatives.md)
  - [4.1. CEOS EO-GPT & CEOS-GPT)](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.1)
  - [4.2. GEO](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.2)
  - [4.3. NASA (ESDIS, IMPACT)](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.3)
  - [4.4. NOAA/NCAI](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.4)
  - [4.5. Indian Space Research Organization (ISRO)](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.5)
  - [4.6. European Space Agency φ-lab](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.6)
  - [4.7. UKSA Initiative in AI and ML for Earth Observation](https://github.com/ceos-org/aiml-white-paper/blob/main/04_Programs_and_Initiatives.md#4.7)
- [**5\. Demonstrative use-cases**](05Demonstrative-use-cases)
  - [5.1. Climate]
  - [5.2. Disaster]
  - [5.3. Infrastructure Monitoring]
  - [5.4. Precipitation]
  - [5.5. Sustainable Finance]
- [**6\. Hot topics/New topics**](06_Hot_topics_new_topics.md)
  - [6.1. Foundational Models]
  - [6.2. LLMs]
- [**7\. Data and platforms**](07_Data_and_Platforms.md)
  - [7.1. Data for AI/ML data interoperability]
  - [7.2. Geospatial AI Platforms]
- [**8\. Challenges & Limitations of AI4EO**](08_Challenges_and_Limitations_of_AI4EO.md)
  - [8.1. Data scarcity & labelling challenges]
  - [8.2. Computational demands for large-scale analysis]
  - [8.3. Model interoperability & trustworthiness]
- [**9\. Conclusion and Future outlook.	76**]
- [**Appendix A. Glossary**](/Appendix/appendix-a-glossary.md)
- [**Appendix B Related Standards and Principles**](/Appendix/appendix-b-related-standards-and-principles.md)
- [**Appendix C. Templates for use case**](/Appendix/appendix-c-templates-for-use-case.md)
- [**Appendix D. AI Ready data checklist**](/Appendix/appendix-d-ai-ready-data-checklist.md)
- [**Reference**](/reference.md)



***

## Preface by the co-chairs

Satellite Earth Observation (EO) technologies allow us to 'look back in time' as far as the 1970s[^1], offering valuable insights into the state of the natural environment and the impacts of human activities. This long-term, global coverage provides a unique perspective for measuring, monitoring and understanding environmental dynamics that are critical to addressing today’s greatest challenges, particularly in advancing the sustainability agenda. Even Antarctic glaciers have recently been named after their ‘satellite heroes’[^2], acknowledging the role of EO in revealing the effects of human activities and a changing climate on these fragile landscapes.

The challenge lies in making sense of the vast volumes of satellite data. Artificial Intelligence and Machine Learning (AI/ML) are uniquely positioned to (1) share the cognitive load, scaling the automation of repetitive analytical tasks. (2) Detect complex or subtle patterns often beyond human perception, from hyperspectral signatures of minerals to the changing signals of an infected crop field. (3) Complement human intuition, recognising that automation and information extracting alone are not enough. An effective human \- AI synergy is essential to transform raw data into actionable insights. Together, EO and AI/ML offer a scalable, global perspective on Earth’s complex processes, opening the door to innovative solutions that advance the UN Sustainable Development Goals. 

This document presents an overview of AI/ML initiatives led by the global space agencies that make up CEOS, highlighting recent advancements in applying these technologies to EO. To frame this landscape, it includes a brief introduction to EO sensor data, key AI/ ML concepts and illustrative applications that integrate AI/ML with EO. Emerging and cutting-edge topics, such as the move from task-specific AI models to foundation models are also briefly explored. 

This document is not intended to be exhaustive. Instead, it serves as a living document, a central reference point for tracking the rapidly evolving intersection of EO and AI/ML. Contributions from the community are warmly encouraged and welcomed: if you would like to expand or update any section, please share your suggestions or content via [GitHub](https://github.com/ceos-org/aiml-white-paper) repository or [contribution form](https://forms.gle/UiCNXoENw24f1gFG6). All inputs will be considered for review alongside analysis of key developments in EO and AI/ML. The document is intended to be updated annually to reflect the latest advancements.   
We especially encourage contributions from space agencies and institutions in the Global South to help ensure diverse perspectives and equitable representation across the global EO and AI/ML community. In future editions, in addition to incorporating community contributions and highlighting major EO and AI/ML developments, we aim to organise dedicated workshops to capture a coordinated roadmap and concrete recommendations on how CEOS agencies can strengthen collaboration in this rapidly evolving domain.

TEIG co-chairs: Yousuke Ikehata (JAXA) and Maral Bayaraa (UK)

[Next](01_Introduction.md)
