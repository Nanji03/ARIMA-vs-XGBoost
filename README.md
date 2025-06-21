# ARIMA-vs-XGBoost
This notebook compares two forecasting models — ARIMA (AutoRegressive Integrated Moving Average) and XGBoost (Extreme Gradient Boosting) — for predicting Google’s daily stock closing prices.

Objective
To evaluate and compare the performance of:
-A traditional time series model (ARIMA)
-A machine learning model (XGBoost with lag features)
on both 1-day and 7-day stock price forecasts.

Dataset
  Source: Google_stock_data[1].csv
  Columns used: Date, Close, Open, High, Low, Volume
  Focus variable: Close price


Methods
ARIMA(1,1,1): 
Trained on the full dataset with differencing to ensure stationarity.

XGBoost:
Uses lag features (previous 7 days’ close prices).
Recursive strategy used for multi-day forecasting.

Results
1-Day Forecast:
XGBoost had a lower RMSE than ARIMA.

7-Day Forecast:
XGBoost showed stronger consistency using recursive predictions.

A statistical comparison (mean, std dev of differences) was performed.

Conclusion
XGBoost outperformed ARIMA on both short and medium-term forecasts, demonstrating its power with engineered features even in time series problems.
