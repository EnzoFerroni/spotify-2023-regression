# Spotify 2023 Regression

[![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)](https://www.python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Regression%20%2B%20KNN-F7931E?logo=scikitlearn&logoColor=white)](https://scikit-learn.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

Predicting the danceability and energy of the most-streamed Spotify songs of 2023 with Linear Regression and KNN, plus outlier detection with Isolation Forest.

## Table of Contents

- [About](#about)
- [Method](#method)
- [Results](#results)
- [Getting Started](#getting-started)
- [Documents](#documents)
- [Team](#team)
- [License](#license)

## About

Data Science course project at Universidade Presbiteriana Mackenzie (2025), delivered
in two stages: a partial project (N1) and a final project (N2). Using the audio
features of the most-streamed Spotify songs of 2023, the project compares two
regression models and then looks for atypical songs in the dataset. The notebook and
reports are in Portuguese.

## Method

1. **Pre-processing.** Handle missing `key` values, convert `streams` from text to
   integer and encode `mode` (Major/Minor) as 1/0.
2. **Models.** Linear Regression, chosen for being simple and interpretable, against a
   KNN Regressor.
3. **Tuning k.** MAE, RMSE and R² plotted for a range of k values; the best region lies
   between 10 and 30 neighbors.
4. **Targets.** Each model predicts a song's danceability and its energy.
5. **Outliers.** Isolation Forest flags atypical songs, visualized in two dimensions
   with PCA.

## Results

Compared on MAE, RMSE and R², Linear Regression performed better than the KNN Regressor
on both tasks, predicting danceability and energy.

## Getting Started

```bash
git clone https://github.com/EnzoFerroni/spotify-2023-regression.git
cd spotify-2023-regression
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook notebook.ipynb
```

The dataset `spotify-2023.csv` is included in the repository.

## Documents

- Partial project (N1): [`relatórios/EntregaProjetoParcial(N1).pdf`](relat%C3%B3rios/)
- Final project (N2): [`relatórios/EntregaProjetoFinal(N2).pdf`](relat%C3%B3rios/)
- Reference notebooks: [`referencias/`](referencias/)

## Team

| Name | GitHub |
| --- | --- |
| Enzo Ferroni | [@EnzoFerroni](https://github.com/EnzoFerroni) |
| Luiz Gabriel Profirio Mendes | [@omgitsgm](https://github.com/omgitsgm) |

Fork of the team repository [omgitsgm/projeto-ciencia-dados](https://github.com/omgitsgm/projeto-ciencia-dados).

## License

Code and documents are released under the [MIT License](LICENSE). Copyright (c) 2025
Enzo Ferroni and Luiz Gabriel Profirio Mendes. The dataset belongs to its original
authors and is redistributed under its original terms.
