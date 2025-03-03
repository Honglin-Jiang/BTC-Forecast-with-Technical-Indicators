# Bitcoin Market Forecasting with Machine Learning

## Overview

This project focuses on using machine learning to predict the direction of Bitcoin price changes using technical indicators. By analyzing the differences, magnitudes, and directions of these indicators, we aim to forecast whether Bitcoin prices will go up or down on the next day. The goal is to provide algorithmic traders and Bitcoin buyers with insights on when to make strategic decisions for buying or selling Bitcoin to maximize returns.

## Data Description

We use a dataset from [Kaggle](https://www.kaggle.com/) that contains BTC trading data published by Binance, a global cryptocurrency exchange platform. The dataset includes Bitcoin price data and technical indicator values from **2020-01-01** to **2023-10-22** at a **minute-level frequency**.

- **Dataset Characteristics:**
  - Around **2,000,000** entries.
  - **27 columns** with a mix of timeseries, integer, and float data types.
  - Contains BTC pricing data and several technical indicators derived from historical pricing, such as **ATR, HMA, KAMA, CMO, Z-Score**, and **QStick**.

### Data Processing

Upon further examination, we decided to condense the dataset to a **day-by-day** frequency. We also expanded the dataset by adding more comprehensive technical indicators, including:

- **Volume indicators**
- **Momentum indicators**
- **Volatility indicators**

### Reasoning Behind Data Transformation

The original minute-level data showed weak efficiency due to the volatile nature of Bitcoin prices. Consequently, we found that the minute-level prices and the original trend-related indicators were insufficient for our model. By switching to daily pricing data and adding more comprehensive indicators, we aim to provide a better understanding of market movements and improve the model’s prediction capabilities.

## Target Variable

The target variable for this project is the **BTC Next Day Price Change** (up vs. down):

- We focus on predicting the **close price movement** (compared to the previous day) to forecast whether it will go up or down.
  
  **Why Close Prices?**
  - **Open prices** are subject to after-market volatility, making them unreliable.
  - **High/Low prices** are too volatile and don’t represent the actual performance of the asset over time.

Thus, we choose **close prices** as the most stable and reliable measure for predicting Bitcoin price movement.

## How It Works

- The model uses historical Bitcoin data and technical indicators to predict the next day's price change (up vs. down).
- We leverage machine learning algorithms to build a model that can recognize patterns and make predictions based on historical price movements and indicators.
- The model helps traders by providing insights into whether the price will go up or down, aiding them in making informed decisions for their trading strategies.

## Getting Started

To run this project, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/bitcoin-market-forecasting.git
