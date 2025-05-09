# 📈 Forecasting Tesla Stock Prices Using Time Series Analysis

This project focuses on applying classical and deep learning models to forecast Tesla Inc.'s stock prices using time series data. We compare multiple models across different time windows to identify the most effective forecasting strategy for volatile financial assets.

## 🏫 Project Submitted At
**School of Computer Science Engineering and Technology, Bennett University**  
**Submitted by:** Utkarsh Sharma (E22CSEU0495)
**Guide:** Mr. Arun Singh Bhadwal

---

## 📌 Objective

- Analyze historical stock data of Tesla to uncover patterns.
- Implement ARIMA/SARIMA, LSTM, BiLSTM, GRU, and hybrid deep learning models.
- Compare the performance of these models in predicting stock prices.

---

## 📊 Dataset

- **Source:** Kaggle - Tesla Historical Stock Prices
- **Period:** Jan 2010 – Dec 2023  
- **Filtered Subset:** Jan 2022 – Dec 2023  
- **Features:** Date, Open, High, Low, Close, Volume

---

## 🔧 Data Preprocessing

- Converted `Date` to datetime and set as index
- Used `Close` price for final modeling
- Handled missing values with forward fill and interpolation
- Normalized values using Min-Max Scaling
- Engineered features: rolling means (MA20, MA50), differencing, lag returns
- Split data: 80/20 (full), 65/35 (filtered)

---

## 📉 Models & Results

### 🔸 Classical Model (ARIMA)
- Poor performance due to non-linearity
- **RMSE:** 74.80 | **MAE:** 59.51 | **R²:** -0.31

### 🔸 LSTM
- **RMSE:** 37.86 | **MAE:** 22.82 | **R²:** 0.76

### 🔸 Bi-LSTM
- **RMSE:** 35.05 | **MAE:** 19.26 | **R²:** 0.80

### 🔸 Hybrid Bi-LSTM + GRU
- **RMSE:** 32.68 | **MAE:** 14.35 | **R²:** 0.82

### 🔸 Final Hybrid Model (Filtered Data: 2022–23)
- **RMSE:** 13.66 | **MAE:** 11.03 | **R²:** 0.86

---

## 📈 Forecast

The final hybrid model was used to forecast the next 30 days of Tesla stock prices. The trend matched historical patterns and captured volatility effectively.

---

## 🔍 Limitations

- Does not incorporate external news, sentiment, or economic indicators
- No real-time prediction
- Financial market volatility can reduce accuracy

---

## 🚀 Future Work

- Add sentiment and macroeconomic data
- Explore attention and transformer-based architectures
- Use real-time streaming data for live forecasts
- Introduce technical indicators like RSI, EMA, MACD




---

## 📦 Dependencies

Install with:

```bash
pip install -r requirements.txt

