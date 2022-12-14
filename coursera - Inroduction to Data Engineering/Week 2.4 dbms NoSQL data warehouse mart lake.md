# SQL
A relational database is a collection of data organized into a table structure, where the tables can be linked, or related, based on
data common to each. Tables are made of rows and columns, where
rows are the **“records”**, and the columns the **“attributes”**. 

Let’s take the example of a customer table that maintains data about each customer in a company. The columns, or attributes, in the customer
table are the Company ID, Company Name, Company Address, and Company Primary Phone; and Each row is a customer record. Now let’s understand what we mean by tables being linked, or related, based on data common to each. Along with the customer table, the company also maintains transaction tables that contain data describing multiple individual transactions pertaining to each customer. The columns for the transaction table might include the Transaction Date, Customer ID, Transaction Amount, and Payment Method. 
The customer table and the transaction tables can be related based on the common Customer ID field. You can query the customer table to produce reports such as a customer statement that consolidates all transactions in a given period. This capability of relating tables based on common data enables you to retrieve an entirely new table from data in one or more tables with a single query. It also allows you to understand the relationships among all available data and gain new insights for making better decisions. 

Relational databases use structured query language, or SQL, for querying data. We’ll learn more about SQL later in this course. Relational databases build on the organizational principles of flat files such as spreadsheets, with data organized into rows and columns
following a well-defined structure and schema. But that is where the similarity ends. 

Relational databases, by design, are ideal for the optimized storage, retrieval, and processing of data for large volumes of data, unlike spreadsheets that have a limited number of rows and columns. Each table in a relational database has a unique set of rows and columns and relationships can be defined between tables, which minimizes data redundancy. Moreover, you can restrict database fields to specific data types and values, which minimizes irregularities and leads to greater consistency and data integrity. 

Relational databases use SQL for querying data, which gives you the advantage of processing millions of records and retrieving large amounts of data in a matter of seconds. 

Moreover, the security architecture of relational databases provides controlled access to data and also ensures that the standards and policies for governing data can be enforced. 

Relational databases range from small desktop systems to massive cloud-based systems. They can be either 
- open-source and internally supported, 
- open-source with commercial support, 
- or commercial closed-source systems. 
IBM DB2, Microsoft SQL Server, MySQL, Oracle Database, and PostgreSQL are some of the popular relational databases. 

Cloud-based relational databases, also referred to as Database-as-a-Service, are gaining wide use as they have access to the limitless compute and storage capabilities offered by the cloud. Some of the popular cloud relational databases include 
Amazon Relational Database Service (RDS), Google Cloud SQL, IBM DB2 on Cloud, Oracle Cloud, and SQL Azure. 

RDBMS is a mature and well-documented technology, making it easy to learn and find qualified talent. One of the most significant advantages of the relational database approach is its ability to create meaningful information by joining tables. 

Some of its other advantages include: Flexibility: Using SQL, you can add new columns, add new tables, rename relations, and make other changes while the database is **running and queries are happening.** 

Reduced redundancy: Relational databases minimize data redundancy. For example, the information of a customer appears in a single entry in the customer table, and the transaction table pertaining to the customer stores a link to the customer table. Ease of backup and disaster recovery: 

Relational databases offer easy export and import options, making backup and restore easy. Exports can happen while the database is running, making restore on failure easy. 

Cloud-based relational databases do continuous mirroring, which means the loss of data on restore can be measured in seconds or less. 

ACID-compliance: ACIDstands for Atomicity, Consistency, Isolation, and Durability. And ACID compliance implies that the data
in the database remains accurate and consistent despite failures, and database transactions are processed reliably. 

Now we’ll look at some use cases for relational databases: 

- Online Transaction Processing: OLTP applications are focused on transaction-oriented tasks that run at high rates. Relational databases are well suited for OLTP applications because they can accommodate a large number of users; they support the ability to insert, update, or delete small amounts of data; and they also support frequent queries and updates as well as fast response times. 

Data warehouses: In a data warehousing environment, relational databases can be optimized for online analytical processing (or OLAP), where historical data is analyzed for business intelligence. IoT solutions: Internet of Things (IoT) solutions require speed as well as the ability to collect and process data from edge devices, which
need a lightweight database solution. This brings us to the  limitations of RDBMS: 

RDBMS does not work well with semi-structured and unstructured data and is, therefore, not suitable for extensive analytics on such data. For migration between two RDBMSs, schemas and type of data need to be identical between the source and destination tables. Relational databases have a limit on the length of data fields, which means if you try to enter more information into a field than it can accommodate, the information will not be stored. 

Despite the limitations and the evolution of data in these times of big data, cloud computing, IoT devices, and social media, RDBMS continues to be the predominant technology for working with structured data.

# NoSQL
NoSQL, which stands for “not only SQL,” or sometimes “non SQL” is a non-relational database design that provides flexible schemas for the storage and retrieval of data. NoSQL databases have existed for many years but have only recently become more popular in the era of cloud, big data, and high-volume web and mobile applications. 

They are chosen today for their attributes around scale, performance,and ease of use. It's important to emphasize that the "No" in "NoSQL" is an abbreviation for "not only" and not the actual word "No." 

NoSQL databases are built for specific data models and have flexible schemas that allow programmers to create and manage modern applications. They do not use a traditional row/column/table database design with fixed schemas, and typically not use the structured query language (or SQL) to query data, although some may support SQL or SQL-like interfaces. 

NoSQL allows data to be stored in a schema-less or free-form fashion. Any data, be It structured, semi-structured, or unstructured, can be stored in any record. 

Based on the model being used for storing data, there are four common types of NoSQL databases: 
- Key-value store, 
- Document-based, 
- Column-based, 
- and graph-based. 

## Key-value store: 
Data in a key-value database is stored as a collection of key-value pairs. The key represents an attribute of the data and is a unique identifier. Both keys and values can be anything from
**simple integers or strings to complex JSON documents.** Key-value stores are great for 
- storing user session data and user preferences, 
- making real-time recommendations and targeted advertising, 
- and in-memory data caching. 

However, if you want to be able to query the data on specific data value, need relationships between data values, or need to have multiple unique keys, a key-value store may not be the best fit. 

- Redis, 
- Memcached, 
- and DynamoDB 
are some well-known examples in this category. 
## Document-based: 
Document databasesstore each record and its associated data within a single document. They enable flexible indexing, powerful ad hoc queries, and analytics over collections of documents. Document databases are preferable for 
- eCommerce platforms, 
- medical records storage, 
- CRM platforms, 
- and analytics platforms. 

However, if you’re looking to run complex search queries and multi-operation transactions, a document-based database may not be the best option for you. MongoDB, DocumentDB, CouchDB, and Cloudant are some of the popular document-based databases. 

## Column-based: 
Column-based models store data in cells grouped as columns of data instead of rows. A logical grouping of columns, that is, columns that are usually accessed together, is called a column family. For example, a customer’s name and profile information will most likely be accessed together but not their purchase history. So,customer name and profile information data
can be grouped into a column family. Since column databases store all cells corresponding
to a column as a continuous disk entry, accessing and searching the data becomes very fast. Column databases can be great for systems that require heavy write requests, storing 
- time-series data, 
- weather data, 
- and IoT data. 

But if you need to use complex queries or change your querying patterns frequently, this may not be the best option for you. The most popular column databases are Cassandra and HBase. 

## Graph-based: 
Graph-based databases use a graphical model to represent and store data. They are particularly useful for visualizing, analyzing, and finding connections between different pieces of data. The circles arenodes, and they contain the data. The arrows represent relationships. Graph databases are an excellent choice for working with connected data, which is data that contains lots of interconnected relationships. Graph databases are great for 
- social networks, 
- real-time product recommendations, 
- network diagrams, 
- fraud detection, 
- and access management. 

But if you want to process high volumes of transactions, it may not be the best choice for you, because graph databases are not optimized for large-volume analytics queries. 
- Neo4J and 
- CosmosDB 
are some of the more popular graph databases. 

Advantages of NoSQLNoSQL was created in response to the limitations of traditional relational database technology. The primary advantage of NoSQL is its ability to **handle large volumes of** 
- structured, 
- semi-structured, 
- and unstructured data. 

Some of its other advantages include: 
- The ability to run as distributed systems scaled across multiple data centers, which enables them to take advantage of cloud computing infrastructure; An efficient and cost-effective scale-out architecture that provides additional capacity and performance with the addition of new nodes; and Simpler design, better control over availability,
and improved scalability that enables you to be more agile, more flexible, and to iterate
more quickly 

## To summarize the key differencesbetween relational and non-relational databases: 
**RDBMS** schemas rigidly define how all data inserted into the database must be typed and composed, whereas **NoSQL databases** can be schema-agnostic, allowing unstructured and semi-structured data to be stored and manipulated. Maintaining high-end, commercial relational
database management systems is expensive whereas NoSQL databases are specifically designed
for low-cost commodity hardware Relational databases, unlike most NoSQL, support
ACID-compliance, which ensures reliability of transactions and crash recovery. RDBMS is a mature and well-documented technology, which means the risks are more or less perceivable as compared to NoSQL, which is a relatively newer technology. 
Nonetheless, NoSQL databases are here to stay, and are increasingly being used for mission critical applications.

# Data Warehouses, Data Marts, and Data Lakes
All data mining repositories have a similar goal, which is to house data for reporting, analysis, and deriving insights. 
But their purpose, types of data stored, and how data is accessed differs. In this video, we will learn about some of the characteristics and applications of data warehouses, data marts, and data lakes. 

## A data warehouse 
is a central repository of data integrated from multiple sources. Data warehouses serve as the single source of truth—storing current and historical data that has been cleansed, conformed, and categorized. When data gets loaded into the data warehouse,
it is already modeled and structured for a specific purpose, meaning it's analysis-ready. 

Traditionally, data warehouses are known to store relational data from transactional systems and operational databases such as CRM, ERP, HR, and Finance applications. But with the emergence of NoSQL technologies and new data sources, non-relational data repositories are also being used for data warehousing. Typically, a data warehouse has a **three-tier architecture:** 
- The bottom tier of the architecture includes the database servers, which could be relational, non-relational, or both, that extract data from different sources. 
- The middle tier of the architecture consists of the OLAP Server, a category of software that allows users to process and analyze information coming from multiple database servers. 
- And the top most tier of the architecture includes the client front-end layer. This tier includes all the tools and applications used for querying, reporting, and analyzing data. In response to the rapid data growth and today's sophisticated analytics tools, data warehouses that once resided in on-premise data centers are moving to the cloud. 

Compared to their on-premise versions, some of the benefits offered by cloud-based data warehouses include: 
- Lower costs, 
- Limitless storage and 
- compute capabilities, 
- Scale on a pay-as-you-go basis; 
- and Faster disaster recovery. 

As an organization, you would opt for a data warehouse when you have massive amounts of data from your operational systems that need to be readily available for reporting and analysis. Some of the popularly used data warehouses include 
- Teradata Enterprise 
- Data Warehouse platform, 
- Oracle Exadata, 
- IBM Db2 Warehouse on Cloud, 
- IBM Netezza Performance Server, 
- Amazon RedShift, 
- BigQuery by Google 
- Cloudera's Enterprise Data Hub, 
- and Snowflake Cloud Data Warehouse. 

## A data mart 
is a sub-section of the data warehouse, built specifically for a particular business function, purpose, or community of users. For example, sales or finance groups in an
organization accessing data for their quarterly reporting and projections. 
There are three basic types of data marts
- dependent,
- independent, 
- and hybrid data marts. 

### Dependent data marts
are a sub-section of an enterprise data warehouse. Since a dependent data mart offers analytical capabilities for a restricted area of the data warehouse, it also provides isolated
security and isolated performance. 
### Independent data marts 
are created from sources other than an enterprise data warehouse, such as internal operational systems or external data. 
### Hybrid data marts 
combine inputs from 
- data warehouses, 
- operational systems, 
- and external systems. 

The difference also lies in how data is extracted from the source systems, the transformations that need to be applied, and how the data is transported into the mart. 
### Dependent data marts
for example, pull data from an enterprise data warehouse, where data has already been cleaned and transformed. 
### Independent data marts 
need to carry out the transformation process on the source data since it is coming directly from operational systems and external sources. Whatever the type, the purpose of a data mart is to: 
- provide users' data that is most relevant to them when they need it,
- accelerate business processes by providing efficient response times, provide a cost and time-efficient way in which data-driven decisions can be taken, 
- improve end-user response time; and provide secure access and control. 
## A Data Lake 
is a data repository that can store large amounts of structured, semi-structured, and unstructured data in their native format. While a data warehouse stores data that has been cleaned, processed, and transformed for a specific need, you do not need to define
the structure and schema of data before loading into the data lake. You do not even need to know all of the use
cases for which you will ultimately be analyzing the data. A data lake exists as a repository of raw
data in its native format, straight from the source, to be transformed based on the use
case for which it needs to be analyzed. Which does not mean that a data lake is a
place where data can be dumped without governance. While in the data lake, the data is appropriately
classified, protected, and governed. A data lake is a reference architecture that
is independent of technology. Data lakes combine a variety of technologies
that come together to facilitate agile data exploration for analysts and data scientists. Data lakes can be deployed using Cloud Object
Storage, such as Amazon S3, or large-scale distributed systems such as Apache Hadoop,
used for processing Big Data. They can also be deployed on different relational
database management systems, as well as NoSQL data repositories that can store very large
amounts of data. Data lakes offer a number of benefits, such
as: The ability to store all types of data – unstructured
data such as documents, emails, PDFs, semi-structured data such as JSON, XML, CSV, and logs, as
well as structured data from relational databases The agility to scale based on storage capacity
– growing from terabytes to petabytes of data Saving time in defining structures, schemas,
and transformations since data is imported in its original format and The ability to repurpose data in several different
ways and wide-ranging use cases. This is extremely beneficial as it is hard
for businesses to foresee all the different ways in which you could potentially leverage
their data in the future. Some of the vendors that provide technologies,
platforms, and reference architectures for data lakes include Amazon, Cloudera, Google,
IBM, Informatica, Microsoft, Oracle, SAS, Snowflake, Teradata, and Zaloni. In this video, we learned about some of the
capabilities of data mining repositories such as data warehouses, data marts, and data lakes. While they all have a similar goal, they need
to be evaluated within the context of the use case and technology infrastructure for
selecting the one that works best for an organization’s needs.