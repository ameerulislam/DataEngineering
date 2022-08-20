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

