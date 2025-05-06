# Amazon-Prime-Data-Analysis-with-PySpark-on-Databricks-
Amazon Prime Data Analysis with PySpark on Databricks This project demonstrates how to process and analyze the Amazon Prime Titles dataset using Apache Spark (PySpark) in Databricks.



📁 Dataset Used:
amazon_prime_titles.csv

Located at: /FileStore/tables/amazon_prime_titles.csv in DBFS

🔧 Platform & Tools:
Databricks Community Edition

PySpark

DBFS (Databricks File System)


1. Data Ingestion

Loaded CSV using spark.read.format('csv') with header and schema inference.

Inspected schema and displayed the dataset.

2. Data Cleaning

Filled missing values for rating and country with defaults.

Dropped rows with other missing values.

Removed duplicates and renamed columns.

3 .Data Transformation

Created new binary columns: is_movie, is_series.

Split listed_in into an array of categories.

4. Exploratory Analysis

Category distribution using explode + groupBy.

Content count by type, country, release year, and rating.

Created a ranking of top-rated content within each release year using Spark Window functions.

5. Data Output

Saved the transformed data in both Delta and CSV formats:

Delta: /FileStore/processed_delta

CSV: /FileStore/processed_csv
