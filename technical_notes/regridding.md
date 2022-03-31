# Australian Climate Service (ACS) – technical note

## Re-gridding of gridded datasets

**Relevance:** gridded observed datasets, reanalyses, climate model outputs (weather, seasonal, decadal and projections models)

**Example uses:**

1. To align the grid from a climate model output to the grid from another model or models – e.g., examine data from CMIP6 models on a common grid

2. To align the grid from models to an observed dataset, e.g., to examine output from CCAM or BARPA on the AGCD grid

**Scope:**
this note refers to regridding, not to statistical downscaling or modelling

**Important information and literature review:**
The range of considerations and best practice differs between regridding to a similar or larger grid spacing, or to a smaller grid spacing. Relevant points from the literature include…XXXX

**Supported methods:**

1. Re-gridding to finer resolution: **Bilinear interpolation.**  
This produces a smoother surface so avoids sharp jumps when using to apply to finer scale gridded data.
   1. Cautions and caveats: must be made clear that this doesn’t produce new information at finer scale, it is simply interpolation of coarser information. Must be made clear that the method may mean that this disrupts the dynamical balance of a model (e.g., budget closures) for the sake of more realistic looking surface.
   2. Notes on applicability to hazards: anything here? (thinking of things like: can create artefacts when the regridded data is used in GEV or FFDI analysis?)
   3. Technical details and python function: TBC

2. Re-gridding to similar/coarser resolution: **Conservative remapping.**  
This retains the maximum information from the original data and doesn’t have to deal with the issue of creating a realistic looking surface.
    1. Cautions and caveats: TBC
    2. Notes on applicability to hazards: TBC
    3. Technical details and python function: TBC
