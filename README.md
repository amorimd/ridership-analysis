# Analysis of TPG ridership data

This repository contains notebooks to analyze the TPG ridership open data, with data visualization and machine learning models.

The source data are:

- TPG Open Data: Ridership per day per stop per line, [see here](https://opendata.tpg.ch/explore/dataset/montees-par-arret-par-ligne/information/?disjunctive.ligne&disjunctive.ligne_type_act&disjunctive.jour_semaine&disjunctive.horaire_type&disjunctive.arret&disjunctive.arret_code_long)
  - Source: transports publics genevois (tpg), état en date du 29/04/2026
- Meteo Suisse: Automatic Weather Stations - Measurement data, daily data for Genève Cointrin (GVE), [see here](https://data.geo.admin.ch/browser/index.html#/collections/ch.meteoschweiz.ogd-smn/items/gve)
  - Source: MétéoSuisse

> [!WARNING]
> This work is for training purposes only, and is not affiliated with the TPG or MétéoSuisse. The data is used under the terms of the respective open data licenses.

## Notebooks

### 1: Data preparation

Notebook `1_tpg_data_build.ipynb` is focused on preparing the data for analysis. The TPG ridership data is aggregated to the line and day level, and enriched with weather data and information about vacations and public holidays.

> [!WARNING]
> The data preparation is not optimized for performance. The base dataset is not included in the repository, only the post-processed dataset is included in folder `/data`.

### 3: Tree-based models

Notebook `3_tree_models.ipynb` is focused on analyzing the data using tree-based models, specifically decision trees and random forests. The performance of the models is evaluated using the R² score and the Mean Squared Error (MSE) on the test set.
