# StockMarket_ShareValue-Trend_Prediction

A Hybrid System Integrating Traditional ML, RL, and Technical Indicators

# Overview
This project aims to predict stock price movements using a combination of traditional machine learning models, list-based rule strategies, and reinforcement learning (RL) agents. By leveraging multiple paradigms, it delivers robust, data-driven predictions that adapt to evolving market behavior. The system includes extensive technical feature engineering, dynamic environment simulation for RL training, and real-time data integration via financial APIs.

# Data Acquisition
Historical stock data is fetched directly using the Yahoo Finance API via the yfinance library. Users can specify the stock symbol and date range, and the system automatically downloads OHLCV (Open, High, Low, Close, Volume) data with support for technical feature augmentation.

# Feature Engineering
An essential part of this project is the use of advanced technical indicators derived from historical stock data. These features capture momentum, volatility, and market trends, significantly enhancing predictive performance. Engineered indicators include:

Exponential Moving Average (EMA): Smoothed trend-following indicator.
Bollinger Bands: Volatility bands around the moving average.
Relative Strength Index (RSI): Momentum oscillator identifying overbought/oversold levels.
Stochastic Oscillator (%K, %D): Compares closing price to price range over time.
On-Balance Volume (OBV): Measures buying/selling pressure using volume and price.
Chaikin Money Flow (CMF): Captures the flow of money into/out of a stock.
Average True Range (ATR): Reflects market volatility.
Missing or infinite values are cleaned and scaled using StandardScaler to prepare the dataset for both machine learning models and RL environments.

# Modeling Approaches
Supervised Learning Models: Includes regression and classification techniques (e.g., XGBoost, LSTM) to predict future stock prices or directional movement.
List-Based Strategies: Rule-based logic derived from indicator thresholds (e.g., RSI < 30 as a buy signal) is used to model expert heuristics.
Reinforcement Learning: RL agents interact with a simulated market environment, learning optimal trading strategies via trial-and-error, reward maximization, and state transitions based on technical signals.

# Key Features
Real-time stock data integration via Yahoo Finance API
Modular technical indicator functions
Clean, scaled datasets ready for modeling
Versatile architecture combining rule-based and learning-based strategies
Integrated reinforcement learning training loop for strategy optimization
