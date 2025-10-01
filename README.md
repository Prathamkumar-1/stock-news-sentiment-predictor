# Stock News Predictor

This repository contains a **single Jupyter Notebook (`stock_news_predictor.ipynb`)** that demonstrates how to combine **stock market price data** with **news sentiment analysis** to predict short-term stock movements.

---

## Overview

The notebook walks through a complete workflow:

1. **Data Collection**
   - Downloads historical stock prices (using `yfinance`).
   - Generates or loads news headlines with timestamps.

2. **Feature Engineering**
   - Calculates returns, moving averages, and volatility from price data.
   - Scores sentiment of headlines using **TextBlob**.
   - (Optional) Trains a simple **Logistic Regression with TF-IDF** if labeled data is sufficient.

3. **Time-Series Forecasting**
   - Tests stationarity and builds an **ARIMA model** to forecast future prices.
   - Handles non-stationary series by differencing where needed.

4. **Sentiment Modeling**
   - Labels each headline as positive, negative, or neutral.
   - Aggregates sentiment scores by trading day.

5. **Ensemble Predictions**
   - Combines ARIMA predictions (price-based signal) with sentiment predictions (news-based signal).
   - Produces a final UP/DOWN prediction for stock movement.

6. **Visualization & Dashboard**
   - Plots historical stock prices with forecast overlay.
   - Displays sentiment trends over time.
   - Shows distribution of returns and sentiment correlations.
   - Provides a summary box of the model’s key outputs.
