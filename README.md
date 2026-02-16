# Healthcare-Data-Platform---Azure-Medallion-Architecture
<h2>Project Overview</h2>
This project implements a modern healthcare analytics platform built on Microsoft Azure using a Medallion Architecture (Bronze → Silver → Gold).
The solution ingests healthcare data from multiple sources, processes it using Azure data services, and delivers curated insights through Power BI Embedded dashboards.

## Architecture Diagram

![Healthcare Architecture](Healthcare-architecture.png)


## Data Sources
<ul>
<li>MySQL → Hospital_TB</li>
<li>Azure Cosmos DB → claims.json</li>
<li>Azure Blob Storage →

disease.csv

group.csv

subgroup.csv

patient.csv

subscriber_record.csv</li>
  
</ul>

## Data Ingestion

Azure Data Factory orchestrates data movement:

Extracts data from MySQL, Cosmos DB, and Blob Storage

Loads raw data into the data lake

## Storage Layer

Azure Data Lake Storage Gen2

Central storage for raw and processed datasets

Supports structured & semi-structured data

## Data Processing & Transformation

Azure Databricks performs data engineering workflows using Spark.

<h3> 🥉 Bronze Layer</h3>

Raw ingestion

Data stored as-is

Schema preservation

<h3>🥈 Silver Layer</h3>

Data cleansing & validation

Handling missing values & duplicates

Standardization & schema enforcement

<h3> 🥇 Gold Layer </h3>

Aggregated & business-ready datasets

Optimized for analytics & reporting
