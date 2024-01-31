# Stock Price Prediction with Machine Learning Models

In this project, I explore the application of machine learning models for predicting stock price
movements. I leverage financial indicators and historical stock price data to train models that can
predict the direction of stock price changes.

**Note:** This project is for educational purposes only and should not be construed as investment advice. The models presented here are for experimental and learning purposes, and their performance may not translate to real-world trading scenarios.

## Data Collection
I gathered historical stock price data for a selected set of BIST100 stocks from Yahoo Finance. 

The data spans from May 21, 2022, to December 13, 2023.

## Feature Engineering
To enhance the predictive power of my models, I employed various technical indicators. These
indicators include Moving Average Convergence Divergence (MACD), Relative Strength Index
(RSI), Bollinger Bands, Average Directional Index (ADX), Exponential Moving Average (EMA), and
Simple Moving Average (SMA).

## Data Preprocessing
The collected data underwent preprocessing steps, including imputation of missing values using
the mean imputation strategy. The target variable, representing the direction of stock price
changes, was derived by comparing the closing prices on consecutive days.

## Model Training and Evaluation
I trained three different machine learning models for each stock: [Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html), [Light GBM](https://lightgbm.readthedocs.io/en/stable/), and
[CatBoost](https://catboost.ai/). 

Hyperparameter optimization with [Optuna](https://optuna.org/) was performed to enhance each model's
performance. 

Model evaluation metrics included accuracy, precision, recall, and F1 score.

## Top 10 Tickers Based on F1 Score and Models Used
| Stock Symbol | Best Model | F1 Score | Accuracy | Precision | Recall |
|--------------|------------|----------|----------|-----------|--------|
| AKFYE.IS     | CatBoost   | 0.7517   | 0.75     | 0.6667    | 0.8    |
| EUPWR.IS     | CatBoost   | 0.7190   | 0.7188   | 0.6875    | 0.7333 |
| YYLGD.IS     | CatBoost   | 0.6642   | 0.6709   | 0.7857    | 0.5238 |
| BIMAS.IS     | CatBoost   | 0.6415   | 0.6456   | 0.68      | 0.7391 |
| GENIL.IS     | CatBoost   | 0.6364   | 0.6389   | 0.6667    | 0.5556 |
| ODAS.IS      | LGB        | 0.6359   | 0.6329   | 0.7143    | 0.6383 |
| ISMEN.IS     | CatBoost   | 0.6354   | 0.6456   | 0.6415    | 0.7907 |
| ZOREN.IS     | CatBoost   | 0.6346   | 0.6329   | 0.7105    | 0.6    |
| CANTE.IS     | RF         | 0.6331   | 0.6329   | 0.6053    | 0.6216 |
| AHGAZ.IS     | LGB        | 0.6234   | 0.6327   | 0.5455    | 0.8571 |

