[Previous](disaster.md) | [Table of contents](/README.md) | [Next](precipitation.md)

***

## 5.3. Infrastructure Monitoring

**GOAL:** EO for infrastructure management are relatively novel, with emerging applications that integrate satellite-based Synthetic Aperture Radar Interferometry (InSAR) with civil engineering modelling and ground instrumentation for structures such as bridges (e.g. [Selvakumaran et al. (2018)](https://www.sciencedirect.com/science/article/pii/S0303243418303052), [Cusson et al. (2020)](https://link.springer.com/article/10.1007/s13349-020-00446-9)) and mine tailings (e.g. [Bayaraa et al. (2024)](https://www.emerald.com/jgeot/article-abstract/74/10/985/1213047/InSAR-and-numerical-modelling-for-tailings-dam?redirectedFrom=fulltext)). 

In parallel, deep learning approaches have been applied to detect ground deformation over critical infrastructure such as tunnels or gas / water extraction ([Anantrasirichai et al. (2020)](https://ieeexplore.ieee.org/abstract/document/9181454)) and airports ([Ma et al. (2020)](https://www.tandfonline.com/doi/abs/10.1080/2150704x.2019.1692390)). Of particular importance are mine tailings, where early detection of anomalous deformation may help protect the surrounding communities and the environment from catastrophic failures of toxic mine waste ([Bayaraa et al. (2023)](https://www.mdpi.com/2072-4292/15/20/4910))). 

**AI4EO example:** A variety of data science approaches, from deep learning to shallow machine (e.g. random forest) models and probabilistic models such as gaussian process regression have shown promise in detecting anomalous deformation signals from InSAR (e.g. [Bayaraa et al. (2023)](https://www.mdpi.com/2072-4292/15/20/4910)). Example is in Figure 5.3-1.  

![Infrastructure Monitoring](/figures/Figure5.3-1.png)  
Figure 5.3-1: Use of machine learning approaches for detecting anomalous deformation signals from satellite InSAR data. (a) InSAR data visualised spatially over the Cadia tailings dam. © ESA Sentinel-2data and ISBAS InSAR data © Terra Motion. (b) Zoom in to the failed area of the dam. Basemap image copyright © 2021 Maxar Technologies, © CNES/Airbus, © Google Earth. (c) An example of an InSAR measurement showing a typical linear deformation with all test measurements within uncertainty envelope of Gaussian Process Regression. (d) An example of anomalous deformation behaviour, with the last four measurements (in blue) falling significantly outside the uncertainty envelope. Modified with permission from [Bayaraa et al. (2023)](https://www.mdpi.com/2072-4292/15/20/4910). 

***

[Previous](disaster.md) | [Table of contents](/README.md) | [Next](precipitation.md)
