Project Over Flow Diagram

![Project Image](https://github.com/talari1729-creator/Earth_Quakes-Medallion_Archi/blob/b94e024092d62cc079b3cfef7881ea135dc55a77/EarthQuakes-Project%20Diagram.png)

Tasks Runs

![tasks runs](https://github.com/talari1729-creator/Earth_Quakes-Medallion_Archi/blob/21a88d4c0361fe7ed99c78e1d5ee544f5ec3a812/Job%20Execution-Task%20Runs.png)

Jobs Execution-Graph

![job execution-grapg](https://github.com/talari1729-creator/Earth_Quakes-Medallion_Archi/blob/8b34d25128706022f3e492fe3025325f4066163b/Job%20Execution-Graph.png)


1.Project Description 

Project Title: Earthquake Data Engineering Pipeline using Medallion Architecture.

This project demonstrates the implementation of a Medallion Architecture (Ingestion → Bronze → Silver → Gold) to build a scalable, reliable, and analytics-ready data pipeline for earthquake data. The source dataset, EarthQuakes.csv, contains information about earthquake events such as occurrence time, location, latitude, longitude, depth, magnitude, and other seismic attributes.

The project also includes production-level components such as centralized logging, validation, audit checks, batch processing, and automated workflow orchestration using Databricks Workflows.

To solve this challenge, an end-to-end data engineering platform was developed using Azure Data Factory (ADF) for orchestration, Azure Databricks (ADB) for transformations, Azure Data Lake Storage Gen2 (ADLS) for storage, and Delta Lake with Medallion Architecture for data processing. The solution ingests data from five different source systems, stores raw data in the Bronze layer, transforms and standardizes it in the Silver layer, and creates business-ready Gold datasets for reporting, analytics, machine learning, and executive dashboards.

2.Tools

Azure Databricks Azure Data Lake Storage Gen2 PySpark Delta Lake Python SQL GitHub Databricks Workflows Table of Contents Project Overview Business Problem Project Objectives Solution Architecture Medallion Architecture Technology Stack Project Folder Structure Source Data Description ADLS Storage Structure Raw Layer Bronze Layer Silver Layer Gold Layer Delta Lake Batch Processing Logger Framework Validation Framework Audit Framework Databricks Workflow Job Scheduling (Cron) Pipeline Execution Screenshots Performance Optimizations Future Enhancements Conclusion References


3.Source System->National Earthquake Information Center (NEIC)

4.Project Context

The National Earthquake Information Center (NEIC) determines the location and size of all significant earthquakes that occur worldwide and disseminates this information immediately to national and international agencies, scientists, critical facilities, and the general public. The NEIC compiles and provides to scientists and to the public an extensive seismic database that serves as a foundation for scientific research through the operation of modern digital national and global seismograph networks and cooperative international agreements. The NEIC is the national data center and archive for earthquake information.

5.Project Content

This dataset includes a record of the date, time, location, depth, magnitude, and source of every earthquake with a reported magnitude 5.5 or higher since 1965.


6.Project Business Objectives

->Build an end-to-end data engineering pipeline using Medallion Architecture.

->Ingest raw earthquake data while maintaining data integrity.

->Clean and standardize the dataset to improve data quality.

->Transform raw records into analytics-ready datasets.

->Generate aggregated business metrics for reporting and visualization.

->Enable efficient querying and dashboard creation using curated Gold tables.


7.Folder Structure

Earthquake_Project/
│
├── data/
│   └── EarthQuakes.csv
│
├── notebooks/
│   ├── 01_Ingestion.py
│   ├── 02_Bronze.py
│   ├── 03_Silver.py
│   └── 04_Gold.py
│
├── tables/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
└── README.md  make this as image    


8.Medallion Architecture Layers and Purposes

1. Ingestion Layer

Definition:
The Ingestion Layer is responsible for collecting data from different source systems and loading it into the data platform without modifying the original data.

Purpose:

->Collect data from source systems

->Preserve raw data

->Prepare data for the Bronze layer

2. Bronze Layer (Raw Layer)

Definition:
The Bronze Layer stores the raw ingested data in its original format with minimal transformations, ensuring that the source data is preserved for future reference.

Purpose:

->Store raw data

->Add basic metadata (Batch ID, Ingestion Timestamp, Source)

->Preserve data lineage

->Serve as the source for the Silver layer

3. Silver Layer (Cleaned Layer)

Definition:
The Silver Layer cleanses, validates, and standardizes the Bronze data by removing duplicates, handling null values, correcting data types, and applying business rules to produce high-quality data.

Purpose:

->Remove duplicates

->Handle null values

->Standardize data formats

->Validate data quality

->Apply business rules

->Generate rejected records and audit reports

->Create clean Delta tables

4. Gold Layer (Business Layer)

Definition:
The Gold Layer contains business-ready, aggregated, and curated data optimized for reporting, dashboards, analytics, and machine learning.

Purpose:

->Create business metrics

->Aggregate and summarize data

->Build reporting tables

->Support BI dashboards and data analysis

->Provide trusted datasets for end users


9.Architecture Flow

EarthQuakes.csv
        │
        ▼
 Ingestion Layer
        │
        ▼
 Bronze Layer
 (Raw Data Storage)
        │
        ▼
 Silver Layer
(Cleaned & Validated Data)
        │
        ▼
  Gold Layer
(Business & Analytics)
        │
        ▼
 Power BI Dashboard

10.Data Flow

CSV File
     │
     ▼
Ingestion
     │
     ▼
Bronze
(Raw Data)
     │
     ▼
Silver
(Cleaned Data)
     │
     ▼
Gold
(Aggregated Analytics)


