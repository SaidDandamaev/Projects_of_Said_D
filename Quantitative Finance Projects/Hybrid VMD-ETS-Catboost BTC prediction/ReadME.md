# Cryptocurrency Price Forecasting

This project is dedicated to forecasting cryptocurrency prices using advanced machine learning techniques. By leveraging historical price data, we aim to predict future trends and movements in the cryptocurrency market using hybrid approach, based on **VMD** decomposition and then application of ARIMA/ETS for trend prediction and **GBR (Catboost)** for predicting fluctuations.

## Installation

Before running the project, ensure you have the necessary libraries installed. The project relies on `yfinance` for financial data, `sktime` and `skforecast` for time series analysis, `catboost` for gradient boosting, `pmdarima` for ARIMA modeling, and `vmdpy` for Variational Mode Decomposition.

## Overview

The project consists of several components that work together to predict cryptocurrency prices:

- **Data Acquisition:** We download historical Bitcoin price data and process it for analysis.
- **Data Preparation:** The data is preprocessed, including  train-test splitting, to prepare it for input into our models. 
- **Decomposition and Feature Engineering:** We implement Variational Mode Decomposition to extract features from the time series data, which are then used to improve the model's predictions.
- **Hybrid Forecasting:** A novel approach is taken by combining ARIMA and CatBoostRegressor to create a hybrid model that utilizes the strengths of both methods.
- **Model Validation:** The models' predictions are evaluated using SMAPE, MAE, and MDA metrics to ensure reliability and accuracy.

## Usage

The project is structured as a series of Jupyter notebook cells. To replicate the analysis, execute the cells in order, from data acquisition to validation.

## Contributing

Contributions to this project are welcome. If you have suggestions for improving the models or would like to implement additional features, please feel free to fork the repository and submit a pull request.

## License

This project is open source and available under the MIT License.
