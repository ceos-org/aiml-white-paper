[Previous](the-future-of-ai4eo-research.md) | [Table of contents](/README.md) | [Next](aiml-tasks-and-use-cases.md)

***
## 3.4. MLOps Life cycle and tasks

### 3.4.1. Background for MLOps life cycle

Machine Learning Operations (MLOps) refers to the idea of best practice managing and operating machine learning systems in production.

Originally, DevOps unified software development and operations through continuous integration and delivery (CI/CD), enabling teams to deploy software faster with fewer errors.

However AI/ML applications are inherently more complex than traditional software. While most  traditional software is composed primarily of code, AI/ML systems consist of code \+ data \+ trained models. In addition, they require well-defined workflows and pipelines for data processing, model training, evaluation and deployment.   **MLOps** has emerged to bridge these gaps, adapting DevOps principles to the unique challenges of AI/ML, and ensuring that machine learning solutions are scalable, reliable, and sustainable in real-world operations.\[[139](/reference.md#ref.139), [140](/reference.md#ref.140), [141](/reference.md#ref.141), [142](/reference.md#ref.142)\]

![MLOps lifecycle example source](/figures/Figure3.4.2-1.png)  
Figure-3.4.2-1 MLOps lifecycle example source: NVIDIA\[[140](/reference.md#ref.140)\]

### 3.4.2. Life cycle

MLOps is a concept as a workflow, and there is no common standardized definition.  
Key Points and relevant remote sensing tasks are shown in Table 3.4.2-1.

Table 3.4.2-1 MLOps stages and tasks

| MLOps Stage | Description | Relevant Remote Sensing Tasks |
| ----- | ----- | ----- |
| **1\. Data Collection & Ingestion** | Collecting raw data from satellites, aerial sensors, ground truth, etc. | \- Data Fusion (multi-sensor)- Time Series Acquisition- Spatial-Temporal Data Gathering |
| **2\. Data Processing & Labeling** | Preprocessing such as denoising, normalization, labeling, and annotation | \- Cloud Masking / Atmospheric Correction- Image Registration- Labeling for Classification, Segmentation, Detection |
| **3\. Model Development & Training** | Selecting models, training algorithms, tuning hyperparameters | \- Land Use Classification- Semantic Segmentation (e.g., flood or crop areas)- Object Detection (e.g., buildings, vehicles)- Change Detection- Anomaly Detection |
| **4\. Model Validation & Evaluation** | Evaluating model performance and generalizability | \- Performance Metrics: Accuracy, F1-score, IoU- Validation using labeled satellite or ground truth data |
| **5\. Model Deployment** | Integrating trained models into production systems like dashboards, APIs, GIS tools | \- Real-time detection for disaster response- Production segmentation pipelines |
| **6\. Monitoring & Feedback** | Monitoring drift, model performance degradation, triggering retraining | \- Distribution/Drift Monitoring- Error analysis (e.g., confusion maps)- Feedback from new imagery or user corrections |
| **7\. Continuous Training / CI-CD** | Automating retraining, model versioning, and deployment pipelines | \- Continuous integration of updated time series- Online learning for dynamic environmental monitoring |


***

[Previous](the-future-of-ai4eo-research.md) | [Table of contents](/README.md) | [Next](aiml-tasks-and-use-cases.md)
