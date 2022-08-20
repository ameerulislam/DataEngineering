## Intro
AWS | Big Data | Athena Project | Understanding Athena
Athena is read only service (Query)
pricing $5.00 per TB of data scanned, but pricing can reduced if compresed
https://aws.amazon.com/athena/pricing/

## DDL
DDL is data definition language. It includes sql commands such as
- Create Table
- Delete Table
- Alter Table
- Drop Table
- Truncate Table
Notice DDL is SQL commands that are related to altering the table.

## Presto db
Distributed SQL Query Engine
Engine architecture is similar to MPP (Massive parallel Processing) engine 

## Apache Hive
Apache Hive is a distributed, fault-tolerant data warehouse system that enables analytics at a massive scale. A data warehouse provides a central store of information that can easily be analyzed to make informed, data driven decisions. Hive allows users to read, write, and manage petabytes of data using SQL.

Hive is built on top of Apache Hadoop, which is an open-source framework used to efficiently store and process large datasets. As a result, Hive is closely integrated with Hadoop, and is designed to work quickly on petabytes of data. What makes Hive unique is the ability to query large datasets, leveraging Apache Tez or MapReduce, with a SQL-like interface.

## Presto vs Hive
- Presto is preferably used for performing quick and fast data analysis that will not require very much memory
- Presto is designed for low latency while on the other hand Hive is used for query throughput and queries that require very large amount of memory.
- We can also use both tools to explore data sitting on top of a Hadoop system.
- Apache Hive uses a language similar to SQL, but it still has some differences that BI-Users might need to learn how to write some queries.

## Using Hive and Presto
Presto does not include built in support for the Hadoop file system and it will need to leverage other tools such as Hive connector (aka HCatalog).

One of the strengths of presto is that it’s suitable for star schema models.

In the use case below it shows how to leverage Hive and Presto while working with NoSQL partition parquet tables and file-system data paths.

## Example of How to use Hive and Presto
Let’s say we need to create a view that requires a fact table (parquet data) and multiple small dimension tables.
The ideal logic will be to use Presto, however we can’t explore parquet tables directly with Presto.
We will need other tools such as Hive that allows us create external tables.
With this setup we can read the other file system data sources with Presto.  

Source and more info : https://www.indellient.com/blog/getting-started-with-presto-hive-on-aws/

## Star Schema
Star schemas are specialized data models used when designing data warehouses.
Dimension tables and a Fact table
- dimension Tables define your business entities. Such as product, employee, customer and geography. And within that dimension you have attribute. And beside the regular attributes you have 2 special attribute columns. 
    - Surrogate Key: Is a unique identifier for an object in the database
    - Alternate Key: Is the primary key from the source system. 
Dimension is usually used for grouping and filtering data when you do your analytics.
- Fact Table are used to track specific events/ transactions/ enrollments/ sales. Usually the tables that you want to calculations. 
so fact Tables contains connection to every other Dimension tables. This is a way of doing quick analysis and grouping filtering on fact table data by the dimension tables. 

## 4 Reasons why you should use star schema
- Usuability : things are grouped together in mutliple table it's cleaner instead of having a big table
- Dax (Data Analysis Expressions) is simpler and cleaner: less code
- Performant when you scale of 10s of millions and billions of rows
- Faster Refresh 
sources: 
https://www.youtube.com/watch?v=vZndrBBPiQc
https://docs.microsoft.com/en-gb/power-bi/guidance/star-schema