[Previous](from-sensing-to-applications.md) | [Table of contents](/README.md) | [Next](mlops-life-cycle-and-tasks.md)

***

## 3.3. The future of AI4EO research

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

[Previous](from-sensing-to-applications.md) | [Table of contents](/README.md) | [Next](mlops-life-cycle-and-tasks.md)
