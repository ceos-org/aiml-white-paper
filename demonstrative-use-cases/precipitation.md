[Previous](infra-monitoring.md) | [Table of contents](/README.md) | [Next](sustainable-finance.md)

***

## 5.4. Precipitation

**GOAL :**
Bias correction of precipitation forecast data from numerical weather prediction (MSM/GPV) by JMA in Japan. Finally aiming at the utilization for hydrological simulation.

**METHOD :**
Assuming a relationship between observed precipitation and the areal precipitation distribution reproduced by numerical weather forecasts, we applied machine learning to correct precipitation bias. Specifically, the target variable was observed precipitation (JMA’s in-situ and ground radar–based observations, Radar-AMeDAS), while the predictor variable was precipitation from the JMA mesoscale numerical forecast model (MSM) 39-hour forecasts. The relationship was trained using data from 2007 to 2020\. Bias correction was then performed by estimating precipitation at the center of the distribution from forecast precipitation distributions not included in training. After correcting the spatial distribution with a support vector machine (SVM), additional quantitative adjustments for precipitation associated with individual convective clouds and squall lines—phenomena that are difficult to capture with machine learning—were made using a statistical method known as cumulative distribution function transform (CDFt).Support vector machine (SVM) regression with quantile-based bias correction For more detail, please refer to (Yin et al., 2022.)  
 [https://doi.org/10.1016/j.jhydrol.2022.128125](https://doi.org/10.1016/j.jhydrol.2022.128125).  
This method is now operationally used in “[Today’s Earth \- Japan](https://www.eorc.jaxa.jp/water/index.html)”, which is terrestrial hydrological simulation system for Japan, developed  by Japan Aerospace Exploration Agency (JAXA) and the University of Tokyo (see the [document](https://www.eorc.jaxa.jp/water/documents/TodaysEarth_20240702_e.pdf) for more detailes).

![Averaged hourly precipitation in January](/figures/Figure5.4-1.png)  
Figure 5.4-1: Averaged hourly precipitation in January from (a) Radar-AMeDAS, (b) MSM-GPV, (c) QM, and (d) CDFt, (e) SVM, (f) SVM-QM, and (g) SVM-CDFt. The  statistical metrics evaluated against Radar-AMeDAS were shown in each subplot, and the units for R, RMSE, and bias are unitless, mm/hr, and mm/hr, respectively. Modified with permission from [Yin et al., 2022](https://doi.org/10.1016/j.jhydrol.2022.128125)

***

[Previous](infra-monitoring.md) | [Table of contents](/README.md) | [Next](sustainable-finance.md)
