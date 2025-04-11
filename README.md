# ECO482 Final Project – Predicting SPY ETF Movement with Sentiment and Financial Indicators

This repository contains all code and data preprocessing pipelines used in our final project for ECO482: Machine Learning for Economists. The objective is to predict the direction of daily SPY ETF returns using a combination of sentiment data from news sources and technical financial indicators.

---

## 📄 Project Overview

We explore whether online sentiment and technical indicators can jointly predict short-term S&P 500 ETF (SPY) price movements. Our dataset includes daily financial indicators (e.g., RSI, MACD, ATR), sentiment scores from major U.S. newspapers (NYT, WSJ, WP), and market-based metrics (VIX, OBV, Ichimoku, etc.).

---

## 🧠 Features & Data

**Sentiment Features (Lagged):**
- VADER and SWN compound scores from:
  - *New York Times*
  - *Wall Street Journal*
  - *Washington Post*

**Financial & Technical Indicators (Lagged):**
- Moving Averages (20-day, 50-day)
- RSI, MACD Histogram
- ATR (volatility), OBV (volume), Stochastic RSI
- Ichimoku baseline, VIX, and SPY returns

**Target Variable:**  
- Binary classification: 1 if SPY return is positive the next day, 0 otherwise

---

## ⚙️ Methodology

- Feature engineering and lag creation (1-day and 3-day)
- Standardization and preprocessing
- Model training using time series-aware cross-validation
- Algorithms tested:
  - Logistic Regression
  - Random Forest
  - XGBoost
  - Support Vector Machine (SVM)

---

## 📊 Evaluation Metrics

Models are evaluated using:
- Accuracy
- F1 Score
- ROC AUC
- Out-of-sample strategy returns
- Sharpe Ratio for backtested strategies

A basic long/short strategy is simulated using predicted labels to assess practical performance.

---

## 📁 Repository Structure

