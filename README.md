Smart Meter Energy Consumption Forecasting

A Python-based forecasting system that predicts hourly electricity consumption for industrial and commercial consumers using live smart meter data.

What This Project Does


Fetches real-time hourly consumption data from the smart meter API
Cleans and preprocesses the data (removes outliers, fills gaps)
Tests multiple forecasting strategies and picks the best one per consumer
Predicts remaining hours of the current day or any future date
Generates charts and accuracy reports for all consumers


Forecasting Strategies Used


Naive Average / Median — uses the same hour from past weeks
Weighted Recent — gives more importance to recent weeks
Robust Seasonal Naive — outlier-resistant version of naive average
Prophet — Facebook's time series model with daily/weekly/yearly seasonality


The best strategy is automatically selected for each consumer based on lowest sMAPE error.

Outputs


Hourly prediction table for today or any target date
14-day historical chart + today's observed vs predicted bar chart
Accuracy summary for all 41+ consumers
JSON file with observed and predicted values per consumer


Requirements

pandas, numpy, requests, matplotlib, prophet, scikit-learn

Install in Google Colab:

bash!pip install prophet scikit-learn

How to Run


Open the notebook in Google Colab
Update the CONFIG cell with your target MSN and date
Run all cells from top to bottom


Configuration

pythonMSN         = '67000509'    # Consumer meter number
TRAIN_START = '2025-01-01' # Start of training data
TARGET_DATE = '2026-06-20' # Date to forecast



