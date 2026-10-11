# FMCG End-to-End Data Engineering Pipeline

## Project Overview

This project demonstrates an end-to-end data engineering pipeline for FMCG (Fast-Moving Consumer Goods) datasets using AWS S3, Azure Databricks, PySpark, and Delta Lake.

The pipeline is designed to ingest raw data, perform data transformations, organize datasets into Bronze, Silver, and Gold layers, and prepare structured data for analytical reporting.

## Technologies Used

- Cloud Storage: Amazon S3
- Data Processing: Azure Databricks, Apache Spark, PySpark
- Storage Format: Delta Lake
- Programming: Python, SQL
- Architecture: Medallion Architecture (Bronze, Silver, Gold)
- Data Modeling: Dimension and Fact Tables
- Processing:** Full Load and Incremental Load

## Data Pipeline Architecture

AWS S3 (Raw CSV Files)
         |
         v
Databricks Ingestion
         |
         v
Bronze Layer (Raw Data)
         |
         v
Silver Layer (Cleaned Data)
         |
         v
Gold Layer (Analytics-Ready Data)
         |
         v
Dimension and Fact Tables


## Project Components

### 1. Data Ingestion

The pipeline reads FMCG datasets from Amazon S3 using PySpark in Databricks.

Datasets include customer, product, pricing, and order information.

### 2. Bronze Layer

The Bronze layer stores ingested source data and supports metadata tracking for incoming files.

### 3. Silver Layer

The Silver layer prepares source data for downstream processing through transformations and data preparation.

### 4. Gold Layer

The Gold layer provides structured datasets intended for analytical reporting.

The project includes a date dimension table with year, month, quarter, and year-quarter attributes.

### 5. Full Load Processing

The project includes a full-load fact processing notebook for loading source data into the analytical pipeline.

### 6. Incremental Load Processing

The project includes an incremental-load fact processing notebook for handling newly arriving data.

This supports processing additional source files without requiring a complete reload of previously processed datasets.

## Repository Structure

Consolidated pipeline/
|
|-- dimension_data_processing/
|   |-- customer_data_processing.py
|   |-- 2_products_data_processing.py
|   |-- 3_pricing_data_processing.py
|
|-- Fact_data_processing/
|   |-- full_load_fact.py
|   |-- 2_incremental_load_fact.py
|
|-- setup/
    |-- setup_catalogs.py
    |-- Utilities.py
    |-- dim_date_table_creation.py

## Key Learning Outcomes

- Working with AWS S3 and Databricks
- Developing data pipelines using PySpark
- Implementing the Medallion Architecture
- Creating Delta Lake tables
- Understanding full and incremental data processing
- Building analytical dimension and fact tables
- Troubleshooting pipeline execution failures

## Future Enhancements

- Add automated data quality validation
- Implement pipeline monitoring and alerting
- Add an architecture diagram and execution screenshots
- Improve configuration management for deployment

## Project Type

Personal data engineering portfolio project developed for hands-on learning and demonstration of cloud data engineering concepts.
