[Previous](README.md) | [Table of contents](/README.md) | [Next](venues-of-cross-disciplinary-research.md)

***

# 3\. Research trends in AI4EO

The rate of progress in AI4EO is primarily driven by advances in hardware and sensor design first, and then by ML software—research-grade code born out of academic papers that eventually makes it into production-grade **GIS** dev tools. The comoving **SOTA** in ML then translates into new model specifications per use-case. For example a new SOTA in semantic **segmentation** will be immediately translated into a solution for segmenting agricultural parcels. This publication pattern occurs enough times in a year to keep practitioners on their toes. The good news is that the useful set of foundational ideas is extended at least every few years. We covered those in section [**2.2\. Core ideas in Deep Learning**.](/Background/core-ideas-in-deep-learning.md)

***


## 3.1. Venues of cross-disciplinary research<a id='3.1'></a> 

The following is a brief overview on top-tier academic conferences, for the readers who are interested in staying up to date with the SOTA in ML. Key journal publications include: JMLR\[[2](/reference.md#ref.2)\], TPAMI \[[3](/reference.md#ref.3)\], FTML\[[4](/reference.md#ref.4)\], TMLR\[[5](/reference.md#ref.5)\]. Key conferences include: NeurIPS \[[6](/reference.md#ref.6)\], ICML, ICLR\[[7](/reference.md#ref.7)\], CVPR\[[8](/reference.md#ref.8)\], AAAI\[[9](/reference.md#ref.9)\], AISTATS\[[10](/reference.md#ref.10)\]. Aside from the main proceedings, each conference also hosts satellite academic workshop events catered to researchers working in specific basic and applied research domains. In the context of AI4EO, the following AI4EO workshops are staples in most annual iterations of the aforementioned conferences: EarthVision\[[11](/reference.md#ref.11)\], AI4Earth\[[12](/reference.md#ref.12)\], MLPS\[[13](/reference.md#ref.13)\], CCAI\[[14](/reference.md#ref.14)\]. Because of their interdisciplinary nature, some of these events are supported by IEEE technical committees which also host their own conferences, like IGARSS\[[15](/reference.md#ref.15)\].

The development and publication of ideas in AI4EO follow a common trajectory:

1. A new SOTA is published at a conference, typically on a problem unrelated to EO.  
2. EO practitioners discover the new ML paper and translate it to their problem.  
3. Occasionally, the translation of the new paper will be successful and the EO researchers will publish their preliminary results in a EO workshop or symposium, such as AGU\[[16](/reference.md#ref.16)\], EGU\[[17](/reference.md#ref.17)\], LPS\[[18](/reference.md#ref.18)\]. This is a good opportunity to receive early feedback from the EO research community.  
4. Finally, the new ML application makes it into a EO or RS journal.

Note that at step 1 of this workflow the new ML methods are not benchmarked on EO datasets. This status quo is perpetuated by much of the ML community framing the advancement of the **SOTA** only with respect to traditional benchmarks for image classification, segmentation, object detection—like ImageNet \[[19](/reference.md#ref.19)\], CIFAR\[[20](/reference.md#ref.20)\], COCO \[[21](/reference.md#ref.21)\]—while EO tasks are not yet featured in the standard regiment of benchmarks. However, an increasing number of larger and larger scale datasets are starting to pop up, like those of the SpaceNet competitions\[[22](/reference.md#ref.22)\]. 

***

## 3.2. From sensing to applications<a id='3.2'></a> 

**Table 3.2-1** provides a detailed breakdown of most of the work in AI4EO in various verticals. Here are the main takeaways:

* Most of the works in AI4EO investigate optical data since it is the most abundant.  
* **CNN** architectures have recently become the most ubiquitous architecture as they allow for the discovery of shift-invariant patterns not only in space, but also in time (**3D-CNNs**). They are also easier to train than **RNNs**, hence the latter are starting to be used less frequently. Therefore, CNNs are recognised as a natural fit for segmentation and classification problems in EO.  
* **SAR** data is becoming increasingly available, with many interesting use-cases emerging for InSAR.  
* With a heterogeneous array of sensors, it is clear that learning to **fuse** instruments harmoniously is key to complementing the observation gaps in isolated instruments.  
* The majority of use-cases in EO are framed as **segmentation** problems, to identify the spatial extent of an object, or regression / nowcasting / forecasting of continuous quantities, like crop yield.  
* Scientific fields have all found uses of ML to embed data into physical models (data assimilation), or fine-tuning physical models through data (parameter retrieval), or forming digital-twins of large-scale phenomena for cheaper simulation and at finer resolutions (down-scaling, subgrid-parametrization).  
* Agriculture is becoming the most frequent user of EO data (after intelligence / reconnaissance users), both in the environmental / sustainability front, like food-security, and commercially, for crop yield forecasting, monitoring, and asset management.  
* Understanding the type of some surface on the Earth (LULC) is a problem that cuts across many disciplines, and ties naturally with **classification** and **segmentation** ML tasks and **architectures**.

| proximity | sensor | method | task | application |
| ----- | ----- | ----: | ----- | ----: |
|  orbital / satellite \[[23](/reference.md#ref.23), [24](/reference.md#ref.24)\]</br>aerial \[[25](/reference.md#ref.25),[26](/reference.md#ref.26),[27](/reference.md#ref.27), [28](/reference.md#ref.28), [29](/reference.md#ref.29), [30](/reference.md#ref.30), [31](/reference.md#ref.31)\]</br>in-situ / ground data \[[32](/reference.md#ref.32), [33](/reference.md#ref.33), [34](/reference.md#ref.34), [35](/reference.md#ref.35)\] |  optical \[[36](/reference.md#ref.36), [37](/reference.md#ref.37), [38](/reference.md#ref38), [39](/reference.md#ref.39), [40](/reference.md#ref.40), [41](/reference.md#ref.41), [42](/reference.md#ref.42), [43](/reference.md#ref.43), [44](/reference.md#ref.44), [45](/reference.md#ref.45), [46](/reference.md#ref.46), [47](/reference.md#ref.47), [48](/reference.md#ref.48), [49](/reference.md#ref.49), [50](/reference.md#ref.50), [27](/reference.md#ref.27), [51](/reference.md#ref.51), [52](/reference.md#ref.52), [53](/reference.md#ref.53), [54](/reference.md#ref.54), [55](/reference.md#ref.55), [56](/reference.md#ref.56), [57](/reference.md#ref.57), [58](/reference.md#ref.58), [59](/reference.md#ref.59), [60](/reference.md#ref.60)\] </br>SAR \[[41](/reference.md#ref.41), [25](/reference.md#ref.25), [61](/reference.md#ref.61), [48](/reference.md#ref.48), [62](/reference.md#ref.62), [63](/reference.md#ref.63), [26](/reference.md#ref.26), [34](/reference.md#ref.34), [64](/reference.md#ref.64), [65](/reference.md#ref.65), [66](/reference.md#ref.66), [67](/reference.md#ref.67), [68](/reference.md#ref.68), [69](/reference.md#ref.69), [70](/reference.md#ref.70), [71](/reference.md#ref.71), [72](/reference.md#ref.72), [60](/reference.md#ref.60), [73](/reference.md#ref.73), [74](/reference.md#ref.74), [75](/reference.md#ref.75)\]</br>lidar \[[76](/reference.md#ref.76), [41](/reference.md#ref.41), [26](/reference.md#ref.26), [77](/reference.md#ref.77), [54](/reference.md#ref.54), [78](/reference.md#ref.78), [79](/reference.md#ref.79), [80](/reference.md#ref.80), [29](/reference.md#ref.29), [30](/reference.md#ref.30), [31](/reference.md#ref.31), [81](/reference.md#ref.81)\] | autoencoder \[[82](/reference.md#ref.82), [83](/reference.md#ref.83), [84](/reference.md#ref.84), [85](/reference.md#ref.85)\]</br>attention / transformer \[[86](/reference.md#ref.86), [68](/reference.md#ref.68), [52](/reference.md#ref.52), [81](/reference.md#ref.81), [87](/reference.md#ref.87)\]</br>Bayesian / probabilistic \[[32](/reference.md#ref.32), [33](/reference.md#ref.33), [88](/reference.md#ref.88)\]</br>CNN / U-Net / ResNet \[[39](/reference.md#ref.39), [76](/reference.md#ref.76), [40](/reference.md#ref.40), [42](/reference.md#ref.42), [45](/reference.md#ref.45), [62](/reference.md#ref.62), [50](/reference.md#ref.50), [89](/reference.md#ref.89), [90](/reference.md#ref.90), [65](/reference.md#ref.65), [68](/reference.md#ref.68), [52](/reference.md#ref.52), [91](/reference.md#ref.91), [77](/reference.md#ref.77), [28](/reference.md#ref.28), [92](/reference.md#ref.92), [54](/reference.md#ref.54), [59](/reference.md#ref.59), [81](/reference.md#ref.81)\]</br>ensemble \[[33](/reference.md#ref.33), [42](/reference.md#ref.42)\]</br>GAN \[[62](/reference.md#ref.62), [93](/reference.md#ref.93), [94](/reference.md#ref.94)\], [95](/reference.md#ref.95)\]</br>boosting \[[48](/reference.md#ref.48)\]</br>regression \[[25](/reference.md#ref.25), [96](/reference.md#ref.96), [82](/reference.md#ref.82), [43](/reference.md#ref.43), [48](/reference.md#ref.48), [62](/reference.md#ref.62), [97](/reference.md#ref.97), [98](/reference.md#ref.98)\]</br>MLP \[[99](/reference.md#ref.99), [42](/reference.md#ref.42), [100](/reference.md#ref.100)\]</br>random forest \[[61](/reference.md#ref.61), [45](/reference.md#ref.45), [48](/reference.md#ref.48), [97](/reference.md#ref.97)\]</br>RNN \[[32](/reference.md#ref.32), [61](/reference.md#ref.61), [47](/reference.md#ref.47), [88](/reference.md#ref.88), [50](/reference.md#ref.50), [66](/reference.md#ref.66), [92](/reference.md#ref.92), [60](/reference.md#ref.60)\]</br>SVM \[[61](/reference.md#ref.61), [48](/reference.md#ref.48), [62](/reference.md#ref.62), [101](/reference.md#ref.101)\] | anomaly detection \[[102](/reference.md#ref.102), [85](/reference.md#ref.85)\]</br>change detection \[[41](/reference.md#ref.41), [103](/reference.md#ref.103), [62](/reference.md#ref.62), [69](/reference.md#ref.69), [71](/reference.md#ref.71), [104](/reference.md#ref.104), [105](/reference.md#ref.105)\]</br>classification \[[36](/reference.md#ref.36), [40](/reference.md#ref.40), [42](/reference.md#ref.42), [82](/reference.md#ref.82), [106](/reference.md#ref.106), [103](/reference.md#ref.103), [44](/reference.md#ref.44), [45](/reference.md#ref.45), [47](/reference.md#ref.47), [27](/reference.md#ref.27), [65](/reference.md#ref.65), [52](/reference.md#ref.52), [91](/reference.md#ref.91), [77](/reference.md#ref.77), [75](/reference.md#ref.75)\]</br>data assimilation \[[96](/reference.md#ref.96), [82](/reference.md#ref.82), [88](/reference.md#ref.88), [107](/reference.md#ref.107), [108](/reference.md#ref.108)\]</br>enhancement / infilling / image translation \[[103](/reference.md#ref.103), [66](/reference.md#ref.66), [109](/reference.md#ref.109), [110](/reference.md#ref.110), [57](/reference.md#ref.57), [93](/reference.md#ref.93), [94](/reference.md#ref.94), [98](/reference.md#ref.98), [95](/reference.md#ref.95)\]</br>object detection \[[39](/reference.md#ref.39), [106](/reference.md#ref.106), [103](/reference.md#ref.103), [50](/reference.md#ref.50), [101](/reference.md#ref.101)\]</br>registration / image matching \[[111](/reference.md#ref.111), [112](/reference.md#ref.112)\]</br>regression / forecasting \[[99](/reference.md#ref.99), [25](/reference.md#ref.25), [82](/reference.md#ref.82), [43](/reference.md#ref.43), [48](/reference.md#ref.48), [107](/reference.md#ref.107), [49](/reference.md#ref.49), [64](/reference.md#ref.64), [100](/reference.md#ref.100), [92](/reference.md#ref.92), [113](/reference.md#ref.113), [97](/reference.md#ref.97), [35](/reference.md#ref.35), [74](/reference.md#ref.64)\]</br>search / mining \[[36](/reference.md#ref.36), [103](/reference.md#ref.103), [114](/reference.md#ref.114), [107](/reference.md#ref.107), [108](/reference.md#ref.108), [115](/reference.md#ref.115), [87](/reference.md#ref.87)\]</br>segmentation \[[36](/reference.md#ref.36), [37](/reference.md#ref.37), [39](/reference.md#ref.39), [76](/reference.md#ref.76), [40](/reference.md#ref.40), [42](/reference.md#ref.42), [82](/reference.md#ref.82), [44](/reference.md#ref.44), [116](/reference.md#ref.116), [50](/reference.md#ref.50), [90](/reference.md#ref.90), [117](/reference.md#ref.117), [57](/reference.md#ref.57), [60](/reference.md#ref.60)\]</br>sensor fusion \[[41](/reference.md#ref.41), [42](/reference.md#ref.42), [82](/reference.md#ref.82), [103](/reference.md#ref.103), [88](/reference.md#ref.88), [26](/reference.md#ref.26), [108](/reference.md#ref.108), [52](/reference.md#ref.52), [113](/reference.md#ref.113), [80](/reference.md#ref.80), [81](/reference.md#ref.81), [118](/reference.md#ref.118)\]</br>surrogate modelling \[[99](/reference.md#ref.99), [96](/reference.md#ref.96), [108](/reference.md#ref.108), [35](/reference.md#ref.35)\]</br>transfer learning \[[82](/reference.md#ref.82), [43](/reference.md#ref.43), [50](/reference.md#ref.50), [91](/reference.md#ref.91)\]</br>unsupervised learning \[[115](/reference.md#ref.115), [53](/reference.md#ref.53), [59](/reference.md#ref.59)\] | agriculture \[[25](/reference.md#ref.25), [42](/reference.md#ref.42), [119](/reference.md#ref.119), [120](/reference.md#ref.120), [82](/reference.md#ref.82), [43](/reference.md#ref.43), [46](/reference.md#ref.46), [63](/reference.md#ref.63), [121](/reference.md#ref.121), [100](/reference.md#ref.100), [52](/reference.md#ref.52), [113](/reference.md#ref.113), [97](/reference.md#ref.97), [29](/reference.md#ref.29), [30](/reference.md#ref.30)\]</br>climate  \[[99](/reference.md#ref.99), [122](/reference.md#ref.122), [88](/reference.md#ref.88), [48](/reference.md#ref.48), [63](/reference.md#ref.63), [49](/reference.md#ref.49), [53](/reference.md#ref.53), [92](/reference.md#ref.92)\]</br>earth / geo science \[[99](/reference.md#ref.99), [96](/reference.md#ref.96), [82](/reference.md#ref.82), [88](/reference.md#ref.88), [63](/reference.md#ref.63), [107](/reference.md#ref.107), [123](/reference.md#ref.123), [108](/reference.md#ref.108), [31](/reference.md#ref.31)\]</br>energy \[[36](/reference.md#ref.36), [33](/reference.md#ref.33), [82](/reference.md#ref.82), [74](/reference.md#ref.74)\]</br>environmental science \[[82](/reference.md#ref.82), [61](/reference.md#ref.61), [34](/reference.md#ref.34)\]</br>epidemiology \[[51](/reference.md#ref.51)\]</br>finance / insurance \[[58](/reference.md#ref.58), [124](/reference.md#ref.124)\]</br>ship / aircraft awareness \[[39](/reference.md#ref.39), [65](/reference.md#ref.65), [73](/reference.md#ref.73), [75](/reference.md#ref.75)\]</br>geology  \[[86](/reference.md#ref.86), [119](/reference.md#ref.119), [63](/reference.md#ref.63), [69](/reference.md#ref.69), [71](/reference.md#ref.71), [54](/reference.md#ref.54), [56](/reference.md#ref.56)\]</br>hydrology / hydrography \[[32](/reference.md#ref.32), [38](/reference.md#ref.38), [82](/reference.md#ref.82), [46](/reference.md#ref.46), [64](/reference.md#ref.64), [54](/reference.md#ref.54)\]</br>infrastructure / development \[[36](/reference.md#ref.36), [37](/reference.md#ref.37), [40](/reference.md#ref.40), [49](/reference.md#ref.49), [102](/reference.md#ref.102), [69](/reference.md#ref.69), [70](/reference.md#ref.70)\]</br>LULC / forestry \[[42](/reference.md#ref.42), [82](/reference.md#ref.82), [106](/reference.md#ref.102), [103](/reference.md#ref.103), [61](/reference.md#ref.61), [47](/reference.md#ref.47), [62](/reference.md#ref.62), [27](/reference.md#ref.27)\]</br>livestock \[[125](/reference.md#ref.125)\]</br>maritime \[[45](/reference.md#ref.45), [65](/reference.md#ref.65), [55](/reference.md#ref.55), [75](/reference.md#ref.75)\] |

**Table 3.2-1**: From sensing to application. A breakdown of work in AI4EO in terms of the type of sensor employed, modelling approach, prediction task, and application domain.

|  **task** | attention / transformer | CNN | RNN | GAN | MLP | random forest | regression | SVM | Bayesian / probabilistic |
| ----- | ----: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | ----: |
| **change detection**</br>anomaly, LULC |  | \[[82](/reference.md#ref.82), [62](/reference.md#ref.62),[85](/reference.md#ref.85)\] |  |  |  |  | \[[62](/reference.md#ref.62)\] | \[[62](/reference.md#ref.62)\]  |  |
| **classification**</br>building, damage, vehicle, hazard, scene, LULC, crop | \[[52](/reference.md#ref.52), [81](/reference.md#ref.81)\] | \[[40](/reference.md#ref.40), [42](/reference.md#ref.42), [82](/reference.md#ref.82), [45](/reference.md#ref.45), [62](/reference.md#ref.62), [65](/reference.md#ref.65), [52](/reference.md#ref.52), [91](/reference.md#ref.91), [77](/reference.md#ref.77), [28](/reference.md#ref.28)\] | \[[61](/reference.md#ref.61), [47](/reference.md#ref.47)\] |  | \[[42](/reference.md#ref.42)\] | \[[61](/reference.md#ref.61), [45](/reference.md#ref.45)\] | \[[82](/reference.md#ref.82)\] | \[[61](/reference.md#ref.61)\] |  |
| **search / mining**</br>question answering, relational reasoning, image search | \[[87](/reference.md#ref.87)\]   |  |  |  |  |  |  |  |  |
| **Image translation**</br>inpainting, infilling, super-resolution, pansharpening, deblurring, denoising, synthetic generation | \[[68](/reference.md#ref.68)\] | \[[68](/reference.md#ref.68)\] | \[[66](/reference.md#ref.66)\] | \[[93](/reference.md#ref.93), [94](/reference.md#ref.94), [95](/reference.md#ref.95)\] |  |  | \[[98](/reference.md#ref.98)\] |  |  |
| **fusion**</br>cross-calibration, harmonisation, optical \+ optical, optical \+ lidar,  optical \+ SAR | \[[52](/reference.md#ref.52), [81](/reference.md#ref.81)\] | \[[42](/reference.md#ref.42), [48](/reference.md#ref.48), [52](/reference.md#ref.52), [77](/reference.md#ref.77), [54](/reference.md#ref.54), [81](/reference.md#ref.81), [118](/reference.md#ref.118),\] | \[[32](/reference.md#ref.32), [88](/reference.md#ref.88)\] |  | \[[42](/reference.md#ref.42)\] |   |  |  | \[[32](/reference.md#ref.32)\] |
| **object detection / counting**</br>Infrastructure, vehicle, cattle |  | \[[50](/reference.md#ref.50), [89](/reference.md#ref.89)\] | \[[50](/reference.md#ref.50)\] |  |  |  |  | \[[101](/reference.md#ref.101)\] |  |
| **registration /  image matching***</br>video stabilisation, 3D reconstruction, orthorectification |  | \[[111](/reference.md#ref.111), [112](/reference.md#ref.112)\] |  |  |  |  | \[[111](/reference.md#ref.ayi2r4cfons6), [112](/reference.md#ref.2elsyncvizn6)\] |  |  |
| **regression / forecasting**</br>water volume, precipitation, temperature, velocimetry, utilisation, biomass, moisture, wind power |  |  | \[[32](/reference.md#ref.32), [82](/reference.md#ref.82)\] |  | \[[99](/reference.md#ref.99), [100](/reference.md#ref.100)\] | \[[48](/reference.md#ref.48), [97](/reference.md#ref.97)\] | \[[25](/reference.md#ref.25), [43](/reference.md#ref.43), [48](/reference.md#ref.48), [82](/reference.md#ref.82)\] | \[[48](/reference.md#ref.48), [97](/reference.md#ref.97)\] | \[[32](/reference.md#ref.32), [33](/reference.md#ref.33)\] |
| **segmentation**</br>cloud / shadow, vegetation, building, oil slick, LULC, water, rock, road, crop | \[[86](/reference.md#ref.86)\] | \[[39](/reference.md#ref.39), [76](/reference.md#ref.76), [40](/reference.md#ref.40), [42](/reference.md#ref.42), [82](/reference.md#ref.82), [50](/reference.md#ref.50), [89](/reference.md#ref.89), [90](/reference.md#ref.90), [54](/reference.md#ref.54)\] | \[[50](/reference.md#ref.50), [60](/reference.md#ref.60)\] |  | \[[42](/reference.md#ref.42)\] |  | \[[82](/reference.md#ref.82)\] |  |  |
| **transfer learning**</br>self-supervised, semi-supervised, zero/few-shot learning, domain adaptation |  | \[[91](/reference.md#ref.91), [59](/reference.md#ref.59)\] | \[[50](/reference.md#ref.50)\] |  |  |  |  |  |  |

**Table 3.2-2**: Tasks and models. Selected works in AI4EO grouped by task and modelling approach. 



***

***

## 3.3. The future of AI4EO research<a id='3.3'></a> 

The following is a curated but not comprehensive list of promising research directions, aimed at prospective researchers about to enter the field of AI4EO.

**Uncertainty** — Quantifying uncertainty in computer vision applications can be largely divided into regression settings such as depth regression, and classification settings such as semantic segmentation. Deep learning methods cannot however represent uncertainty in an interpretable manner. Vanilla deep learning models do not allow for uncertainty representation in regression settings for example, and deep learning classification models often output softmax probability vectors, but their predictive uncertainty can be miss-calibrated when the related features are rare. For both settings, uncertainty can be better calibrated  with Bayesian deep learning approaches, which offer a systematic and principled framework for modelling uncertainty \[[126](/reference.md#ref.126)\].

**AI explainability** — During the last decade ML has proven to be extremely successful in a variety of different problems \[[119](/reference.md#ref.119)\], yet it is often used as a black box that does not provide us with any insight besides the final outcome \[[96](/reference.md#ref.96)\]. Given that, the EO community has been reluctant to abandon traditional approaches and adopt ML in all those critical areas that require transparency and trust, such as the Earth sciences. In order to overcome these limitations, recently there has been a great interest in developing methods for explainable AI (**xAI**) \[[127](/reference.md#ref.127)\]. The main goal of this research direction is to increase the understanding of ML models without sacrificing their remarkable predictive power. To this end, several post-hoc model-agnostic explanation methods, that enrich DL and shed some light on how decisions are taken, have been developed \[[128](/reference.md#ref.128)\].

### 3.3.1. Quality of data products

On the quality of data products derived from ML models, it is fair to revisit conventional approaches of measuring correctness in supervised settings; to question our confidence in a product’s closeness-to-reality. Often, the latter is compromised by a generative model’s lack of attention to detail, or excessive creativity:

* **Uncertainty maps** \[[129](/reference.md#ref.129)\] — a type of saliency map to visualise what the model does not know. Uncertainty maps should be a standard component of the metadata accompanying a synthetic product, like those produced by fusion and **image-translation** models, like **super-resolution**. Disclosing the margins or errors in the data values would provide transparency and increase the trust by users of analysis-ready products. An exemplary map is displayed in Figure 12\. 


* **Perceptual metrics** \[[130](/reference.md#ref.130), [131](/reference.md#ref.131)\] have been traditionally applied on the image-translated products, like in **super-resolution** and **pansharpening**. Alternative approaches may consider saliency, which is deeply rooted on the broad concepts of information and uncertainty. While saliency criteria can be also founded on solid perceptual criteria, a purely statistical approach allows to scrutinise not only the output product but the inner layers in neural networks.

* **Distortions and hallucinations** that result from image translation tasks should be evaluated at the model level, either by looking at the internal latent feature representations, studying the effect of convolutional filters, how and when they activate under different stimuli \[[132](/reference.md#ref.132)\].

* **Losses for image-to-image translation tasks** — Existing work in image tasks uses predominantly pixel-based (MSE, MAE, SSIM), kernel-based (KSSIM), perceptual (learned filter-based comparison), adversarial (discriminator \+ generator minimax game). Research opportunity: losses that operate in Fourier and wavelet domains.

![An example of uncertainty map for a CNN-based land cover classification task](/figures/Figure3.3.1-1.png)  
**Figure 3.3.1-1**: An example of uncertainty map for a CNN-based land cover classification task. From left to right: aerial optical image, its ground truth, the CNN-predicted land cover classes and the uncertainty map. The uncertainties of the predictions are highest at the edges of classes (lighter colour) and lowest at the core of each class type. Source: \[[133](/reference.md#ref.133)\].

### 3.3.2. Harmonisation

In section [**7.2. Data for AI/ML data interoperability**](#7.1.-data-for-ai/ml-data-interoperability) we discussed the main challenges of ML-based harmonisation. Recent advances in Deep Learning architectures imply further room for progress:

* **Attention over time** — Current attention-based architectures attend only on pixels or patches, like the visual Transformer with multiple self-attention heads at the level of tiled patches \[[134](/reference.md#ref.134)\]. There is an opportunity to design an attention over time, for datacubes that involve time-series of satellite revisits.

* **Generative-based harmonisation** — Opportunity to use generative models, like Conditional GANs, to  realistically generate missing modalities \[[95](/reference.md#ref.95)\] or to infill missing data, for example due to cloud coverage.

* **Spatial co-registration of products** — End-to-end spatial co-registration during sensor fusion. Satellite inclinations are naturally modelled by projective / homography transformations \[[135](/reference.md#ref.135)\].

* **Spectral registration of optical products** — As of yet, the spectral bands of a pixel are not treated as a longitudinal data series, by which each band is represented by both its reflectance value and its wavelength interval. Instead, only the reflectance value is used, as in most cases all of the training data come from the same sensor, so there is no need to keep track of the exact wavelength intervals of each band. The need for a longitudinal spectral analysis arises in cross-instrumental studies (e.g. sensor-to-sensor mapping, sensor fusion). One way to achieve this could be through “band-positional” encodings that capture correlations of partially overlapping bands between different instruments. The idea is inspired by the (spatial) positional encodings used in the visual Transformer.

### 3.3.3. AI safety

“Technology is an amplifier of human intent” \[[136](/reference.md#ref.136)\]. The point of this quote is not that technology is inherently neutral; it is not because tech cannot exist in isolation from civilization. Therefore, one would be amiss to think that AI will ‘do no evil’ [^5]. Bias is a key ingredient of our ability to learn, therefore AI systems too are inherently biassed. These vulnerabilities can be exploited to concentrate power, or to fool and attack AI-based infrastructure systems.

* **Robustness to adversarial inputs** — Our increasing reliance on EO data will eventually necessitate their safeguarding from malicious signals on the ground. This type of interference is a real concern for situational awareness applications involving InSAR \[[137](/reference.md#ref.137)\].

* **Privacy and ethics** — Indigenous tribes in the Amazon rainforest; villages in rural parts of Darfur, Western Sudan; migrants fleeing violence —are all examples of vulnerable populations that can be compromised en masse through the wrong use of a data API. This problem is actually best addressed not by AI, but with the instilling of ethical practices in school and university curricula. That being said, AI can in fact help, through the systematic collection evidence for acts against humanity [^6]. But it can also help to deliberately obfuscate the sensitive information of such communities, like geolocation data and visual indicators of activity in rural regions.

* **Onboard-ML** can also play a role here, through the development of lightweight ML models that can be installed directly on the hardware of satellites, and help with the prefiltering of sensitive data, prior to transmitting them to the Earth \[[138](/reference.md#ref.138)\].

[^5]: [Artificial intelligence is creating a new colonial world order | MIT Technology Review](https://www.technologyreview.com/2022/04/19/1049592/artificial-intelligence-colonialism/)
[^6]: [Using AI to scale up human rights research: a case study on Darfur – Citizen Evidence Lab](https://citizenevidence.org/2020/07/06/using-artificial-intelligence-to-scale-up-human-rights-research-a-case-study-on-darfur/)

***

***
## 3.4. MLOps Life cycle and tasks<a id='3.4'></a> 

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


## 3.5. AI/ML Tasks and use cases<a id='3.5'></a> 

The table introduces common AI/ML tasks and the representative models used for them.

Table 3.5-1 AI/ML tasks and use cases

| Task | Abstract | Use case | Methods, models |
| :---- | :---- | :---- | :---- |
| **Classification** | Assigns each pixel or object to a specific class (e.g., forest, water, urban) | Land use/land cover classification (LULC), crop type mapping | Random Forest, SVM, CNN, ResNet, Transformer |
| **Segmentation** | Pixel-level labeling to divide an image into semantic regions | Building extraction, road mapping, flood extent detection | U-Net, DeepLab, SegNet, Mask R-CNN |
| **Object Detection** | Identifies specific objects (e.g., buildings, vehicles) using bounding boxes | Urban monitoring, infrastructure analysis, disaster damage mapping | YOLO, Faster R-CNN, RetinaNet |
| **Change Detection** | Detects changes between images taken at different times | Deforestation monitoring, urban growth, disaster impact assessment | Siamese Network, FC-EF, CVAE, STANet |
| **Anormaly Detection** | Identifies unusual or unexpected patterns in imagery | Early warning of wildfires, oil spills, glacier melting | AutoEncoder, Isolation Forest, GAN |
| **Super-resolution** | Enhances low-resolution images to higher resolution | Precision monitoring, SAR image enhancement | SRGAN, ESRGAN, SwinIR |
| **Time Series Analysis** | Analyzes temporal patterns of a location over time | Crop monitoring, drought detection, surface temperature trends | LSTM, TCN, Tfansformer, EarthNet |
| **Spatial Modeling** | Predicts or interpolates spatial distributions | Soil moisture, PM2.5 estimation, rainfall mapping | Kriging+ML, GCN, GeoAI |
| **Data Fusion** | Integrates data from different sensors or resolutions | Multi-sensor analysis (e.g., optical \+ SAR) | CNN+LSTM, Transformer Fusion, DANN |



***

[Previous](README.md) | [Table of contents](/README.md) | [Next](venues-of-cross-disciplinary-research.md)
