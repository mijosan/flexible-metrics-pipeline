# Real-Time Metric Collection Pipeline

## Introduction
This project is aimed at setting up a real-time metric collection pipeline using Telegraf, Kafka, Spark, Elasticsearch, InfluxDB, Grafana and Apache Burrow. The pipeline is designed to collect metrics from various sources, process the data in real-time, and display the results on a Grafana dashboard. Additionally, Apache Burrow is used to monitor the Kafka Consumer Lag, and the results are collected by Telegraf and visualized in Grafana.

## Project Architecture
![draw](https://user-images.githubusercontent.com/49933141/218268836-74396a01-1c38-4418-b5c5-f14ce2271643.png)

The project architecture is as follows:
1. Telegraf is used to collect metrics from various sources such as servers, databases and applications.
2. The collected metrics are then sent to a Kafka topic for processing.
3. Spark is used to process the data and store the results in Elasticsearch.
4. The processed data is then sent back to a Kafka topic.
5. InfluxDB is used to store the processed data in a time-series database.
6. Apache Burrow is used to monitor the Kafka Consumer Lag.
7. Telegraf collects the results from Apache Burrow's REST API.
8. Grafana is used to display the data in real-time on a dashboard.

## Components
1. Telegraf: Collects metrics from various sources and the results from Apache Burrow's REST API.
2. Kafka: Used for processing the data.
3. Spark: Processes the data and stores the results in Elasticsearch.
4. Elasticsearch: Stores the processed data.
5. InfluxDB: Stores the processed data in a time-series database.
6. Apache Burrow: Monitors the Kafka Consumer Lag.
7. Grafana: Displays the data in real-time on a dashboard.

## Data Flow
1. Telegraf collects metrics from various sources and sends them to a Kafka topic.
2. Spark processes the data from the Kafka topic and stores the results in Elasticsearch.
3. The processed data is then sent back to a Kafka topic.
4. InfluxDB stores the processed data in a time-series database.
5. Apache Burrow monitors the Kafka Consumer Lag and provides the results through its REST API.
6. Telegraf collects the results from Apache Burrow's REST API.
7. Grafana retrieves the data from InfluxDB and displays it in real-time on a dashboard.

## Project Set-up
To set up the project, follow the steps below:
1. Install and configure Telegraf to collect metrics from various sources and the results from Apache Burrow's REST API.
2. Set up a Kafka cluster and create topics for data processing.
3. Install and configure Spark to process the data from the Kafka topic.
4. Set up Elasticsearch to store the processed data.
5. Install and configure InfluxDB to store the processed data in a time-series database.
6. Install and configure Apache Burrow to monitor the Kafka Consumer Lag.
7. Install and configure Grafana to retrieve the data from InfluxDB and display it in real-time on a dashboard.
