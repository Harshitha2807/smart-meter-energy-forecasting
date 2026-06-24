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

<img width="472" height="610" alt="image" src="https://github.com/user-attachments/assets/0e787470-bb04-41e3-8003-28504d499f86" />

<img width="1492" height="605" alt="image" src="https://github.com/user-attachments/assets/f7272e83-60ee-46a8-ae5a-da97b28cf84f" />

14-day historical chart + today's observed vs predicted bar chart

<img width="1570" height="576" alt="image" src="https://github.com/user-attachments/assets/59bd8cd6-563f-4f04-9049-06cea5921ba2" />

<img width="1582" height="566" alt="image" src="https://github.com/user-attachments/assets/52d1fd36-e3d9-4c20-8d1f-f4e68574ddb1" />

Accuracy summary for all 41+ consumers

<img width="1760" height="585" alt="image" src="https://github.com/user-attachments/assets/0ddcfabe-28c5-4b01-a778-421937b3baf6" />

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





