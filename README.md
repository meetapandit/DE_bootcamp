# Capstone projects completed during Data Engineering Boot camp

## [Analysis of Stock Market Trends using Python and Airflow on GCP](https://github.com/meetapandit/stock_market_trends)
- Downloaded 20+ years of stock market data from AlphaVantage API in json format and scraped 500+ stock symbols from StockAnalysis site to scale up the dataset
- Transformed dataset using pandas to remove metadata from the beginning of dataset and added columns like stock_symbol, week start date, week end date, year, and week number
- Added time ranges to analyze data by last week, last month, last 3 months, 6 months, YTD and 52 week
- Computed rolling mean, exponential rolling mean and Bollinger bands to assist users in analyzing stock trends along with time range filters
- Developed an interactive dashboard using Plotly Dash (python library) and deployed the application to Google Cloud Platform

Tech Stack: Python, pandas, Google Cloud Platform, Plotly dash
