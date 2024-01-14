# Capstone projects completed during Data Engineering Boot camp

## [Analysis of Stock Market Trends using Python and Airflow on GCP](https://github.com/meetapandit/stock_market_trends)

Tech Stack: Python, pandas, Google Cloud Platform, Plotly dash

- Downloaded 20+ years of stock market data from AlphaVantage API in JSON format and scraped 500+ stock symbols from the StockAnalysis site to scale up the dataset
- Transformed dataset using pandas to remove metadata from the beginning of dataset and added columns like stock_symbol, week start date, week end date, year, and week number
- Added time ranges to analyze data by last week, last month, last 3 months, 6 months, YTD, and 52 week
- Computed rolling mean, exponential rolling mean, and Bollinger bands to assist users in analyzing stock trends along with time range filters
- Developed an interactive dashboard using Plotly Dash (python library) and deployed the application to Google Cloud Platform


## [Real-time Data Streaming using Kafka](https://github.com/meetapandit/kafka_streaming_user_creation)

Tech Stack - Airflow, Docker, Apache Kafka, Apache Spark, Cassandra

- Built an end-to-end data ingestion and enrichment pipeline for extracting user profile data from randomuser.me API and scheduled DAG in Airflow
- Set up a Kafka cluster on Zookeeper including schema registry for keeping track of schema changes and control center for monitoring the streaming of events in the cluster
- Consumed the data into Spark for processing and stored the transformed records in Cassandra table for downstream analysis
- Containerized all components in Docker for ease of deployment and scaling

## [Equity Market analysis](https://github.com/meetapandit/equity_market_analysis)

Tech Stack - Airflow, Python, Apache Spark

- Built end-to-end data pipeline from ingestion of disparate data sources with different formats to Google Cloud Storage
- Stored partitioned the data by day as parquet files for ease of storage and retrieval for further processing
- Joined the 2 datasets using Spark utilizing partitions and broadcast join to avoid shuffling of data across worker nodes
- Computed latest stock price, prior day closing price, and 30-min moving average price using SparkSQL window functions while storing intermediate results to Hive metastore
- Triggered Airflow DAGs using Python Operator for raw data extraction and Bash Operator for submitting Spark jobs to driver program for transformation
- Created ETL load and analytical load jobs for extraction and creating new metrics respectively
