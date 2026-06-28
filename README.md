![project image](https://github.com/talari1729-creator/-Earth_Quakes_Medallion_Archi_Project/blob/dc2b2253067f1b12ab5bfbb9af65ab9d01c5be04/EarthQuakes-Project%20Diagram.png)
Project Description

Project Title: Earthquake Data Engineering Pipeline using Medallion Architecture

Project Description

This project demonstrates the implementation of a Medallion Architecture (Ingestion → Bronze → Silver → Gold) to build a scalable, reliable, and analytics-ready data pipeline for earthquake data. The source dataset, EarthQuakes.csv, contains information about earthquake events such as occurrence time, location, latitude, longitude, depth, magnitude, and other seismic attributes.

The pipeline begins by ingesting the raw CSV file into the data lake while preserving the original data. The Bronze layer stores the raw dataset without modifications, ensuring data lineage and historical tracking. The Silver layer performs data cleansing, validation, duplicate removal, null-value handling, data type conversion, and feature engineering to improve data quality and consistency. Finally, the Gold layer creates business-ready aggregated tables and analytical datasets that support reporting, dashboards, and decision-making.

The processed data can be visualized in Power BI or other BI tools to analyze earthquake trends, identify regions with high seismic activity, monitor earthquake magnitudes over time, evaluate depth distributions, and generate meaningful insights for researchers, disaster management authorities, and policymakers.

Project Objectives
Build an end-to-end data engineering pipeline using Medallion Architecture.
Ingest raw earthquake data while maintaining data integrity.
Clean and standardize the dataset to improve data quality.
Transform raw records into analytics-ready datasets.
Generate aggregated business metrics for reporting and visualization.
Enable efficient querying and dashboard creation using curated Gold tables.
Architecture
