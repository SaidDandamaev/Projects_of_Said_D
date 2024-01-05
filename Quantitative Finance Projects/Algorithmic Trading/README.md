# Algorithmic Trading Strategy and Backtesting

### Made by Said Dandamaev

## Overview
This project involves developing an algorithmic trading strategy based on **machine learning** models and **backtesting** it using historical cryptocurrency data. The strategy is inspired by quantitative trading approaches that leverage statistical and machine learning methods to predict asset price movements. The approach was inspired by the article: https://doi.org/10.3934/QFE.2023028 

## Strategy
The strategy implemented in this project follows the methodology outlined in a research article on quantitative trading. It involves two main steps:
1. **Regression Model**: Predicting the next day's Moving Average (MA) change (which also indicates change in Close price for future day).
2. **Classification Model**: Based on the regression output, predicting whether the asset's price will go up (+1) or down (-1).

## Features
- Fetches historical price data for Bitcoin (BTC/USDT) from the `ccxt` library.
- Implements feature engineering, adding technical indicators like Moving Averages, RSI, and OBV.
- Utilizes `Fedot`, a machine learning framework, for building and optimizing regression and classification models.
- Backtesting is performed using the `Backtesting.py` library to evaluate the strategy's performance.

## Tools and Libraries
- `pandas` for data manipulation.
- `numpy` for numerical computations.
- `ccxt` for fetching historical cryptocurrency data.
- `sklearn` for scaling data and model evaluation.
- `Fedot` for automated model design.
- `Backtesting.py` for simulating the trading strategy over historical data.

## Usage
1. Fetch historical data.
2. Apply feature engineering.
3. Train regression and classification models.
4. Backtest the strategy to evaluate performance.


## Contacts
- Email: ssdandamaev@gmail.computations
- Telegram: @treasure_of




