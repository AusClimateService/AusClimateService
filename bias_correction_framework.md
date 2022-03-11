# Bias Correction Methods and Considerations for ACS Downscaled Data

## Working Group on Bias Correction for ACS
**Lead:** Justin Peter?  
**Members:**  
Ulrike Bende-Michl  
Chloe Mackallah  
Raktima Dey  
...

---
## Methods

### QME (BoM)
Quantile matching for Extremes.  
Dowdy, A., 2019. Towards seamless predictions across scales for fire weather. Proceedings for the 6th International Fire Behavior and Fuels Conference, International Association of Wildland Fire, Missoula, Montana, USA.
http://albuquerque.firebehaviorandfuelsconference.com/wp-content/uploads/sites/13/2019/04/Dowdy-Sydney.pdf

### MRNBC (UNSW)
Multivariate Nested Bias Correction
Johnson, F., and Sharma, A. (2012), A nesting model for bias correction of variability at multiple time scales in general circulation model precipitation simulations, Water Resour. Res., 48, W01504.  
https://doi.org/10.1029/2011WR010464  

Strengths:  
Weaknesses:  
Other notes:  

#### MRQNBC
Multivariate Quantile-Matching Bias Correction
R. Mehrotra and A. Sharma, 2016. A Multivariate Quantile-Matching Bias Correction Approach with Auto- and Cross-Dependence across Multiple Time Scales: Implications for Downscaling.  
https://doi.org/10.1175/JCLI-D-15-0356.1  
https://doi.org/10.1016/j.envsoft.2018.02.010 (software)

### ISIMIP (Potsdam)
Inter-Sectoral Impact Model Intercomparison Project.  
S. Hempel, K. Frieler, L. Warszawski, J. Schewe, and F. Piontek, 2013. A trend-preserving bias correction – the ISI-MIP approach. Earth Syst. Dynam., 4, 219–236, 2013. Journal of Climate, 29(10), 3519-3539. 
https://doi.org/10.5194/esd-4-219-2013

Strengths:  
Weaknesses:  
Other notes:  

#### ISIMIP2b
Frieler et al., 2017. Assessing the impacts of 1.5 °C global warming – simulation protocol of the Inter-Sectoral Impact Model Intercomparison Project (ISIMIP2b). Geosci. Model Dev., 10, 4321–4345, 2017.  
https://doi.org/10.5194/gmd-10-4321-2017

#### ISIMIP3
Lange, S., 2019. Trend-preserving bias adjustment and statistical downscaling with ISIMIP3BASD (v1.0). Geosci. Model Dev., 12, 3055–3070, 2019.  
https://doi.org/10.5194/gmd-12-3055-2019

### QQ-scaling (CSIRO)
Shao, Q., Li, M. An improved statistical analogue downscaling procedure for seasonal precipitation forecast. Stoch Environ Res Risk Assess 27, 819–830 (2013).  
https://doi.org/10.1007/s00477-012-0610-0

Strengths:  
Weaknesses:  
Other notes:  

---
## Observational / reanalysis datasets to use for bias correction

### AGCD / AWAP
For precipitation.  
5km reolution for older version; 1km resolution for new version?  
Australian Bureau of Meteorology (2020), "Australian Gridded Climate Data ( AGCD ) / AWAP ; v1.0.0 Snapshot (1900-01-01 to 2020-06-30)".  
https://doi.org/10.4227/166/5a8647d1c23e0

### ERA5
For winds/temp?  
30km resolution.  
Hersbach, H, Bell, B, Berrisford, P, et al. The ERA5 global reanalysis. Q J R Meteorol Soc. 2020; 146: 1999– 2049.  
https://doi.org/10.1002/qj.3803
https://confluence.ecmwf.int/display/CKB/ERA5%3A+data+documentation

#### ERA5.1
2000-2006 update due to stratospheric biases.  
Simons, A., 2010. Global stratospheric temperature bias and other stratospheric aspects of ERA5 and ERA5.1. ECMWF Technical Memoranda 859.
http://dx.doi.org/10.21957/rcxqfmg0

### BARRA (v1/2?)
For winds/temp?  
12km resolution.  
Su, C.-H., Eizenberg, N., Steinle, P., Jakob, D., Fox-Hughes, P., White, C. J., Rennie, S., Franklin, C., Dharssi, I., and Zhu, H.: BARRA v1.0: the Bureau of Meteorology Atmospheric high-resolution Regional Reanalysis for Australia, Geosci. Model Dev., 12, 2049–2068, https://doi.org/10.5194/gmd-12-2049-2019, 2019.  
https://doi.org/10.5194/gmd-12-2049-2019


---
## Technical Considerations

### Resolution at which to perform bias correction
Options:
- BC at resolution of observation / reanalysis
- BC at resolution of climate model (GCM / RCM)
- BC at resolution of most coarse-scale dataset
- BC at resolution of most fine-scale dataset

### Regridding 
Options:
- Conservating remapping
- Bilinear interpolation
