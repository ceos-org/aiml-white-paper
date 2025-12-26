[Previous](foundational-models.md) | [Table of contents](/README.md) | [Next](/data-and-platforms/README.md)

***

## 6.2. LLMs

Large Language Models(LLMs) are used on various occasions without earth observation.

**Use cases**  
While LLMs have traditionally been applied in natural language processing tasks, their integration into remote sensing is gaining traction. Key current use cases include:

* Metadata and Report Generation: LLMs are used to generate textual summaries of satellite imagery analysis, automate mission reports, and create descriptions for geospatial datasets.  
* Semantic Search & Retrieval: By linking natural language queries to remote sensing data, LLMs enable intuitive search and support interfaces (ref. [EO advanced AI Assistant](#6.2.1.-eo-advanced-ai-assistant))  
* Multimodal Systems: Combined with vision models, LLMs support vision-language tasks such as image captioning, question answering, and cross-modal analysis in remote sensing contexts.(ref. [Vision-Language Models](#6.1.2.-vision-language-foundation-model))

### 6.2.1. EO Advanced AI Assistant

The EO AI Advanced Assistant is a research demonstrator which aims to provide quick and unrestricted access to ESA Earth Explorers and Third Party Mission data, information and services made available by the European Space Agency.

This project which is currently at the pre-operational beta version stage leverages Large Language Models and Natural Language Processing techniques for intent understanding, query interpretation and name entity recognition. The LLM has been enhanced with features which allow it to extract queries and parameters via the EO MAAP Catalogue API, ESA TellUs API and EO Identity Access Management API. This allows integration with systems for data discovery, data request and personal user profile retrieval. Furthermore the system queries a vector database of regularly updated web information furnished by ESA via the Earth Online (earth.esa.int) and eoPortal (eoportal.org) websites allowing it to provide the latest updates to its users.  
To address the limitations of LLM hallucinations the mechanism is validated through transformed based pipelines fine tuned on EO specific entities.  
This multi function solution provides users with a single interface to simplify access for both entry-level and experienced users.  
The EO AI Advanced Assistant is being developed with operational principles in mind ensuring compliance with security and hosting requirements for future upscaling and operational release as well as integration with a wider range of tools and services.  
The strength of the assistant lies in its versatile orchestration of AI tools and pipelines delivering a personalized experience for data product discovery, visualisation, technical and code based support and data access bridging the gap between research and operations.  
The assistant uses Retrieval Augmented Generation (RAG) to provide answers from a regularly updated vector database of contents which uses sources such as the Earth Online website ([earth.esa.int](http://earth.esa.int)) and the eoPortal website ([eoportal.org](http://eoportal.org)). The eoPortal website is a compendium of global Earth Observation missions built on top of the CEOS Missions, Instruments and Measurements Database ([https://database.eohandbook.com/](https://database.eohandbook.com/) ).

***

[Previous](foundational-models.md) | [Table of contents](/README.md) | [Next](/data-and-platforms/README.md)
