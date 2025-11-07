# Amazon-Stock-Price-Forecasting-using-ARIMA-SARIMA-GARCH-and-LSTM

📘 Project Overview

This project aims to forecast Amazon’s stock price movement using multiple time-series forecasting models
to compare their predictive performance and ability to capture both trend and volatility in financial data.

The analysis covers data from 1997 to 2020, exploring both statistical and deep learning approaches to understand short- and long-term market behavior.

---
🗂️ Dataset

Source: [https://www.kaggle.com/datasets/salmanfaroz/amazon-stock-price-1997-to-2020](https://www.kaggle.com/datasets/salmanfaroz/amazon-stock-price-1997-to-2020)
Period: 15/05/1997- 31/07/2020
Size: 5842 daily observations × 6 columns
Frequency: Daily
Target Variable: `Close` — closing stock price of Amazon

---

⚙️ Methodology

1. Data Preparation
  - Imported daily Amazon stock prices.

  - Performed log transformation and differencing to ensure stationarity.

  - Split the data into training and testing sets.

2. Model Implementation

  - ARIMA / SARIMA: Modeled linear time dependencies and seasonality.

  - GARCH: Captured time-varying volatility and clustering in stock returns.

  - LSTM: Applied deep learning to learn nonlinear temporal relationships.

3. Model Evaluation

  - Compared models using MAE, RMSE, and visual forecast plots.

  - Conducted rolling forecasts and residual diagnostics for model stability.

---

📊 Results Summary

| **Model** | **Key Strength** | **Limitation** | **Performance** |
|:-----------|:-----------------|:---------------|:----------------|
| **ARIMA** | Simple and easy to interpret | Struggles with nonlinear and rapidly changing patterns | Moderate |
| **SARIMA** | Handles seasonality and cyclical patterns | Still assumes linear relationships | Moderate |
| **GARCH** | Effectively captures volatility clustering and risk | Focuses on variance rather than price-level forecasting | Good |
| **LSTM** | Captures nonlinear trends and sudden market shocks | Requires tuning and higher computational resources | **Best** |

Best Model: LSTM

- MAE: 46.27

- RMSE: 60.75

Mean Price: 1439.78

This indicates that, on average, the LSTM’s predictions deviated by around **3–4%** from the actual stock prices, showing **strong predictive accuracy** and **robust generalization** on unseen data.

LSTM effectively captured both **long-term upward trends** and **short-term fluctuations**,  outperforming traditional statistical models that rely on linear assumptions.

---

📈 Key Insights

- ARIMA/SARIMA: Poor in reacting to short-term shocks; produce smoothed, linear forecasts.

- GARCH: Strong at capturing volatility clustering, useful for risk analysis.

- LSTM: Best at capturing nonlinear trends and complex time dependencies, achieving the lowest error metrics.

---
💡 Conclusion

The experiment shows that deep learning models like LSTM outperform traditional time-series methods for forecasting stock prices, particularly in volatile and nonlinear financial markets.
Future extensions could include hybrid ARIMA–LSTM models or incorporating macroeconomic indicators to improve predictive power.

🧩 Technologies Used

Python (Pandas, NumPy, Matplotlib, Seaborn,itertools,datetime,os)

Statsmodels, arch, TensorFlow/Keras, scikit-learn,pmdarima

Jupyter Notebook for analysis and visualization

