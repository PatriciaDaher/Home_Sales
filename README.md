# Home_Sales
Using SparkSQL to determine key metrics about home sales data, and Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

# MODULE 22 Challenge

## Home_Sales - Big Data Analysis with SparkSQL
## Patricia Daher
## Overview
This project uses PySpark SQL to analyze a dataset of home sales, answering key metrics about pricing trends. It demonstrates:
Creating temporary views in Spark
Querying data with SparkSQL
Performance optimization via caching and partitioning
Runtime comparison between cached/uncached/partitioned data

## Repository Structure
```
Home_Sales/  
├── Home_Sales.ipynb          # Jupyter Notebook with full analysis  
├── README.md                 # Project documentation
├── LICENSE                   # General Public Lisense

```
## Assignment Workflow
### 1. Data Preparation
Read home_sales_revised.csv from an AWS S3 bucket into a PySpark DataFrame.
Created a temporary view named home_sales for SQL queries.
### 2. Key Queries (SparkSQL)
Average price of 4-bedroom houses per year.
Average price of 3-bedroom, 3-bathroom homes grouped by build year.
Average price of homes with specific filters (3 beds, 3 baths, 2 floors, ≥2000 sqft).
Runtime analysis for a query filtering homes by "view" rating (avg price ≥ $350K).
### 3. Performance Optimization
Caching:
Cached the home_sales table and reran Query 4 to compare runtime.
Partitioning:
Saved data as Parquet files partitioned by date_built.
Created a temporary view from partitioned data and reran Query 4.
Uncaching: Verified the table was uncached successfully.
## Technologies Used
PySpark 3.4.1 (SparkSQL for big data processing)
Jupyter Notebook (Code execution and visualization)
AWS S3 (Data storage)
Parquet (Columnar storage for partitioning)
## How to Run
Prerequisites:
Java 11 (for Spark)
PySpark (pip install pyspark)
Jupyter Notebook
Execution:
Open Home_Sales.ipynb in Google Colab or a local Spark environment.
Run cells sequentially 
## References
Dataset: Provided by edX Boot Camps LLC (for educational purposes).
Spark Documentation: https://spark.apache.org/docs/latest/api/python/