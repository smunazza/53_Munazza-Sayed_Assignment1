#  Stock Price Forecasting using ARIMA Model: A Case Study of DIVISLAB

## (1) Problem Statement
Stock prices are highly dynamic and influenced by multiple market factors, making them difficult to predict accurately. Investors and analysts require reliable methods to analyze historical data and estimate future price movements. In this project, the challenge is to analyze past stock price data of DIVISLAB and apply time series modeling techniques to understand its behavior and forecast future prices.


## (2) Objective
- To collect and preprocess historical stock price data of DIVISLAB.
- To analyze the time series characteristics of the stock prices.
- To apply the ARIMA model for forecasting future stock prices.
- To evaluate the model performance using appropriate metrics.
- To predict the next 30 days’ closing prices and interpret the trend.


## (3) Dataset
Source:
Historical stock price data was obtained from the National Stock Exchange (NSE) using the yfinance library.

Features:
Date
Open
High
Low
Close
Volume

Size:
Approximately 1 year of daily trading data (~240–250 records).


## (4) Methodology
Data Preprocessing: 
- Converted date column to datetime format and set it as index
- Checked and handled missing values
- Sorted data for time series consistency
  
Exploratory Data Analysis (EDA):
- Visualized closing price trend over time
- Observed volatility and fluctuations in stock prices

Model Building
- Conducted ADF test to check stationarity
- Applied differencing to make data stationary
- Used ACF and PACF plots to determine ARIMA parameters
- Built ARIMA(1,1,1) model

Evaluation
- Evaluated model using RMSE
- Analyzed AIC value for model performance
- Checked residual behavior

## (5) Results
Metrics:
```
RMSE: 92.742
AIC: 2944.6
```

Insights:
- The stock exhibited significant fluctuations over the observed period
- The ARIMA model captured short-term patterns but showed moderate accuracy
- The forecast indicated stability with minor fluctuations, suggesting no strong upward or downward trend in the next 30 days
- The model is suitable for short-term forecasting but may not capture long-term market movements accurately

## (6) How to Run
```bash
pip install -r requirements.txt
python main.py
```

## (7) Conclusion
The analysis of DIVISLAB stock prices over the past year revealed a highly volatile pattern with frequent fluctuations and no consistent long-term trend. The Augmented Dickey-Fuller (ADF) test indicated that the series was weakly stationary, and first-order differencing was applied to improve model stability.

An ARIMA(1,1,1) model was developed to capture the time series behavior. While the model demonstrated moderate performance, it was effective in identifying short-term patterns in the data.

The 30-day forecast suggests that the stock price is likely to remain relatively stable with minor fluctuations, showing no strong upward or downward trend. This reflects the inherent uncertainty and volatility of financial markets, where short-term movements are difficult to predict with high accuracy.

## (8) Student's details
- Name: Munazza Sayed
- Roll No: 53
- UIN: 231A046
- YEAR: TE-AIDS
