[Previous](README.md) | [Table of contents](/README.md) | [Next](disaster.md)

***

## 5.1. Climate

### 5.1.1. Mapping glacier grounding lines {#5.1.1.-mapping-glacier-grounding-lines}

**GOAL:**
AI/ML are becoming integral to climate science, offering new methods to analyze the vast and complex datasets produced by satellites, in-situ measurements, and climate models. For example,  artificial intelligence can improve monitoring of ice-sheet dynamics by automatically mapping grounding lines, which are the boundary where glaciers transition from grounded ice to floating ice shelves (Mohajerani et al. (2021)). Accurate delineation of these lines is crucial for understanding ice-sheet stability and sea level rise.

**AI4EO example:**
Mohajerani et al. (2021) applied a deep learning model to Differential Interferometric Synthetic Aperture Radar (DInSAR) data from the Sentinel-1 A/B satellites, training it to recognize grounding line signatures in complex interferometric phase patterns. Unlike traditional manual delineation or threshold-based techniques, the AI approach processes large datasets quickly and consistently, reducing human error and improving efficiency.

The figure below compares grounding lines derived by the deep learning model against those mapped manually. The AI-generated line (black) closely overlaps with the expert-drawn reference (white line), illustrating the accuracy and reliability of the automated approach. This example highlights the potential of AI/ML to scale up glacier and ice-sheet monitoring for climate studies and sea level rise projections.

![Different steps of the pipeline for (a) a sample interferogram with hand-drawn grounding line in white](/figures/Figure5.1.1-1.png)  
Figure 5.1.1-1 Different steps of the pipeline for (a) a sample interferogram with hand-drawn grounding line in white; (b) output of the neural network in raster format with a variable width that is a measure of uncertainty of the output. The gray mask in the background represents training (white) and testing (gray) sites; (c) Vectorized output and uncertainty contours; (d) zoomed-in region highlighted by the maroon box in panel (c) showing both manual and ML results and uncertainty bars; (e) Comparison of the manual and ML performances in the area outlined in blue in panel (c).

### 5.1.2. Thin ice thickness

**GOAL:**
The application of AI/ML in sea ice research has expanded into a wide range of tasks, including the estimation of sea ice concentration, thickness, and drift, classification of ice types, detection of ice edges, leads, and melt ponds, and seasonal forecasting of sea ice distributions. In particular, most studies have focused on these tasks using SAR and optical sensors with high spatial resolution. On the other hand, passive microwave radiometers such as AMSR2 and SSM/I, which can globally observe Earth’s surface regardless of day/night conditions or cloud cover and have long been utilized for climate monitoring, have also seen progress in AI/ML-based applications. One example is the retrieval of thin ice thickness. In winter, coastal polynyas, thin ice regions surrounded by pack ice and coasts, experience substantial heat loss to the atmosphere, resulting in the formation of large amounts of sea ice. The dense water formed in association with this sea ice production partly intrudes into the subsurface, intermediate, and deep oceans and drives the overturning circulation and material cycles such as CO₂. Information on thin ice thickness is therefore indispensable for estimating sea ice production, and many studies have developed thin ice thickness retrieval algorithms. Most of these algorithms rely on deriving simple empirical equations by comparing ice thickness obtained from thermal infrared sensors with microwave radiometer data. Such empirical formulations can be replaced by AI/ML methods with greater representational power, offering the potential for improved accuracy.

**AI4EO example:**
Nakata et al. (in prep.) employed a NN model to estimate thin ice thickness below 20 cm across the entire Antarctic sea ice region. To construct a highly generalizable retrieval model, a large volume of high-quality training data was required. They used a total of \~200,000 training samples, consisting of accurate thin ice thickness and thin/thick ice types derived from MODIS data. As input, instead of directly using AMSR2 L1B brightness temperature data (18, 36, and 89 GHz; spatial resolutions of 20 km, 10 km, and 5 km, respectively), they used corrected brightness temperatures obtained through the following preprocessing steps. First, the radiometer version of the Scatterometer Image Reconstruction (rSIR) method was applied to downscale the data to grid spacings of 10 km, 5 km, and 2.5 km. Second, a unidirectional variation model was used to remove stripe noise. Furthermore, the influence of atmospheric water vapor was corrected using a simplified radiative transfer model. To address thin ice retrieval, they employed a simple three-layer neural network that outputs both thin ice thickness and thin ice probability, trained with a loss function combining mean squared error for regression and binary cross-entropy for thin ice classification. As a result, the retrieved thin ice thickness dataset demonstrated remarkable improvements compared to previous algorithms. As shown in Figure 1, the comparison between a previous algorithm and the AI/ML approach demonstrates that, with appropriate preprocessing and the use of a neural network, thin ice distribution can be represented with higher accuracy and greater detail.

![Thin ice thickness](/figures/Figure5.1.2-1.png)  
Figure 5.1.2-1\. (a) Thin ice area (yellow regions) derived from the previous algorithm. (b) Pseudo-color composite image derived from the AI/ML approach (Red: thin ice probability, 50–100%; Green: thin ice thickness, 20–0 cm).

***

[Previous](README.md) | [Table of contents](/README.md) | [Next](disaster.md)
