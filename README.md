
# Home_Sales Project

## Overview

In this project, I applied SparkSQL techniques to analyze home sales data. The focus was on creating temporary views, partitioning data, caching and un-caching tables, and evaluating query performance to gain insights into home sales metrics.

## Repository Information

- **Repository Name**: `Home_Sales`
- **GitHub Repository**: [Home_Sales](https://github.com/MAHALELP/Home_Sales)

## Project Files

- **Home_Sales.ipynb**: Jupyter Notebook containing all code and analysis.
- **home_sales_revised.csv**: Dataset used for the analysis.

## Objectives and Accomplishments

### 1. Setup and Data Loading

- **Notebook Initialization**: Renamed `Home_Sales_starter_code.ipynb` to `Home_Sales.ipynb`.
- **Library Imports**: Imported necessary PySpark SQL functions for data processing.
- **Data Ingestion**: Loaded the `home_sales_revised.csv` from the url "https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv"


### 2. Creation of Temporary Table

- **Temporary Table**: Created a temporary table named `home_sales` from the DataFrame to facilitate SQL-based queries.

### 3. Query Analysis

- **Four-Bedroom Houses**: Calculated the average price for four-bedroom houses sold each year, rounding results to two decimal places.
- **Homes with Specific Features**: Determined the average price of homes with three bedrooms and three bathrooms, grouped by the year built, with results rounded to two decimal places.
- **Homes with Additional Criteria**: Analyzed homes with three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet. Computed the average price by the year built, with results rounded to two decimal places.
- **Price per "View" Rating**: Computed the average price per "view" rating for homes with an average price of $350,000 or more, including the runtime of the query, rounded to two decimal places.

### 4. Caching and Performance Evaluation

- **Table Caching**: Cached the `home_sales` temporary table to enhance query performance.
- **Runtime Comparison**: Ran the "view" rating query on both cached and uncached data to compare runtimes.

### 5. Data Partitioning

- **Partitioning**: Partitioned the data by the `date_built` field and saved the dataset in parquet format.
- **Temporary Table for Parquet Data**: Created a temporary table for the partitioned parquet data.
- **Query Performance**: Executed the "view" rating query on the parquet table and compared the runtime with the uncached data.

### 6. Uncaching and Verification

- **Uncaching**: Uncached the `home_sales` temporary table.
- **Verification**: Verified that the table was successfully uncached.

## Conclusion

This project highlights the use of SparkSQL for comprehensive data analysis, including creating temporary views, optimizing performance through caching, and partitioning data. The `Home_Sales.ipynb` notebook provides detailed insights and results from the analysis.

