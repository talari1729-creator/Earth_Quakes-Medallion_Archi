![project image](https://github.com/talari1729-creator/-Earth_Quakes_Medallion_Archi_Project/blob/dc2b2253067f1b12ab5bfbb9af65ab9d01c5be04/EarthQuakes-Project%20Diagram.png)
Project Description

Project Title: Earthquake Data Engineering Pipeline using Medallion Architecture.

This project demonstrates the implementation of a Medallion Architecture (Ingestion → Bronze → Silver → Gold) to build a scalable, reliable, and analytics-ready data pipeline for earthquake data. The source dataset, EarthQuakes.csv, contains information about earthquake events such as occurrence time, location, latitude, longitude, depth, magnitude, and other seismic attributes.

To solve this challenge, an end-to-end data engineering platform was developed using Azure Data Factory (ADF) for orchestration, Azure Databricks (ADB) for transformations, Azure Data Lake Storage Gen2 (ADLS) for storage, and Delta Lake with Medallion Architecture for data processing. The solution ingests data from five different source systems, stores raw data in the Bronze layer, transforms and standardizes it in the Silver layer, and creates business-ready Gold datasets for reporting, analytics, machine learning, and executive dashboards.


Source System->National Earthquake Information Center (NEIC)

Project Context

The National Earthquake Information Center (NEIC) determines the location and size of all significant earthquakes that occur worldwide and disseminates this information immediately to national and international agencies, scientists, critical facilities, and the general public. The NEIC compiles and provides to scientists and to the public an extensive seismic database that serves as a foundation for scientific research through the operation of modern digital national and global seismograph networks and cooperative international agreements. The NEIC is the national data center and archive for earthquake information.

Project Content

This dataset includes a record of the date, time, location, depth, magnitude, and source of every earthquake with a reported magnitude 5.5 or higher since 1965.


Project Business Objectives

->Build an end-to-end data engineering pipeline using Medallion Architecture.
->Ingest raw earthquake data while maintaining data integrity.
->Clean and standardize the dataset to improve data quality.
->Transform raw records into analytics-ready datasets.
->Generate aggregated business metrics for reporting and visualization.
->Enable efficient querying and dashboard creation using curated Gold tables.

Folder Structure

                                       
│ Earthquake_Project
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
└── README.md


Architecture Flow

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
      (Cleaned & Standardized)
                     │
                     ▼
               Gold Layer
    (Business & Analytical Tables)
                     │
                     ▼
        Power BI / Tableau / SQL

Data Flow

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
     │
     ▼
Power BI Dashboard

