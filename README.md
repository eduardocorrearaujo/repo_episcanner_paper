# Code and data of the "Large-scale Epidemiological modeling: Scanning for Mosquito-Borne Diseases Spatio-temporal Patterns in Brazil" paper

The Episcanner methodology implemented in the paper are implemented in the script: https://github.com/AlertaDengue/episcanner-downloader/blob/main/src/scanner/scanner.py that creates the data plotted in the [online dashboard](https://info.dengue.mat.br/epi-scanner/). To run the script is necessary to have the infodengue incidence data that can be accessed [here](https://api.mosqlimate.org/docs/datastore/GET/infodengue/#usage_examples). 

The params files saved in the `data` folder can be downloaded using the example [here](https://api.mosqlimate.org/docs/datastore/GET/episcanner/). The name of the parameters file contains the disease and state names that they refer to.

The `train_HGBR_model.ipynb` contains the code used to train the regression model discussed in section 2-e) of the article. It also contains the data to generate the Figures 7 and 8. 

The `gen_article_figures.ipynb` contains the code to generate Figures 1, 2, 3, 4, 5, 6 e 9. This code used the parameters table. 

The table of features used in the HGBR model is presented in the table below: 

| Feature description                                                                                                                   | Type            |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| \textbf{year:}  year of the peak week  that are being predicted.                                                                        | temporal        |
| \textbf{cases\_jan:}   sum of cases in the January of the year whose peak week are being predicted..                                    | epidemiological |
| \textbf{cases\_3rdQ:} sum of cases on the third quarter of the previous year.                                                           | epidemiological |
| \textbf{cases\_4thQ:} sum of cases on the fourth quarter of the previous year.                                                          | epidemiological |
| \textbf{population:} population in the previous year.                                                                                   | demographic     |
| \textbf{peak\_week:}  peak week estimated on the previous year.                                                                         | epidemiological |
| \textbf{R0:} reproduction number estimated on the previous year.                                                                        | epidemiological |
| \textbf{ep\_dur:} epidemic duration estimated on the previous year.                                                                     | epidemiological |
| \textbf{mean\_temp\_4thQ:} average of the average temperature over the fourth quarter of the previous year.                             | climatic        |
| \textbf{temp\_range\_4thQ:} average of the temperature amplitude  over the fourth quarter of the previous year.                         | climatic        |
| \textbf{max\_temp\_4thQ:} average of the maximum temperature over the fourth quarter of the previous year.                              | climatic        |
| \textbf{min\_temp\_4thQ:} average of the minimum temperature over the fourth quarter of the previous year.                              | climatic        |
| \textbf{min\_humid\_4thQ:} average of the minimum humidity over the fourth quarter of the previous year.                                | climatic        |
| \textbf{max\_humid\_4thQ:} average of the maximum humidity over the fourth quarter of the previous year.                                | climatic        |
| \textbf{humid\_range\_4thQ:}average of the  humidity amplitude over the fourth quarter of the previous year.                            | climatic        |
| \textbf{enso\_4thQ:} average of the  multivariate ENSO (El Niño-Southern Oscillation) in the fourth quarter of the previous year.       | climatic        |
| \textbf{tot\_precip\_4thQ:} sum of the total precipitation over the fourth quarter of the previous year.                                | climatic        |
| \textbf{rainy\_days\_4thQ:} days with rain (precipitation above zero) over the fourth quarter of the previous year.                     | climatic        |
| \textbf{days\_min\_temp\_4thQ:} days with minimum temperature below 15-celsius degrees                                                  | climatic        |
| \textbf{days\_temp\_range\_4thQ:} days with temperature amplitude above celsius degrees.                                                | climatic        |
| \textbf{days\_mean\_umid\_4thQ:} days with average humidity above 0.8.                                                                  | climatic        |
| \textbf{jan\_mean\_temp:}  average of the average temperature over the january of the year whose peak week is being predicted.          | climatic        |
| \textbf{jan\_temp\_range:} average of the temperature amplitude over the january of the year whose peak week is being predicted.        | climatic        |
| \textbf{jan\_max\_temp:} average of the maximum temperature over the january of the year whose peak week is being predicted.            | climatic        |
| \textbf{jan\_min\_temp:} average of the minimum temperature over the january of the year whose peak week is being predicted.            | climatic        |
| \textbf{jan\_tot\_precip:} sum of total precipitation over the january of the year whose peak week is being predicted.                  | climatic        |
| \textbf{rainy\_days\_jan:} days with precipitation over the january of the year whose peak week is being predicted.                     | climatic        |
| \textbf{enso\_jan:} average of the ENSO (El Niño-Southern Oscillation) over the January of the year whose peak week is being predicted. | climatic        |
| latitude of  the city center.                                                                                                           | spatial         |
| longitude of the city center.                                                                                                           | spatial         |

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.13236547.svg)](https://doi.org/10.5281/zenodo.13236547)
