# Mobile Phone Data for Disaster Risk Reduction and Resilience

This the code supporting the paper:

**Mobile Phone Data for Disaster Risk Reduction and Resilience**
Francesca Giardini, Natalia Selini Hadjidimitriou, Marco Mamei, Giordano Bastardi, Nico Codeluppi, and Francesca Pancotto
Submitted to Scientific Reports in 2022

Files and data allow to reproduce all the reported experiments


## File content and structure

- **quake_data** contains the main datasets to run the experiments. This fonder contains SHP files with regions' geometry, aggregated mobile phone data, aggregated company (AIDA) data, etc.

- **sisma2016_data** contains datasets about damage assessment and reconstructions. This data is extected from: https://sisma2016data.it


- **mobilephone_analysis.ipnynp** computes the time-series forecasting algorithm discusses in the paper, and computes MPE

- **mobilephone_maps.ipnynp** draws maps with the results of MPE

- **regression_MPE.ipynb** computes the regression described in Table 2 of the paper

- **regression_SISMA2016.ipynb** computes the regression described in Table 3 of the paper

- **aida_analysis.ipynb** and **aida_analysis_norm_by_population** process company data and computes the industrial composition of each municipality. aida_analysis computes industrial composition in terms of the fraction of the total revenue of the sector VS. total overall revenues. The result is in **quake_data/imprese_ateco_wide.csv**. aida_analysis_norm_by_population computes industrial composition in terms of number of companies per sector pro capite. The result is in **quake_data/imprese_ateco_wide_norm_by_pop.csv**.

- **Sisma-analysis.ipynb** analyse data in sisma2016_data and produces the file **quake_data/sisma_all.csv**. This is the file used in the regression *regression_SISMA2016*

- **spatial_autocorrelation.ipynb** performs spatial autocorrelatios analysis (Moran's I)

- **clustering.ipynb** cluster municipalities on the basis of multiple features. This is an alternative analysis reported at the enf of the paper (*Predict variation*)

- **geo_distances_epicenters** and **geo_distances_big_municipalities.ipynb** computes min distances between municipalies and earthquake epicenters and municipalities and "big" cities (population > 20000). They create output files: **quake_data/distance_from_epicenter.csv** and **quake_data/distance_from_big.csv**

- **pre_process_files_2022.ipynb** minor utility file to format some data in sisma2016_data






