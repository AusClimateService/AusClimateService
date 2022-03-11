# ACS Data Hierarchy
A hierarchy of data levels, defined according to the amount of processing / transformation that has been applied to the climate model output data.

### Level 0a
This defines data written directly by and during the model simulation, within the modelling suites.  

- Does not typically contain publication-level metadata.
- Each file generally contains many different parameters across multiple valid times.
- UM fieldsfile format (for UM-based models).
- To be archived on tape.

### Level 0b
This defines data that has undergone variable separation and timeseries concatenation. 

- Does not typically contain publication-level metadata.
- One file per parameter across multiple valid times.
- netCDF format.
- To be placed on disk for further post-processing, and deleted from disk after conversion to Level 1.

### Level 1a
This defines data that has undergone 'CMORisation' or similar data transformation. 

- Parameters are not significantly tranformed, with only cleaning / masking applied where needed.
- Must contain publication-level metadata.
- Follows (ACS Data Standards)[https://github.com/AusClimateService/data-code-group/blob/main/data_standards.md] and ACS Data Request (in progress).
- One file per parameter across multiple valid times.
- netCDF format.
- To be shared through ia39 on Gadi (and published where appropriate).

### Level 1b
This defines data that has undergone 'CMORisation' or similar data transformation. 

- Parameters have been significantly tranformed such as averaging, unit conversion, etc.
- Must contain publication-level metadata.
- Follows (ACS Data Standards)[https://github.com/AusClimateService/data-code-group/blob/main/data_standards.md] and ACS Data Request (in progress).
- To be prescribed by the (ACS Data and Code Group)[https://github.com/AusClimateService/data-code-group].
- One file per parameter across multiple valid times.
- netCDF format.
- To be shared through ia39 on Gadi (and published where appropriate).

### Level 2
This defines data that has been bias corrected (according to the [Bias Correction Framework](bias_correction_framework.md)).

- Must contain publication-level metadata.  
- Follows (ACS Data Standards)[https://github.com/AusClimateService/data-code-group/blob/main/data_standards.md] and ACS Data Request (in progress).  
- To be prescribed by the Working Group on Bias Correction for ACS.  
- One file per parameter across multiple valid times.  
- netCDF format.  
- To be shared through ia39 on Gadi (and published where appropriate).  

### Level 3?
This defines derived evaluation metrics, including added value statistics.

- Must contain publication-level metadata.
- Follows (ACS Data Standards)[https://github.com/AusClimateService/data-code-group/blob/main/data_standards.md] and ACS Evaluation Metrics Request (in progress).
- To be prescribed by the Working Group on Evaluation for ACS.
- netCDF or csv format.
- To be shared through ia39 on Gadi (and published where appropriate).

### Level 4?
This defines derived hazard indicators, such as extreme value statistics (AEP, EVA), climatologies, multi-model ensemble statistics or products, etc.

- Must contain publication-level metadata.
- Follows (ACS Data Standards)[https://github.com/AusClimateService/data-code-group/blob/main/data_standards.md] (in progress).
- To be prescribed by WP4.
- netCDF or csv format.
- To be shared through ia39 on Gadi (and published where appropriate).
