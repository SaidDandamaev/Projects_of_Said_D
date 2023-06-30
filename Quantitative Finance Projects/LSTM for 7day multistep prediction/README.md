# README - Bitcoin Time Series multistep Forecasting

This repository contains the code for predicting Bitcoin prices using time series data. The code primarily uses a Long Short-Term Memory (LSTM) network, a type of recurrent neural network well-suited to time series data. The code also includes an implementation of Sequential Model-based Algorithm Configuration (SMAC) to fine-tune hyperparameters. 

## Code Overview

The code is divided into several sections:

1. **Installation of Dependencies**: This section takes care of installing all the necessary libraries and packages that will be needed for the execution of the script.

2. **Data Import**: We use Yahoo Finance to download the Bitcoin data. The data contains open, high, low, closing prices and volume of Bitcoin trades.

3. **Data Preprocessing**: We compute an additional feature 'stability' to provide insight into the relative change in Bitcoin prices over time. We also calculate the 'drawdowns' for our Bitcoin series.

4. **Model Training**: In this part of the script, we define and train our LSTM model. We have defined two types of LSTM layers (standard and bidirectional), as well as Dropout layers for regularization, Dense layers for output, and used Mean Absolute Error (MAE) as the loss function. We also use SMAPE (Symmetric Mean Absolute Percentage Error) as an additional metric. 

5. **Model Tuning**: This section is commented out in the script but contains code for fine-tuning the model using keras-tuner.

6. **Model Testing**: Finally, we load the trained models and use them to predict the future prices.

## Running the Code

Before running the code, please ensure you have the necessary libraries and packages installed. If not, you can install them by uncommenting the first section of the script. 

To run the script, you simply need to execute the cells sequentially. It is recommended to use Jupyter notebook for this purpose.

## Model Performance

The performance of the model is evaluated using three metrics: SMAPE (Symmetric Mean Absolute Percentage Error), MAE (Mean Absolute Error), and MDA (Mean Directional Accuracy).

## Results

| Forecasting horizon | Metrics | OHLCV input data | OHLCV and sustainability input data | OHLCV and cumulative drawdowns input data |
|---------------------|---------|------------------|-------------------------------------|-------------------------------------------|
| 1                   | SMAPE   | 2.10%            | 2.41%                               | 2.83%                                     |
|                     | MAE     | 485.39           | 552.71                              | 625.41                                    |
|                     | MDA     | 56%              | 50%                                 | 52%                                       |
| 2                   | SMAPE   | 2.46%            | 2.86%                               | 3.19%                                     |
|                     | MAE     | 570.42           | 670.51                              | 706.46                                    |
|                     | MDA     | 55%              | 52%                                 | 52%                                       |
| 3                   | SMAPE   | 2.92%            | 3.15%                               | 3.82%                                     |
|                     | MAE     | 673.19           | 740.31                              | 842.87                                    |
|                     | MDA     | 55%              | 50%                                 | 52%                                       |
| 4                   | SMAPE   | 3.33%            | 3.40%                               | 4.12%                                     |
|                     | MAE     | 753.54           | 794.31                              | 900.93                                    |
|                     | MDA     | 56%              | 51%                                 | 54%                                       |
| 5                   | SMAPE   | 3.98%            | 3.91%                               | 4.73%                                     |
|                     | MAE     | 905.14           | 920.76                              | 1041.13                                   |
|                     | MDA     | 51%              | 49%                                 | 52%                                       |
| 6                   | SMAPE   | 4.18%            | 4.05%                               | 5.22%                                     |
|                     | MAE     | 945.56           | 945.90                              | 1123.8                                    |
|                     | MDA     | 56%              | 53%                                 | 53%                                       |
| 7                   | SMAPE   | 4.40%            | 4.36%                               | 5.34%                                     |
|                     | MAE     | 992.82           | 1018.80                             | 1156.34                                   |
|                     | MDA     | 56%              | 53%                                 | 53%                                       |
|                     |         |                  |                                     |                                           |
