# Expedia Hotel Recommendation

A team machine-learning study that compares three model families for recommending the five hotel clusters an Expedia customer is most likely to choose.

[![Read the full paper](https://img.shields.io/badge/Read_the_full_paper-PDF-B31B1B?logo=adobeacrobatreader&logoColor=white)](./Hotel_Recommendation.pdf)

## Overview

This academic project uses the [Expedia Hotel Recommendations](https://www.kaggle.com/competitions/expedia-hotel-recommendations) dataset published on Kaggle. The task is framed as multiclass classification: predict and rank the top five `hotel_cluster` candidates from customer search, click, and booking events.

The study was completed at Lakehead University by Sravya Sudarsanan, Eunwha Park, and Jude Jolly Mampilly.

## What we used

- **Data:** Expedia training events from 2013-2014 and test events from 2015, with 22 analyzed fields
- **Models:** k-Nearest Neighbors (k-NN), Random Forest, and XGBoost
- **Evaluation:** Mean Average Precision at 5 (MAP@5) as the ranking metric, with classification accuracy reported alongside it
- **Preprocessing:** missing-value imputation, derived check-in and stay-duration features, and experiments with and without outliers
- **Analysis:** booking and package behavior, travel seasonality, correlation analysis, and f-test feature selection
- **Model selection:** hyperparameter tuning followed by a comparison of the three model families

## Results

The best hyperparameter-tuned results reported in the paper are:

| Model | MAP@5 | Accuracy |
| --- | ---: | ---: |
| k-NN | 0.3007 | 0.2123 |
| **Random Forest** | **0.4096** | **0.3160** |
| XGBoost | 0.4052 | 0.3061 |

Random Forest achieved the highest MAP@5 and accuracy in the documented evaluation, with XGBoost close behind. The f-test feature-selection experiment did not improve the three models' scores.

## Paper

The full eight-page report describes the dataset, related work, preprocessing, model design, evaluation method, results, limitations, and future work.

**[Open `Hotel_Recommendation.pdf`](./Hotel_Recommendation.pdf)**

## Repository scope

This repository currently contains the project paper. The implementation and Kaggle data are not included, so the reported results can be reviewed here but cannot be reproduced from this repository alone.
