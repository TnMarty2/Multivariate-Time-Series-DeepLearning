# Multivariate-Time-Series-DeepLearning
Multivariate Time Series ARIMA and LSTM Models Forecasting Indonesian Bank Stocks (BBCA, BBRI, BMRI)

## 📌 Project Overview

This repository aims to compare **traditional time series forecasting** (ARIMA) with **deep learning models** (LSTM variants) for multivariate stock price prediction. The dataset includes stock prices and trading volumes of three major Indonesian banks:
- **BBCA** (Bank Central Asia)
- **BBRI** (Bank Rakyat Indonesia)
- **BMRI** (Bank Mandiri)

The goal is to evaluate forecasting performance and identify which model provides the most accurate predictions for financial time series data.

---

## 🧠 Models Implemented

- **ARIMA (AutoRegressive Integrated Moving Average)**
- **Vanilla LSTM**
- **Bidirectional LSTM**
- **Stacked LSTM**

Each model was trained on preprocessed multivariate data (`Close`, `Volume`, etc.) and evaluated based on prediction accuracy.

---

## 🔧 Features & Workflow

### 1. Data Collection
- Source: Kaggle
- Timeframe: Historical daily prices

### 2. Data Preprocessing
- Handling missing values
- Normalization (MinMaxScaler)
- Feature selection: `Close`, `Volume`
- Sequence generation for LSTM models

### 3. Modeling
- ARIMA for univariate time series
- LSTM variants for multivariate time series
- Train-test split ratio 80:20

### 4. Evaluation
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **Mean Absolute Percentage Error (MAPE)**

### 5. Visualization
- Time series plots
- Prediction vs. actual comparison
- Loss and metric trend lines

---

## 📚 Libraries Used

- **Data Handling:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Preprocessing & Metrics:** `scikit-learn`
- **Time Series Modeling:** `statsmodels`
- **Deep Learning:** `tensorflow`, `keras`
- **Data Source:** `yfinance`

---

## 🚀 Results Summary

**BBCA Close**
| Model               | RMSE     | MAE      | MAPE     |
|--------------------|----------|----------|----------|
| ARIMA              | 124.1    | 95.0     | 0.9%     |
| Vanilla LSTM       | 200.5    | 160.7    | 1.6%     |
| Bidirectional LSTM | 227.8    | 192.0    | 1.9%     |
| Stacked LSTM       | 231.5    | 188.0    | 1.9%     |

**BBCA Volume**
| Model               | RMSE         | MAE          | MAPE     |
|--------------------|--------------|--------------|----------|
| ARIMA              | 52.662.514,0 | 27.808.104,2 | 36,9%    |
| Vanilla LSTM       | 55.683.352,3 | 26.871.570,6 | 30,4%    |
| Bidirectional LSTM | 53.678.671,9 | 26.862.275,7 | 34,4%    |
| Stacked LSTM       | 54.245.496,5 | 28.869.947,1 | 40,7%    |
