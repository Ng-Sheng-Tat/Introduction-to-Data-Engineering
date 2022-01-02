## Week 2
A data engineer’s ecosystem includes the **infrastructure, tools, frameworks, and processes for extracting data** from disparate sources, **architecting and managing data pipelines for transformation, integration, and storage of data**, **architecting and managing data repositories**, **automating and optimizing workflows and flow of data between systems**; and **developing applications needed through the data engineering workflow**.

**Data**
1. Structured - organized into rows and columns
2. Semi-structured - hybrid like emails, html, zipped files, etc
3. Unstructured - video, audio, pdf, etc

**Data Repositories**
1. **Transactional or Online Transaction Processing (OLTP) System**
  - designed to store high volume day-to-day operational data
  - typically relational, but can be non-relational
2. **Analytical or Online Analytical Processing (OLAP) Systems**
  - optimized for conducting complex data analytics
  - include relational and non-relational databases, data warehouses, data marts, data lakes, and big data stores

**Data Integration**
1. Data Collection
2. Processed Data
3. Cleansed Data
4. Integrated Data
5. Users use data

**Languages**
1. Query Languages
  - SQL
2. Programming Languages
  - Python, R, Java
3. Shell and Scripting Languages
  - for repetitive operational tasks
  - power shell, linux/unix shell

**Reporting tools** like real time tableau

**Data Format**
1. JSON
2. CSV/TSV (flat file)
3. Excel Spreadsheet
4. XML
5. PDF

**Data Sources** such as Relational Databases; Flatfiles and XML Datasets APIs and Web Services; Web Scraping; Data Streams and Feeds.
---
**What is metadata?**
Metadata is **data that provides information about other data**.

Let us consider the concept of metadata within the context of databases, data warehousing, business intelligence systems, and all kinds of data repositories and platforms.

We'll consider the following three main types of metadata:
1. **Technical metadata**
2. **Process metadata**
3. **Business metadata**

**Technical metadata**
Technical metadata is metadata which **defines the data structures in data repositories or platforms, primarily from a technical perspective.** For example, technical metadata in a data warehouse includes assets such as:

- Tables that record information about the tables stored in a database, like:
  - each table's name
  - the number of columns and rows each table has
- A data catalog, which is an inventory of tables that contain information, like:
  - the name of each database in the enteprise data warehouse
  - the name of each column present in each database
  - the names of every table that each column is contained in
  - the type of data that each column contains

The technical metadata for relational databases is typically stored in specialized tables in the database called the System Catalog.

**Process metadata**
Process metadata **describes the processes that operate behind business systems such as data warehouses, accounting systems, or customer relationship management tools**.Many important enterprise systems are responsible for collecting and processing data from various sources. Such critical systems need to be monitored for failures and any performance anomalies that arise. Process metadata for such systems includes tracking things like:
- process start and end times
- disk usage
- where data was moved from and to, and
- how many users access the system at any given time
This sort of data is invaluable for troubleshooting and optimizing workflows and ad hoc queries.

**Business metadata**
Users who want to **explore and analyze data within and outside the enterprise are typically interested in data discovery**. They need to be able to find data which is meaningful and valuable to them and know where that data can be accessed from. These business-minded users are thus interested in business metadata, which is information about the data described in readily interpretable ways, such as:
- how the data is acquired
- what the data is measuring or describing
- the connection between the data and other data sources
Business metadata also serves as documentation for the entire data warehouse system.

**Managing metadata**
Managing metadata includes **developing and administering policies and processes to ensure information can be accessed and integrated from various sources and appropriately shared across the entire enterprise**. **Creation of a reliable, user-friendly data catalog** is a primary objective of a metadata management model. The data catalog is a core component of a modern metadata management system, serving as the main asset around which metadata management is administered. It serves as the basis by which companies can inventory and efficiently organize their data systems. A modern metadata management model will include a web-based user interface that enables engineers and business users to easily search for and find information on key attributes such as CustomerName or ProductType. This kind of model is central to any Data Governance initiative.

**Why is metadata management important?**
Good metadata management has many valuable benefits. **Having access to a well implemented data catalog greatly enhances data discovery, repeatability, governance, and can also facilitate access to data.** Well managed metadata helps you to understand both the business context associated with the enterprise data and the data lineage, which helps to improve data governance. Data lineage provides information about the origin of the data and how it gets transformed and moved, and thus it facilitates tracing of data errors back to their root cause. Data governance is a data management concept concerning the capability that enables an organization to ensure that high data quality exists throughout the complete lifecycle of the data, and data controls are implemented that support business objectives.

The key focus areas of data governance include **availability, usability, consistency, data integrity and data security** and includes establishing processes to ensure effective data management throughout the enterprise such as accountability for the adverse effects of poor data quality and ensuring that the data which an enterprise has can be used by the entire organization.

**Popular tools for metadata management**
Popular metadata management tools include:
- IBM InfoSphere Information Server
- CA Erwin Data Modeler
- Oracle Warehouse Builder
- SAS Data Integration Server
- Talend Data Fabric
- Alation Data Catalog
- SAP Information Steward
- Microsoft Azure Data Catalog
- IBM Watson Knowledge Catalog
- Oracle Enterprise Metadata Management (OEMM)
- Adaptive Metadata Manager
- Unifi Data Catalog
- data.world
- Informatica Enterprise Data Catalog

**Summary**
Metadata is data that provides information about other data, and includes three main types: technical, process, and business metadata
The technical metadata for relational databases is typically stored in specialized tables in the database called the system catalog
A primary objective of business metadata management modelling is the creation and maintenance of a reliable, user-friendly data catalog
Having access to a well-implemented data catalog greatly enhances data discovery, repeatability, governance, and can also facilitate access to data. Metadata management tools from IBM include InfoSphere Information Server and Watson Knowledge Catalog.
---
**Data Repository** is a general term used to refer to data that has been collected, organized, and isolated.  The types include:
1. **Databases**
  - collection of data for input, storage, search, retrieval, and modification of data
  - Database Management System (DBMS) is a set of programs for creating and maintaining the database, and storing, modifying, and extracting information from the database through **querying** function.
  - types of database used influence by data type, data structure, querying mechanisms, latency requirements, transaction speeds, intended use of data
  - Relational Database Management System (RDBMS)
    1. data is organized into tabular format
    2. well defined structure and schema
    3. optimized for data operation and querying
    4. use SQL as querying languages
  - Non-Relational Database Management System (NoSQL)
    1. Emerged in response to the volume, density, and speed at which data is being generated today
    2. built for speed, flexibility, and scale
    3. data can be stored in a schema-less form
    4. widely used for processing big data
2. **Data Warehouses**
  - consolidates data though ETL process into one comprehensive database for analytics, and business intelligence
3. **Big Data Stores**
  - distributed computational and storage infrastructure to store, scale, and process very large data sets.
Overall, data repositories help to isolate data and make reporting and analytics more efficient and credible while also serving as a data archive.
---
**Relational Database (RDBMS)**
- records as rows, attributes as columns

**Advantages**
1. Create meaningful information
2. Flexibility for changes
3. Minimize data redundancy
4. Ease of backup and disaster recovery
5. Accuracy, Reliability in database transactions (ACID) compliant

**Well Suited for**
1. OLTP application
2. Data warehouse by optimizing OLAP
3. IoT solutions

**Limitation**
- does not work well with unstructured data
- migration between two database is possible only when the source and destination tables have identical schemas and data types
- entering a value greater than the defined length of a data field results in loss of information
---
**Non-relational database management system (NoSQL)**
- data stored in a schema-less and free-form fashion
1. Key-Value store
  - uses key value pairs
2. Document-based
  - each data is stored in a single document
3. Column-based
  - data stored in cells grouped as columns of data instead of rows
4. Graph-based
  - uses graphical model to represent and store data

**Advantages**
1. ability to handle large volumes of all structed of data
2. ability to run as a distributed system scaled across multiple data centers
3. efficient and cost-effective scale-out architecture that provides additional capacity and performance with addition of new nodes
4. simpler design, better control over availability, and improved scalability that makes it agile, flexible, and support quick iterations.
---
**Data Warehouse**
- after data is Cleansed and stored in a data warehouse
- has 3-tier architecture
  1. Client Front-End Layer
  2. OLAP Server
  3. Database Servers

**Data Marts** is a sub-section of the data warehouse, built specifically for a particular business function, purpose, or community of users.
- used to provide data to users
- accelerate business process
- provide a cost and time efficient way in which data-driven decisions can be taken
- improves end-user response time

**Data Lakes**
- store large amounts of data in their native format
- can be loaded without defining the schema and structure of the data
- exist as a repository of raw data straight from the source, to be transformed based on the use case
- data is classified, protected, and governed
- as a reference architecture that combines multiple technologies
---
**Extraction, Transform, and Load Process (ETL)**
Extraction can be through
1. batch processing
2. stream processing

Loading is classified into
1. Initial loading
2. Incremental loading
3. Full refresh
- load verification checks for missing or null values, server performance, and load failures

Sometimes, ELT process is used as it helps to process large data sets of unstructured and non-relational data. It is ideal for data lakes. The advantages include:
1. Shorten the cycle between extraction and delivery
2. Allows to ingest volumes of raw data as immediately as the data becomes available
3. Affords greater flexibility for data analysis
4. Transform only that data

**Data pipelines** encompasses the entire journey of moving data from one system to another.
---
**Data Integration** is a discipline comprising the practices, architectural techniques, and tools that allow organizations to ingest, transform, combine, and provision data across various data types. It is the entire process after extraction of data from multiple sources and before data warehousing. The ETL process is incorporated in the data integration step. It includes
1. accessing, queueing, or extracting data from operational systems
2. transforming and merging extracted data either logically or physically
3. data quality and governance
4. delivering data through an integrated approach for analytics purposes.
---
A Data Repository is a general term that refers to data that has been collected, organized, and isolated so that it can be used for reporting, analytics, and also for archival purposes.

The different types of Data Repositories include:

Databases, which can be relational or non-relational, each following a set of organizational principles, the types of data they can store, and the tools that can be used to query, organize, and retrieve data.

Data Warehouses, that consolidate incoming data into one comprehensive store house.

Data Marts, that are essentially sub-sections of a data warehouse, built to isolate data for a particular business function or use case.

Data Lakes, that serve as storage repositories for large amounts of structured, semi-structured, and unstructured data in their native format.

Big Data Stores, that provide distributed computational and storage infrastructure to store, scale, and process very large data sets.

The ETL, or Extract Transform and Load, Process is an automated process that converts raw data into analysis-ready data by:

Extracting data from source locations.

Transforming raw data by cleaning, enriching, standardizing, and validating it.

Loading the processed data into a destination system or data repository.

The ELT, or Extract Load and Transfer, Process is a variation of the ETL Process. In this process, extracted data is loaded into the target system before the transformations are applied. This process is ideal for Data Lakes and working with Big Data.

Data Pipeline, sometimes used interchangeably with ETL and ELT, encompasses the entire journey of moving data from its source to a destination data lake or application, using the ETL or ELT process.

Data Integration Platforms combine disparate sources of data, physically or logically, to provide a unified view of the data for analytics purposes.
---
**Big Data**
It refers to the dynamic, large and disparate volumes of data being created by people, tools, and machines. The 5Vs in big data
1. Velocity
2. Veracity
  - fast and accuracy
  - consistency
  - completeness
  - integrity
  - ambiguity
3. Volume
4. Variety
5. Value
---
Big Data refers to the vast amounts of data that is being produced each moment of every day, by people, tools, and machines. The sheer velocity, volume, and variety of data challenged the tools and systems used for conventional data, leading to the emergence of processing tools and platforms designed specifically for Big Data.

Big Data processing technologies help derive value from big data. These include NoSQL databases and Data Lakes and open-source technologies such as Apache Hadoop, Apache Hive, and Apache Spark.

Hadoop provides distributed storage and processing of large datasets across clusters of computers. One of its main components, the Hadoop File Distribution System, or HDFS, is a storage system for big data.

Hive is a data warehouse software for reading, writing, and managing large datasets.

Spark is a general-purpose data processing engine designed to extract and process large volumes of data. 
