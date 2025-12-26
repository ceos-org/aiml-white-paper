[Previous](README.md) | [Table of contents](/README.md) | [Next](geo.md)

***

## 4.1. CEOS SEO

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

***

[Previous](README.md) | [Table of contents](/README.md) | [Next](geo.md)
