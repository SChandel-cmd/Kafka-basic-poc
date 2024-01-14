
# Project Title: Real-time Stock Market Data Streaming and Analysis

## Overview

This project aims to simulate a real-time streaming setup for stock market data using AWS services, Kafka, and Python. The workflow involves deploying Kafka on an EC2 instance, generating stock market data in real-time using a Python notebook as a Kafka producer, consuming this data with another Python notebook acting as a Kafka consumer, and storing the processed data in an S3 bucket. Additionally, a crawler is used to automatically populate an Athena table for easy querying.

## Setup Instructions

### 1. Kafka Server Deployment on EC2

- Launch an EC2 instance on AWS.
- Install and configure Kafka on the EC2 instance.

### 2. Kafka Producer Setup

- Use a Python notebook to create a Kafka producer.
- Read a stock market CSV file and send a random entry per second to the Kafka topic.

### 3. Kafka Consumer Setup

- Utilize another Python notebook to create a Kafka consumer.
- Consume data from the Kafka topic and write each entry to individual files on a specified S3 location.

### 4. S3 Storage

- Create an S3 bucket on AWS to store the processed data.

### 5. Athena Table and Crawler

- Set up an Athena table to query the data stored in the S3 bucket.
- Create a crawler to automatically populate the Athena table with the streaming data.

## Usage

1. **Kafka Producer:**
   - Open `KafkaProducer.ipynb` in a Jupyter notebook environment.
   - Run the notebook to start generating and sending stock market data to the Kafka topic.

2. **Kafka Consumer:**
   - Open `KafkaConsumer.ipynb` in a Jupyter notebook environment.
   - Run the notebook to consume data from the Kafka topic and write it to S3.

3. **Athena Querying:**
   - Use Athena to run SQL queries on the data stored in the S3 bucket.

## Dependencies

- Python 3.x
- Apache Kafka
- Jupyter notebook
- AWS SDK for Python (Boto3)
- Athena

## Acknowledgments

- Special thanks to the open-source community and the AWS team for providing the tools and resources necessary for this project.
