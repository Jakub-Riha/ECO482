# Sentiment-Driven Markets: Enhancing ETF Price Prediction with News and Tweet Analysis


Replication files & code for an ECO482 course project.

---

## 📄 Project Overview

This repository contains the paper PDF, code, and supporting files, for a machine learning forecast of S&P500 daily price movements. This project aims to explore whether Trump's tweets, major news headlines, and technical indicators can jointly predict short-term S&P 500 ETF (SPY) price movements

---

## 🧠 Features & Data

**Sentiment Features (Lagged):**
- VADER and SWN compound scores from:
  - *New York Times*
  - *Wall Street Journal*
  - *Washington Post*
 
- VADER and Topic Discovery from:
  - *Trump's tweets*

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
  - K-Nearest Neighbors (KNN)

---

## 📊 Evaluation Metrics

Models are evaluated using:
- Accuracy
- F1 Score
- ROC AUC
- PnL strategy returns
- Sharpe Ratio

A basic long/short strategy is simulated using predicted labels to assess practical performance.

---

## 📁 Repository Structure

**ECO482_Code.ipynb**
- Full ML pipeline (data loading, training, evaluation) 

**dataset.csv**
- Cleaned dataset with sentiment and financial features models

---

## 🧪 Requirements

- Python 3.8+
- Required packages:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`
  - `xgboost`

Install via:

```bash
pip install -r requirements.txt
