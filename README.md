# FAIR Docker with Jupyter Notebook, NHANES data and statistical analysis using R

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2248123.svg)](https://doi.org/10.5281/zenodo.2248123) [![](https://images.microbadger.com/badges/version/dbmi/fair_jupyter_r_nhanes.svg)](https://microbadger.com/images/dbmi/fair_jupyter_r_nhanes "Get your own version badge on microbadger.com")

The built Docker image has been archived individually on Zenodo since Docker Hub does not guarantee preservation by allowing tagged images to be overwritten easily.  The DOI for the Docker image is 

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1933605.svg)](https://doi.org/10.5281/zenodo.1933605)

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/hms-dbmi/Reproducible_FAIR_NHANES/master)

## What is the purpose of this repository ?

This GitHub repository serves as an illustration of our way to create a reproducible and F.A.I.R (findable, accessible, interoperable, reusable) statistical analysis and is associated with an article whose reference will be added soon in this section. Both reproducibility and “fairness” concepts are relevant and complementary. They promote a more open, discoverable and credible science. For this reason, they should ideally be strived for by any researchers.

The analysis presented in the Jupyter notebook (ipynb file) is performed on public National Health and Nutrition Examination Survey (NHANES) data collected between 1999 and 2006. The `NHANES_extracted.csv` dataset on which the analysis is performed on, was extracted from the whole NHANES dataset corresponding to this period. This large dataset is archived and can be found on dryad digital repository at http://dx.doi.org/10.5061/dryad.d5h62. Steps leading to the creation of the extracted dataset are displayed in the notebook.

A Docker Compose file is included to specify creation of a reproducible container environment. It includes all the  packages and system tools requried to rerun the statistical analysis described above and contained in the Jupyter notebook.  To launch this environment install Docker and Docker Compose, clone this repo and then run the following command from within the directory

`docker-compose up` 

_More information on CDC NHANES [here](https://www.cdc.gov/nchs/nhanes/index.htm)._


## Mybinder

`install.R` and `runtime.txt` files are additionnal files enabling the creation of a Mybinder environement in the cloud with a Jupyter using R. You can then execute the code by clicking this button : [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/hms-dbmi/Reproducible_FAIR_NHANES/master) and share it via this link https://mybinder.org/v2/gh/hms-dbmi/Reproducible_FAIR_NHANES/master 

(_The loading of the page might take up to ten minutes._ )

If you prefer executing the code locally, you can either use the R script or the ipynb file provided in the repo.

More information about the reproducibility aspects are provided in the article that will be soon associated with this repository.

### Resources on F.A.I.R guidelines

 [The FAIR Guiding Principles for scientific data management and stewardship](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4792175/)

 [FORCE11](https://www.force11.org/fairprinciples) 
 
 [FAIR-TLC](https://zenodo.org/record/203295#.W3HO8rjZAe0) 
 
 [FAIRMetrics](https://github.com/FAIRMetrics/Metrics) 
 
 [DTLS](https://www.dtls.nl/fair-data/fair-principles-explained) 

## License

Apache 2 license

Please cite this repository as:

Dan Traviglia, Jason Stedman, & Norah Anthony. (2018, December 13). hms-dbmi/fair_docker_jupyter: Docker Compose (Version v0.1.1). Zenodo. http://doi.org/10.5281/zenodo.2248123
