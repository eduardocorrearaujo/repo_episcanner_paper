# Code and data of the "Large-scale Epidemiological modeling: Scanning for Mosquito-Borne Diseases Spatio-temporal Patterns in Brazil" paper

The Episcanner methodology implemented in the paper are implemented in the script: https://github.com/AlertaDengue/episcanner-downloader/blob/main/src/scanner/scanner.py that creates the data plotted in the [online dashboard](https://info.dengue.mat.br/epi-scanner/). To run the script is necessary to have the infodengue incidence data that can be accessed [here](https://api.mosqlimate.org/docs/datastore/GET/infodengue/#usage_examples). 

The params files saved in the `data` folder can be downloaded using the example [here](https://api.mosqlimate.org/docs/datastore/GET/episcanner/). The name of the parameters file contains the disease and state names that they refer to.

The `train_HGBR_model.ipynb` contains the code used to train the regression model discussed in section 2-e) of the article. It also contains the data to generate the Figures 7 and 8. 

The `gen_article_figures.ipynb` contains the code to generate Figures 1, 2, 3, 4, 5, 6 e 9. This code used the parameters table. 
