# Algorithmic Trading with Machine Learning and Quantitative Strategies

This project focuses on developing and testing algorithmic trading strategies using machine learning and quantitative methods.

## Introduction

Algorithmic trading uses computer algorithms to automate trading decisions. This project aims to create efficient and profitable trading strategies using various algorithms and data analysis techniques.

## Project Structure

- Algorithmic_Trading_Machine_Learning_Quant_Strategies.ipynb : Jupyter notebook containing the code for developing and testing the trading strategies.

- sentiment_data.csv : CSV file containing Twitter sentiment data.

- simulated_5min_data.csv : CSV file containing simulated 5-minute intraday data.

- simulated_daily_data.csv : CSV file containing simulated daily data.

## Methods and Steps

### 1. Download/Load SP500 Stocks Prices Data

- Download SP500 stock prices data using `yfinance`.
- Calculate features and technical indicators for each stock:

  - Garman-Klass Volatility
  - RSI
  - Bollinger Bands
  - ATR
  - MACD
  - Dollar Volume

### 2. Aggregate Data and Filter Top 150 Most Liquid Stocks

- Aggregate data to the monthly level.
- Filter the top 150 most liquid stocks for each month based on dollar volume.

### 3. Calculate Monthly Returns

- Calculate monthly returns for different time horizons as features.

### 4. Download Fama-French Factors and Calculate Rolling Factor Betas

- Download Fama-French factors using `pandas-datareader`.
- Calculate rolling factor betas using `RollingOLS`.

### 5. K-Means Clustering

- Fit a K-Means clustering algorithm to group similar assets based on their features.
- Visualize clusters.

### 6. Portfolio Optimization

- Select assets based on the cluster and form a portfolio based on Efficient Frontier max Sharpe ratio optimization.
- Define a portfolio optimization function using `PyPortfolioOpt`.

### 7. Twitter Sentiment Investing Strategy

- Load Twitter sentiment data.
- Aggregate monthly and calculate average sentiment for the month.
- Select top 5 stocks based on their cross-sectional ranking for each month.
- Calculate portfolio returns with monthly rebalancing.
- Compare strategy returns to NASDAQ/QQQ returns.

### 8. Intraday Strategy Using GARCH Model

- Load simulated daily and 5-minute data.
- Fit a GARCH model on the daily data and predict 1-day ahead volatility.
- Calculate prediction premium and form a daily signal.
- Merge with intraday data and calculate intraday indicators to form the intraday signal.
- Generate the position entry and hold until the end of the day.
- Calculate final strategy returns.

## Visualization

- Visualize portfolio returns and compare to SP500 returns.
- Visualize Twitter engagement ratio strategy return over time.
- Visualize intraday strategy returns.

## Requirements

- Python 3.8+
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- yfinance
- pandas_datareader
- statsmodels
- sklearn
- PyPortfolioOpt
- arch
- pandas_ta


## License

This project is licensed under the MIT License.
