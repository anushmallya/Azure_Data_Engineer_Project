# Azure_Data_Engineer_Project

This project demonstrates an end-to-end Azure data engineering built using **Azure Data Factory (ADF), Azure Data Lake Storage Gen2 (ADLS Gen2), and Azure Databricks**.

## 🚀 Project Overview

The pipeline uses **Azure Data Factory** to ingest NYC TLC Trip Record Data from **'https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page'** into the Bronze layer of ADLS Gen2 in Parquet format.

The project processes Green Taxi Trip Record data from 2016 to 2025. The source configuration includes CSV files containing the required data and a JSON file containing the information used to dynamically load the datasets. Azure Data Factory uses this configuration to dynamically process the available source data and ingest it into the Bronze layer.

From the ingested data, the 2025 dataset is selected for processing using Azure Databricks, where the data is cleaned, transformed, and organized into the Silver and Gold layers.

The project follows the Medallion Architecture, separating raw, cleaned, and business-ready data into Bronze, Silver, and Gold layers.

Azure Data Factory is used for data ingestion and pipeline orchestration, while Azure Databricks and PySpark are used for data transformation and processing.

## 🏗️ Architecture

```text
NYC TLC Trip Record Data
         ↓
Azure Data Factory
         ↓
ADLS Gen2 Bronze Layer
         ↓
Azure Databricks Silver Transformation
         ↓
ADLS Gen2 Silver Layer
         ↓
Azure Databricks Gold Transformation
         ↓
ADLS Gen2 Gold Layer
```
## 🛠️ Resources & Technologies Used

- **Microsoft Azure**
- **Azure Data Factory**
- **Azure Data Lake Storage Gen2**
- **Azure Databricks**
- **PySpark**
- **Medallion Architecture**
- **Paruet**
- **Delta Table**

## 🥉 Bronze Layer

The Bronze layer stores the raw data ingested from the NYC TLC data source through Azure Data Factory.
The data is retained in **Parquet format** in ADLS Gen2 before transformation.

## 🥈 Silver Layer

The Silver layer is created using Azure Databricks.

Transformations include:

- Column renaming and standardization
- Datatype handling
- Value standardization
- Dataset-specific transformations
- Cleaning and preparation of data for downstream processing

The transformed data is written back to ADLS Gen2 as the Silver layer.

## 🥇 Gold Layer

The Gold layer contains further transformed and organized data intended for analytical and business use.

Azure Databricks is used to perform the required transformations before storing the resulting data in the Gold layer of ADLS Gen2 in Delta Table format.

## 🎯 Project Objective

The objective of this project is to build a cloud-based data engineering pipeline that demonstrates:

- Data ingestion
- Pipeline orchestration
- Cloud data lake storage
- Distributed data processing
- Data transformation
- Medallion architecture

## 🔗 Connect with Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue)](http://www.linkedin.com/in/anush-mallya-3ba198286)
