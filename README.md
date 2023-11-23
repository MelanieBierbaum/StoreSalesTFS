# StoreSalesTFS
Repository for the Kaggle challenge Store Sales Time Series Forecasting

This repository contains several notebooks I made for the Kaggle Challenge https://www.kaggle.com/competitions/store-sales-time-series-forecasting.

The task was to predict sales data for 2 weeks. 

Metric: root mean squared log error.

EDA was done using PowerBi, but the pbix file is to large to upload here.

## StoreSalesTSF - LGBM
LightGBM was the first model I used. Many re-runs with evolving features. Marking categorical features gave similar results than not marking them. Although hyperparameters were tuned with unmarked categorical features.

## StoreSalesTSF - Regression
As a 2nd model I ran Regression (Linear + Ridge). While the results were not that great, it made me aware that there are still NaNs in my features. (LightGMB just handled them)

## StoreSalesTSF - XGBoost
XGBoost was the 3rd model I used. It gave me my best result on the public leaderboard. Place 78/698 at the time. 
Marking categorical features gave worse results, even when hyperparameters were retuned with marking categorical features.

## StoreSalesTSF - Catboost
Catboost was the 4th model I ran. This was my first time using catboost. It took quite long to run, compared to XGBoost and LightGBM and did not deliver equal results.
Always marked categorical features.

## StoreSalesTSF - FeatureEngineering
In this notebook I created all my features. The other notebooks load this one. 

## StoreSalesTSF - Optuna Tuning
This one notebook was used to tune LightGBM, XGBoost and Catboost. Each algorithm was re-run with optimized hyperparameters and it gave better results each time. For tuning only a very basic subset of the featues was used. Basically only the original features plus the time-stamp based features.

## StoreSalesTFS - PandasProfiler
I used this one for a quick overview about statistical properties of my data.


## Open
Maybe re-tune my best XGBoost with all the features again and re-train afterwards.

