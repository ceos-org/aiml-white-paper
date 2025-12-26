[Previous](/data-and-platforms/README.md) | [Table of contents](/README.md) | [Next](conclusion-and-future-outlook.md)

***

# 8\. Challenges & Limitations of AI4EO

The transformative potential of Artificial Intelligence (AI) is tempered by a set of inherent challenges and limitations that are critical to understand for strategic implementation. AI models are not infallible; their performance is intrinsically linked to the quality of their training data and they can exhibit significant shortcomings when applied outside their original design parameters. Furthermore, the development of sophisticated models necessitates substantial computational resources, creating cost and scalability barriers. Organizations must also navigate a complex landscape of legal and ethical considerations, including data privacy, algorithmic bias, and regulatory compliance. A clear comprehension of these constraints is essential for managing risk, setting realistic expectations, and deploying AI solutions in a sustainable and responsible manner.

## 8.1. Data scarcity & labelling challenges

The development and deployment of robust Artificial Intelligence and Machine Learning (AI/ML) models for geospatial analysis are fundamentally constrained by the availability and quality of training data. Unlike other domains, the unique characteristics of satellite and aerial imagery present significant hurdles in data acquisition and preparation, which directly impact the feasibility, cost, and timeline of AI initiatives. It is difficult to obtain ground *truth measurements* at a very large scale given the temporal variation due to natural and man made activities.

The primary challenge for geospatial models doesn’t lie in a general lack of imagery, but in the scarcity of *relevant, accurately annotated* data required to train these models for specific tasks. This challenge manifests in two core areas: the acquisition of usable data and the subsequent process of labelling it.

**The Challenge of Data Scarcity**

Data scarcity in the geospatial context is often a problem of relevance and specificity, rather than absolute volume.

* **Class imbalance due to event rarity:** Many critical applications involve detecting events or features that are inherently rare within vast geographical areas. For instance, identifying maritime oil spills, monitoring illegal logging, or detecting specific infrastructure failures requires training models on a significant number of positive examples, which are difficult to acquire due to their low occurrence rate.  
* **Lack of Historical Data:** For novel applications or new satellite sensors, sufficient historical data simply may not exist. This absence prevents the training of models that require longitudinal analysis or a deep historical baseline for comparison.  
* **Domain-Specific Requirements:** Models are highly sensitive to the conditions under which training data was captured. Variations in atmospheric conditions, seasonal changes, sun illumination angles, and sensor specifications can drastically alter the appearance of a location. Consequently, data that is not representative of the target operational environment has limited utility, effectively creating a scarcity of contextually appropriate imagery.

**The Labelling Bottleneck**

The process of annotating geospatial imagery, known as labelling, is a critical and resource-intensive bottleneck. The accuracy of the labels directly determines the performance and reliability of the resulting AI model.

* **Requirement for Expert Knowledge:** Accurate labelling of geospatial data is not a trivial task. It requires domain-specific expertise to correctly identify and delineate features. Distinguishing between crop types, classifying geological formations, or identifying specific maritime vessels necessitates skills possessed by geologists, agronomists, and other subject matter experts. This reliance on a scarce and expensive workforce significantly increases the cost and time required for data preparation.  
* **Subjectivity and Consistency:** Labelling can involve a degree of interpretation, leading to inconsistencies. Different experts may have differing opinions on the precise boundaries of a feature or its classification. Without rigorous standardized protocols, this subjectivity introduces "label noise," which degrades model performance and erodes trust in the AI's outputs.  
* **Scale and Labor Intensity:** Labelling is a manual process that does not scale efficiently. High-resolution imagery covers extensive areas, and annotating features at the pixel level (e.g., for land cover classification) is an immensely time-consuming and tedious endeavour. The cost of creating large, accurately labelled datasets often constitutes one of the largest investments in an AI/ML project.

## 8.2. Computational demands for large-scale analysis

The application of artificial intelligence and machine learning to large-scale geospatial data analysis entails significant computational requirements, which in turn pose substantial environmental and operational challenges \[[152](/references.md#ref.152)\]. Training sophisticated deep learning models—particularly those processing high-resolution satellite imagery across extensive geographical areas—demands immense processing power, typically supplied by high-performance computing clusters or cloud-based Graphic Processing Unit (GPU) arrays. This reliance on energy-intensive hardware contributes directly to elevated carbon emissions, particularly in regions where electricity generation remains dependent on fossil fuels. The financial cost of such computational resources can also be prohibitive, limiting access for smaller organizations or public sector entities and potentially widening the gap between well-resourced and emerging players in the field.

Moreover, the environmental footprint of model training and inference is further amplified by the need for repeated experiments, hyperparameter tuning, and continuous model updates to maintain accuracy over time. As geospatial datasets grow in volume and resolution, and as algorithms increase in complexity, the energy consumption required for meaningful analysis will continue to rise. Organizations are therefore encouraged to adopt efficiency-minded strategies such as model optimization, selective processing, and energy-aware computing infrastructure to align technological advancement with sustainability goals. Without deliberate mitigation efforts, the scalability of AI-driven geospatial insights may come at a considerable ecological cost.

## 8.3. Model interoperability & trustworthiness

Model interoperability refers to the ability of AI systems to seamlessly exchange information and utilize functionality across diverse platforms, software environments, and data formats, which is essential for integrating specialized tools into broader analytical workflows and avoiding vendor lock-in. Trustworthiness, a multifaceted requirement, encompasses not only the technical performance such as accuracy, robustness, and reliability, but also adherence to ethical principles, including fairness, transparency, and accountability. Establishing trust requires that models operate consistently under varying conditions, provide explanations for their outputs, and are developed with rigorous validation and governance frameworks to ensure they perform as intended without causing unintended harm. Therefore, fostering interoperability and embedding trustworthiness are not merely technical challenges but foundational to the responsible adoption, scalability, and long-term success of AI technologies in critical applications.

The current state of model interoperability in geospatial AI remains highly fragmented, with numerous proprietary formats and closed ecosystems limiting seamless integration. While standards like OGC APIs and cloud-optimized formats are emerging, widespread adoption is still evolving. Most models are developed for specific platforms or data structures, creating significant friction in cross-system deployment and collaboration. This lack of cohesion hinders the scalability, reproducibility, and efficient combination of specialized models into unified analytical workflows.

***

[Previous](/data-and-platforms/README.md) | [Table of contents](/README.md) | [Next](conclusion-and-future-outlook.md)
