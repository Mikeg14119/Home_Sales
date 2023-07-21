PySpark SQL Assignment ReadMe


This repository contains the code and data for a PySpark SQL assignment. In this assignment, we perform various data manipulation and analysis tasks using PySpark SQL functions on a dataset of home sales.

Getting Started

Environment Setup: Make sure you have Apache Spark installed and the necessary environment variables set up, such as SPARK_HOME and HADOOP_HOME.

Dependencies: The assignment requires Python with PySpark. 

You can install PySpark using pip:

pip install pyspark


Data: The data used in this assignment is in the file home_sales_revised.csv. This CSV file contains information about home sales, including the number of bedrooms, bathrooms, floors, square footage, price, and the year the home was built.


Steps to Run the Assignment


Importing Necessary Libraries: In the Jupyter Notebook or Python script, the first step is to import the required PySpark SQL functions.

Reading Data into Spark DataFrame: We read the home_sales_revised.csv data into a Spark DataFrame using the read function from pyspark.sql module.

Creating a Temporary Table: We create a temporary table named home_sales from the DataFrame, which allows us to query the data using SparkSQL.

Question 1: Average Price for Four-Bedroom Houses per Year: We answer the first question by calculating the average price for four-bedroom houses sold each year using SparkSQL aggregation functions.

Question 2: Average Price for 3-Bedroom, 3-Bathroom Houses per Year Built: We answer the second question by calculating the average price for three-bedroom, three-bathroom houses for each year they were built.

Question 3: Average Price for 3-Bedroom, 3-Bathroom, 2-Floor Houses with >= 2,000 Sq. Ft.: We answer the third question by calculating the average price for three-bedroom, three-bathroom houses with two floors and a size greater than or equal to 2,000 square feet.

Question 4: "View" Rating for Homes with Price >= $350,000: We find the "view" rating for homes with a price greater than or equal to $350,000 and measure the query's runtime.

Caching the Temporary Table: We cache the home_sales temporary table to improve query performance for repetitive analyses.

Checking if the Table is Cached: We verify if the home_sales table is indeed cached using PySpark SQL functions.

Querying Cached Data: We run the query again using the cached data to find "view" ratings with an average price greater than or equal to $350,000. We measure the runtime and compare it with the uncached version to demonstrate caching benefits.

Partitioning the Formatted Parquet Data: We partition the formatted parquet home sales data by the date_built field for better data organization and query performance.

Creating a Temporary Table for Parquet Data: We create a temporary table for the parquet data to perform further analyses.

Querying Parquet Data: We run the query to find "view" ratings with an average price greater than or equal to $350,000 using the parquet data. We measure the runtime and compare it with the uncached version to demonstrate the benefits of using parquet format.

Uncaching the Temporary Table: We uncache the home_sales temporary table after finishing all analyses.

Verifying if the Table is Uncached: We verify that the home_sales temporary table is indeed uncached using PySpark SQL functions.


Conclusion


This assignment demonstrates the use of PySpark SQL functions to manipulate and analyze a dataset of home sales. We perform various queries and aggregations to answer specific questions related to home prices, bedrooms, bathrooms, floors, and square footage. Additionally, we explore the benefits of caching and using parquet data format for improving query performance in PySpark.
