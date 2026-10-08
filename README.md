# Databricks_Project

## 📖 General Description

This project is an end-to-end data engineering pipeline built on Databricks, using the Medallion Architecture to turn raw sales data from two source systems (a CRM and an ERP) into an analytics-ready dimensional model. Raw CSV files are ingested into Delta tables, progressively cleaned and standardized, and finally modeled into a star schema that can be consumed directly by BI tools and analytical queries.

The pipeline is implemented with PySpark and Spark SQL in Databricks notebooks, with all tables stored as Delta tables and governed through Unity Catalog. Each layer has a clear responsibility: Bronze keeps the data as close to the source as possible, Silver applies cleaning, type casting and column standardization, and Gold applies the business logic that produces the dimension and fact tables (such as `fact_sales`, joined to the product and customer dimensions through surrogate keys).

## 🏗️ Architecture

This project follows the Medallion Architecture:

### 🥉 Bronze Layer
- Raw data ingestion
- Schema inference and storage as Delta tables

### 🥈 Silver Layer
- Data cleaning and standardization
- Type casting and validation

### 🥇 Gold Layer
- Dimensional Data Model (Business Transformation)
- Ready for BI and analysis

## 🛠️ Technologies Used

- Databricks
- Apache Spark
- PySpark
- Spark SQL
- Delta Lake
- Unity Catalog

## 🙏 Acknowledgements

This project was built based on the material from **Data with Baara**. All credit for the original concept, dataset and teaching content goes to the creator; this repository is my own implementation and adaptation of what I learned from it.
