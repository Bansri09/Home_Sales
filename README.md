# Home Sales Analysis with PySpark

The goal of this challenge is to leverage **Apache Spark** and **SparkSQL** to analyze a large home sales dataset and optimize data querying using various Spark techniques such as caching, partitioning, and temporary views.

---

## Challenge Overview

In this challenge, I used PySpark and SparkSQL to:

- Analyze trends in home sales across different years
- Use temporary views and SQL queries to extract insights
- Apply caching and partitioning techniques to improve performance
- Measure query execution times with and without caching
- Work with parquet-formatted data

---

## Dataset

The dataset, `home_sales_revised.csv`, was loaded directly from an AWS S3 bucket into a PySpark DataFrame and contains sales information such as:
- Bedrooms and bathrooms count
- Price
- Home size (sqft)
- Number of floors
- Year built
- View rating
- Sale date

---

## Key Tasks & Deliverables

| Task | Description |
|------|-------------|
| DataFrame Creation | Loaded CSV into PySpark DataFrame |
| Temp Table Creation | Created temporary view: `home_sales` |
| SQL Query 1 | Calculated average price for **4-bedroom** homes sold each year |
| SQL Query 2 | Found average price of homes with **3 beds and 3 baths** for each year built |
| SQL Query 3 | Found average price for homes with **3 beds, 3 baths, 2 floors, and ≥2000 sqft** |
| SQL Query 4 | Found average price per **view rating**, where avg price ≥ $350,000 (timed) |
| Cache Table | Cached `home_sales` and verified caching |
| Cached Query | Re-ran Query 4 on cached table and measured performance boost |
| Partitioning | Partitioned dataset by `date_built` and saved as parquet |
| Parquet Temp Table | Loaded parquet data and created new temp view |
| Parquet Query | Ran Query 4 again on parquet table (timed) |
| Uncache Table | Uncached `home_sales` and verified uncache success |

---

## Performance Insights

By comparing the execution time of uncached, cached, and partitioned queries, this project highlights the power of **data caching and partitioning** in Spark. These optimizations significantly improve query performance on large datasets.

---
