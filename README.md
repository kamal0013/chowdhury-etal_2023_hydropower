[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8008401.svg)](https://doi.org/10.5281/zenodo.8008401)

# chowdhury-etal_2023_hydropower

This repository contains Jupyter Notebooks and instructions to reproduce the results of the following paper: 

**Future Hydropower Expansion in Eco-Sensitive River Basins under Global Energy-Economic Change**

AFM Kamal Chowdhury<sup>1\*</sup>, Thomas Wild<sup>2</sup>, Ying Zhang<sup>2</sup>, Matthew Binsted<sup>2</sup>, Gokul Iyer<sup>2</sup>, Son H. Kim<sup>2</sup>, and Jonathan Lamontagne<sup>3</sup>


<sup>1 </sup> Earth System Science Interdisciplinary Center, University of Maryland, College Park, MD 20740, United States

<sup>2 </sup> Joint Global Change Research Institute, Pacific Northwest National Laboratory, College Park, MD 20740, United States

<sup>3 </sup> Department of Civil and Environmental Engineering, Tufts University, Medford, MA 02155, United States


\* corresponding author: kchy@umd.edu

DOI (pre-print): https://doi.org/10.21203/rs.3.rs-3089500/v1


## Summary
In this study, we investigate how rapid economic growth and transition to low-carbon energy may impact hydropower development, with potential countervailing effects of increasingly cost-competitive variable renewable energy (VRE). We explore the effects of these forces on hydropower expansion in the world's 20 most eco-sensitive river basins, that have substantial untapped hydropower potential and ecological richness. Our investigation is based on the [Global Change Analysis Model (GCAM)](https://github.com/JGCRI/gcam-core), an integrated model of global energy-water-economy dynamics. The Jupyter Notebooks provided in this repository, in combination with the GCAM outputs and other data provided in [this Zenodo repository](https://doi.org/10.5281/zenodo.8008401), can be used to conduct our key analysis, and reproduce the relevant results.


## Data
The following data, provided in [this Zenodo repository](https://doi.org/10.5281/zenodo.8008401), will be required to reproduce our results.

| Folder name |   Contents   |
|-------------|-------------|
| other_data | `hydro_fish_stats_by_basins.csv` : Basin-scale untapped hydropower potential, planned hydropower capacity, fish richness, and fish catch. |
|            | `eco_sensitivity_rank_by_basins.csv` : Eco-sensitivity ranks of the global basins, an output file based on our analysis of the above-mentioned four hydropower-fish parameters. |
|            | `L227.SmthRenewRsrcCurves_hydro.csv` : Basin-region-scale exploitable hydropower potential and resource supply curves. |
|            | `basin_shapefile` : Shapefile of the GCAM basin-regions. |
| gcam_outputs | `scenario_names.csv` : Names of the eight scenarios used in this study. |
|              | `scenario_outputs` : GCAM outputs for each scenario that are used in our analysis. These outputs are generated using [GCAM version 5.3](https://github.com/JGCRI/gcam-core/releases/tag/gcam-v5.3) with an endogenous representation of hydropower, as described in [Zhang et al. (2022)](https://iopscience.iop.org/article/10.1088/1748-9326/ac9ac9). The instructions on running GCAM scenarios are available [here](https://github.com/JGCRI/gcam-core). |


## Jupyter Notebooks
The analysis and plotting will require the following Jupyter Notebooks, written in Python 3.8.

- `plot_fig1_selection_of_eco_sensitive_basins.ipynb` : Define eco-sensitivity rank of the global river basins based on four hydropower-fish parameters: untapped hydropower potential, planned hydropower capacity, fish richness, and fish catch. Also, plot the parameters on a scatter plot and identify the world's top 20 eco-sensitive river basins.

- `plot_fig2_overall level_of_hydropower_deployment.ipynb` : Estimate and plot the overall level of hydropower deployment in the world's top 20 eco-sensitive river basins for 2015 and 2050 under eight scenarios.

- `plot_fig3_basin_region_scale_hydropower_deployment.ipynb` : Estimate and plot the basin-region-scale level of hydropower deployment in the world's top 20 eco-sensitive river basins for 2015 and 2050 under eight scenarios.

- `plot_fig4_uncertainty_in_basin_scale_mid_century_deployment.ipynb` : Estimate and plot the min-max range of basin-scale hydropower deployment (as share of exploitable potential) in 2050 across the eight scenarios for the world's top 20 eco-sensitive river basins.


## Reproduce Our Results
Our results can be reproduced in the following steps:

- Install required Python packages, including `geopandas` and `plotly`, preferably in a dedicated virtual environment.

- Download `gcam_outputs` and `other_data` from the Zenodo repository and save them in the `data` folder.

- Run the Jupyter Notebooks to obtain the results as mentioned above.

- In the Notebooks, use `save_outputs = 'yes'` to save the output plots in the `figures` folder.
