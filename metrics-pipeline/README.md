# Real-Time Metric Collection Pipeline

## Introduction
This project is aimed at setting up a real-time metric collection pipeline using Telegraf, Kafka, Spark, Elasticsearch, InfluxDB and Grafana. The pipeline is designed to collect metrics from various sources and process the data in real-time to be displayed on a Grafana dashboard.

## Project Architecture

The project architecture is as follows:
1. Telegraf is used to collect metrics from various sources such as servers, databases, and applications.
2. The collected metrics are then sent to a Kafka topic for processing.
3. Spark is used to process the data.
4. The processed data is then sent to a Kafka topic.
5. Kafka Connector is used to load the processed data into InfluxDB and Elasticsearch.
6. InfluxDB is used to store the processed data in a time-series database.
7. Elasticsearch stores the processed data.
8. Grafana retrieves the data from InfluxDB and displays it in real-time on a dashboard.

## Components
1. Telegraf: Collects metrics from various sources.
2. Kafka: Used for processing the data.
3. Spark: Processes the data.
4. Kafka Connector: Loads the processed data into InfluxDB and Elasticsearch.
5. InfluxDB: Stores the processed data in a time-series database.
6. Elasticsearch: Stores the processed data.
7. Grafana: Displays the data in real-time on a dashboard.

## Data Flow
1. Telegraf collects metrics from various sources and sends them to a Kafka topic.
2. Spark processes the data from the Kafka topic.
3. The processed data is then sent to a Kafka topic.
4. Kafka Connector loads the processed data into InfluxDB and Elasticsearch.
5. InfluxDB stores the processed data in a time-series database.
6. Elasticsearch stores the processed data.
7. Grafana retrieves the data from InfluxDB and displays it in real-time on a dashboard.

+------------+ +----------+ +------------+
| Telegraf |---->| Kafka |<----->| Spark |
+------------+ +----------+ +------------+
                    |
                    v
           +-----------------+
           | Kafka Connector |
           +-----------------+
                    |
                    v
      +----------+ +---------------+ 
      | InfluxDB | | Elasticsearch |
      +----------+ +---------------+
                   |
                   v
              +----------+
              | Grafana |
              +----------+

## Project Set-up
To set up the project, follow the steps below:
1. Install and configure Telegraf to collect metrics from various sources.
2. Set up a Kafka cluster and create topics for data processing.
3. Install and configure Spark to process the data from the Kafka topic.
4. Set up Elasticsearch to store the processed data.
5. Install and configure InfluxDB to store the processed data in a time-series database.
6. Install and configure Grafana to retrieve the data from InfluxDB and display it in real-time on a dashboard.