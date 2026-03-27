# Home Sales Analysis with PySpark

## Overview
In this challenge I use **PySpark and SparkSQL** to analyze home sales data. The goal is to determine key metrics, improve query performance using caching and paritioning, and understand how these techniques impact runtime.

The analysis includes calculating average home prices by different criteria, caching temporary tables, and paritioning Parquet data for optimized queries.

## SparksSQL Analysis
Using SparkSQL, answer the following questions:
* Average price for four-bedroom homes by year
* Average price by year built for homes with three bedrooms and three bathrooms
* Average price by year built for homes with three bedrooms, three bathrooms, two floors, and ≥ 2,000 sq ft
* Average price per "view" rating for homes ≥ #350,000
  * Record query runtime for comparison
 
## Cache and Compare
* Cache the `home_sales` temporary table
* Verify that the table is cached
* Run the query for average price per "view" rating using cached data
* Compare the runtime to the uncached query

## Parition Parquet Data
* Save formatted home sales data as Parquet, partitioned by `date_built`
* Create a temporary table for the Parquet data
* Run the "average price per view rating ≥ $350,000" query
* Compare runtime to previous uncached query

## Uncache and Verify
* Uncache the `home_sales` temporary table
* Verify that the table is no longer cached using PySparks
