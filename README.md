# Jay-Zz Entertainment Data Streaming and Analysis Project

![Alt text](https://memgraph.com/images/blog/develop-smarter-by-uncovering-insights-inside-data-streams-memgraph-cloud-lab/cloud-release-blog-post-2.png)

## Overview

This project aims to provide Jay-Zz Entertainment with a comprehensive solution for real-time analysis and recommendations based on movie critiques. The system is designed to stream and process movie critique data using Kafka, transform and store it in Memgraph, and enable efficient real-time analysis using Cypher queries. The development environment is containerized using Docker and Docker Compose for seamless deployment.

## Table of Contents

- [Installation and Configuration](#installation-and-configuration)
- [Integration and Configuration of Kafka](#integration-and-configuration-of-kafka)
- [Development of the Transformation Module](#development-of-the-transformation-module)
- [Data Processing with Memgraph](#data-processing-with-memgraph)
- [Analysis and Cypher Queries](#analysis-and-cypher-queries)
- [GDPR Compliance and Data Governance](#gdpr-compliance-and-data-governance)

## Project Structure 

```
Entertainment Data Streaming and Analysis Project/
|-- .gitignore
|-- README.md
|-- docker-compose.yml
|-- deploy/
|   |-- kubernetes/
|       |-- deployment.yaml
|       |-- service.yaml
|-- src/
|   |-- main.go
|   |-- config/
|       |-- config.go
|   |-- kafka/
|       |-- kafka.go
|   |-- transformation/
|       |-- transformer.go
|   |-- memgraph/
|       |-- memgraph.go
|   |-- cypher/
|       |-- queries.go
|-- tests/
|   |-- kafka_test.go
|   |-- transformation_test.go
|   |-- memgraph_test.go
|   |-- cypher_test.go
|-- scripts/
|   |-- initialize.sh
|   |-- start.sh
|   |-- stop.sh
|-- data/
|   |-- sample_data.json
```

## Explanation of each directory/file 
```
.gitignore: Specifies files and directories to be ignored by Git.
README.md: Project documentation.
docker-compose.yml: Configuration file for Docker Compose.
deploy/: Contains deployment-related files for different environments.
    kubernetes/: Kubernetes deployment files.
src/: Main source code directory.
    main.go: Entry point of the application.
    config/: Configuration package.
        config.go: Configuration management.
    kafka/: Kafka-related package.
        kafka.go: Kafka integration code.
    transformation/: Transformation module package.
        transformer.go: Transformation logic.
    memgraph/: Memgraph integration package.
        memgraph.go: Memgraph connection and data processing.
    cypher/: Cypher query package.
        queries.go: Cypher queries.
tests/: Test files for each package.
scripts/: Shell scripts for various tasks.
    initialize.sh: Initialization script.
    start.sh: Script to start the application.
    stop.sh: Script to stop the application.
data/: Directory for storing data related to the project.
    sample_data.json: Sample input data for testing.
```
## Installation and Configuration

- Set up the development environment using Docker and Docker Compose.
- Install Memgraph Lab for visualization and Cypher query execution.

## Integration and Configuration of Kafka

- Configure Kafka for streaming movie critique data.
- Create necessary Kafka topics and ensure proper integration.

## Development of the Transformation Module

- Design and implement a Python module to transform Kafka messages into a format compatible with Memgraph.

## Data Processing with Memgraph

- Configure Memgraph for processing Kafka data streams.
- Create a graph database tailored to the movie critique data model.

## Analysis and Cypher Queries

- Develop Cypher queries for real-time data analysis and movie recommendations.
- Optimize queries for high performance.

## GDPR Compliance and Data Governance

- Ensure system compliance with GDPR, focusing on user consent and personal data protection.
- Implement data governance policies for data quality, security, and integrity.
- Develop and maintain a detailed data catalog for traceability and understanding of data sources.

## Data Input Format

The input data should be modeled in the following format:

```json
{"userId": "365", "movie": { "movieId": "7526", "title": "Lord of the Rings: The Fellowship of the Ring, The (2001)", "genres": ["Adventure", "Fantasy"] }, "rating": "5", "timestamp": "45554125" }
```
