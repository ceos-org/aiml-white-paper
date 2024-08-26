[Previous](use-cases-at-WGISS.md) | [Table of contents](README.md) | [Next](conclusion.md)

***

# 7. Data and platform
This section introduces data and platforms used with machine learning and AI by CEOS/WGISS agencies indicated in the section 5.

## 7.1. Data
This section shows data available with machine learning and AI.
The use cases in section 5 are analyzed using the following data.
This section also introduces data that is not presented in section 5 but is available with machine learning and AI provided from CEOS agencies.

Annex Data

### 7.1.1. BigEarthNet
BigEarthNet is a large-scale benchmark dataset, supporting deep learning (DL) studies for remote sensing image analysis. The recently released version of  BigEarthNet (BigEarthNet v2.0)   is made up of 549,488 pairs of Sentinel-1 and Sentinel-2 image patches acquired over 10 European countries [[9](https://github.com/ceos-org/aiml-white-paper/blob/main/reference.md)].  
Each pair of patches in BigEarthNet is associated with a pixel-level reference map and scene-level multi-labels provided by the CORINE Land Cover (CLC) map of 2018. To pay more justice to the properties of BigEarthNet image pairs, its developers introduced a new class-nomenclature by modifying the labels extracted from the CLC 2018. To this end, the CLC Level-3 nomenclature is interpreted and arranged in a new nomenclature of 19 classes [[10](https://github.com/ceos-org/aiml-white-paper/blob/main/reference.md)].  
The complete dataset, the code for constructing it in a reproducible manner and also the weights of several pre-trained models  (which are: i) ResNet; ii) vision transformer; iii) MLP-Mixer; iv) ConvMixer; v) MobileViT; and vi) ConvNeXt-v2) using BigEarthNet are publicly available at https://bigearth.net.  
We would like to note that the public availability of the code developed for its construction allows all its users not only to reproduce the dataset but also to extend it to any geographical area of interest. Moreover, a software tool (called as rico-hdl) that converts the dataset into a DL-optimized data format has been recently released by its developers to minimize the DL model training time. For details, we refer the Reader to the dataset webpage https://bigearth.net.

## 7.2. Machine learning and AI analysis platform
This section indicates the analysis platforms available with machine learning and AI.
Some of the use cases in section 5 are used for public analysis platforms and such platforms are introduced.
This section also introduces the platforms that are not presented in the section 5 but is available with machine learning and AI provided from CEOS agencies.

Appendix. Platform

***
[Previous](use-cases-at-WGISS.md) | [Table of contents](README.md) | [Next](conclusion.md)
