[Previous](README.md) | [Table of contents](/README.md) | [Next](llms.md)

***

## 6.1. Foundational Models

The paradigm shift in AI/ML is the idea of being able to train a machine learning model capable of doing many different tasks (object detection, segmentation, image captioning, classification..) based on data from a variety of satellite sensors. This is the promise of ‘foundation models’, as shown in Figure 5.1-1. It represents a shift away from task-specific AI/ML approaches (such as the ones described in Section Y) to versatile models that are trained on multi-modal data from different satellite sensors, resolutions that can be adapted to make predictions across a range of downstream tasks, such as predicting wildfires to mapping land cover and floods to forest monitoring.  

![Figure6.1-1](/figures/Figure6.1-1.png)  
*Figure 6.1-1: foundation models aim to be able to take many different types of data, including different EO data modalities for a variety of downstream taks. From [Xiong et al. (2024)](https://arxiv.org/pdf/2403.15356v2)*

Foundation models can be categorized by its functions.

### 6.1.1. Vision Foundation Model

These models are trained solely on visual (image-based) data from remote sensing platforms such as satellites or drones. They are designed to understand and interpret spatial features and patterns in imagery. Applications include land cover classification, object detection, semantic segmentation, and change detection. 

**Key characteristic:**   
Exclusively trained on visual data, these models learn hierarchical, multi-scale representations that capture spatial context, texture, and morphology. This enables consistently strong performance on dense, pixel-wise inference (semantic/instance segmentation, change detection) and object-level reasoning (detection, tracking) across sensors and resolutions. Pretraining objectives such as contrastive learning and masked-image modeling promote invariance to viewpoint, illumination, seasonal, and atmospheric variation, improving robustness, domain transfer, and few-shot fine-tuning in geospatial applications.

![Figure6.1.1-1](/figures/Figure6.1.1-1.png)  
*Figure 6.1.1-1: foundation models aim to be able to take many different types of data, including different EO data modalities for a variety of downstream tasks. From [XIan Sun et al.](https://ieeexplore.ieee.org/document/9844015)*

### 6.1.2. Vision-Language Foundation Model

These models combine visual data with textual data (e.g., labels, descriptions, captions, metadata). They are trained on paired image-text datasets and can understand and generate natural language related to remote sensing imagery. This allows for capabilities like image captioning, visual question answering (VQA), and cross-modal retrieval (e.g., finding images based on text queries or vice versa).

**Key characteristic:**  
Multimodal learning that fuses vision and language by aligning image and text representations (e.g., via contrastive objectives and cross-attention) to enable interactive, interpretable analysis of EO data. This alignment supports open-vocabulary, promptable understanding and zero-/few-shot generalization for tasks such as captioning, VQA, cross-modal retrieval, and classification across sensors and resolutions. Incorporating textual prompts, ontologies, and metadata (e.g., geotags, acquisition time, sensor) provides semantic grounding and controllable inference, while instruction-tuning yields robust performance under distribution shifts and facilitates natural-language rationales for improved explainability.

![Figure6.1.2-1](/figures/Figure6.1.2-1.png)  
*Figure 6.1.2-1:EarthGPT as Vision Language Models From [Wei Zhang et al.(2024)](https://arxiv.org/pdf/2401.16822)*

### 6.1.3. Generative Foundation Models

These models are capable of generating new data, either visual or multimodal, based on learned representations. They include generative models like GANs, diffusion models, or transformer-based models such as GPT for geospatial data. Applications include synthetic image generation (e.g., simulating satellite images), super-resolution, data augmentation, and future prediction (e.g., predicting land change).

**Key characteristic:**  
Generative models perform enhancement and restoration (super-resolution, pan-sharpening, denoising/cloud removal, gap-filling), spatiotemporal forecasting, and cross-sensor translation/fusion (e.g., optical↔SAR) with geometric and radiometric consistency. Physics- and sensor-aware constraints improve realism and provide uncertainty estimates, while synthetic augmentation and generative priors strengthen downstream segmentation/detection and support provenance and bias auditing.

![Figure6.1.3-1](/figures/Figure6.1.3-1.png)  
*Figure 6.1.3-1. From [Zhiping Yu et al. (2024)](https://arxiv.org/abs/2405.13570)*

### 6.1.4. Limitation of Foundation Models

There are notable foundation models such as Prithvi, Terramind.

Despite the promise of foundation models, there are critical challenges currently holding back its widespread practical application in remote sensing. The computational resources required for training and fine-tuning foundation models are significantly higher than task-specific AI approaches. Task-specific AI/ML models still perform better and have a much lower computational cost compared to foundation models for a variety of downstream tasks (e.g. [*Marsocci et al. (2024)*](https://arxiv.org/pdf/2412.04204)). This is illustrated in Figure X2, where task-specific UNet model outperforms most foundation models in a variety of scenarios, except for when there are limited labels available. 

![Figure6.1.4-1](/figures/Figure6.1.4-1.png)  
*Figure 6.1.4-1: Comparison of the performance of different foundation models and a task-specific UNet model on a variety of dataset. The y-axis represents the normalized performance across the 11 PANGAEA’s benchmark datasets, where the best performing model is assigned a value of 1 and the worst performing model, a value of 0\. (a) Full Labels: the models are trained on downstream tasks with access to fall the labelled dataset. The task-specific baselines, especially UNet outperforms the foundation models. (b) Limited Labels (10%): models are trained on downstream tasks with access to only 10% of labelled data. In this scenario, the foundation models, especially CROMA, excel and outperform the supervised baselines. (c) Multi-spectral data: UNet excels and outperforms foundation models. Foundation models pre-trained on high resolution data, such as Scale-MAE, underperform. (d) High resolution data: Foundation models pre-trained on high-resolution images and UNet perform well. However, most foundation models pre-trained on lower-resolution imagery, such as Prithvi, underperform. From [Marsocci et al. (2024)](https://arxiv.org/pdf/2412.04204)*.

### 6.1.5. Prithvi

Prithvi is a first-of-its-kind temporal Vision Transformer foundation model developed collaboratively by IBM and NASA, pre-trained on contiguous US Harmonized Landsat Sentinel 2 (HLS) data using a self-supervised Masked AutoEncoder (MAE) learning strategy. The model uniquely incorporates both spatial attention across multiple patches and temporal attention for each patch, accepting remote sensing data in video format with a crucial temporal dimension that distinguishes it from other geospatial models. Its accuracy outperforms six other geospatial foundation models when benchmarked on remote sensing tasks across different domains and resolutions (from 0.1m to 15m), demonstrating versatility in both classical earth observation and high-resolution applications. The model has wide-ranging potential applications including tracking land use changes, monitoring natural disasters, and predicting crop yields. 

### 6.1.7. TerraMind

TerraMind is the first multimodal generative foundation model for Earth Observation, developed jointly by IBM, the European Space Agency (ESA) Φ-lab, and the FAST-EO project. The model uses a dual-scale transformer-based encoder-decoder architecture built on Prithvi that simultaneously processes pixel-level and token-level data Geospatial foundation models for image analysis: evaluating and enhancing NASA-IBM Prithvi’s domain adaptability, combining insights from nine types of Earth observation data, include optical and radar imagery from Sentinel-1 and -2 satellites, textual representations of the environment, geomorphology, AI generated Land cover classification, vegetation, and historical climate data, to provide an intuitive understanding of our planet. TerraMind introduces the "Thinking-in-Modalities" approach to handle missing modalities and reaches new state-of-the-art results on downstream tasks. The model outperforms comparable models in performance tests while requiring less computing power, and is available as an open-source model on Hugging Face for researchers and practitioners working with geospatial data.

***

[Previous](README.md) | [Table of contents](/README.md) | [Next](llms.md)
