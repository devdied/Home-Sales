# Home-Sales
In this SparkSQL project, we analyze home sales data to derive key metrics:

* Calculate the average price for four-bedroom houses sold each year.
* Determine the average price of homes by year built, with three bedrooms and three bathrooms.
* Find the average price of homes with specific criteria: three bedrooms, three bathrooms, two floors, and at least 2,000 square feet.
* Calculate the average "view" rating for homes priced at or above $350,000.
* Evaluate the impact of caching on query runtimes and explore partitioning for optimized data processing.
* The project is implemented using PySpark SQL, and results are rounded to two decimal places. Code and analysis are available in the provided Home_Sales.ipynb notebook, with data sourced from the home_sales_revised.csv file.

## Description 
- Parquet:
Columnar Format: Parquet is a columnar storage format, which means it stores data column by column rather than row by row. This format is highly efficient for analytics queries because it allows for column pruning (only reading necessary columns) and better compression of data within each column.

- Cached Data:
In-Memory: Caching data in memory means keeping frequently accessed data in RAM. When you cache data, you avoid reading it from disk repeatedly, which can significantly speed up queries.

Cache or Parquet?

- Data Size: For small to medium-sized datasets that can fit in memory, caching data can provide excellent performance. It's suitable for interactive queries where low latency is critical.

- Big Data: For very large datasets that don't fit in memory, Parquet, with its columnar storage and partitioning, is often a better choice. It reduces the amount of data read from disk and optimizes query performance.

- Use Case: Consider the specific use case. If you have complex analytical queries on large datasets, Parquet is likely the better option. If you need sub-millisecond response times for simple lookups, caching might be sufficient.

- Infrastructure: Consider the capabilities of your infrastructure. Modern data warehouses and data lakes often support optimized Parquet querying, making it a natural choice for big data analytics.

## Results 
I performed the analysis on a small dataset where Cache had a better performance in comparison to Parquet.


