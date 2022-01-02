## Week 3

**Layers of a Data Platform Architecture**
1. Data Ingestion or Data Collection Layer
2. Data Storage and Integration Layer
3. Data Processing Layer
  - structuring
  - normalization
  - denormalization
  - data cleaning
4. Analysis and User Interface Layer
5. Data Pipeline Layer

**Factors for designing a data store**
1. Types of data
2. Volume of data
3. Intended use of data
  - number of transactions
  - frequency of updates
  - type of operations
  - response time
  - backup and recovery
4. Storage considerations
  - performance
  - availability
  - integrity
  - recoverability of data
5. Privacy, Security, and Governance needs
  - access control
  - multizone encryption
  - data management
  - monitoring systems
---
**Data Security**
**CIA Triad**
1. Confidentiality
2. Integrity
3. Availability
---
1. Physical Infrastructure Security
2. Network Security
3. Application Security
4. Data security
---The architecture of a data platform can be seen as a set of layers, or functional components, each one performing a set of specific tasks. These layers include:

Data Ingestion or Data Collection Layer, responsible for bringing data from source systems into the data platform.

Data Storage and Integration Layer, responsible for storing and merging extracted data.

Data Processing Layer, responsible for validating, transforming, and applying business rules to data.

Analysis and User Interface Layer, responsible for delivering processed data to data consumers.

Data Pipeline Layer, responsible for implementing and maintaining a continuously flowing data pipeline.

A well-designed data repository is essential for building a system that is scalable and capable of performing during high workloads.

The choice or design of a data store is influenced by the type and volume of data that needs to be stored, the intended use of data, and storage considerations. The privacy, security, and governance needs of your organization also influence this choice.

The CIA, or Confidentiality, Integrity, and Availability triad are three key components of an effective strategy for information security. The CIA triad is applicable to all facets of security, be it infrastructure, network, application, or data security.
---
**Data Extraction**
1. Using SQL databases
2. API
3. Web data
4. Sensor Data
5. Exchanges Data
---
**Data Wrangling and Data Munging** is an iterative process that involves data exploration, transformation, validation, and making data available for credible and meaningful analysis.

**Transformation**
- structuring data
- join by attributes
- union of rows/records
- normalization
  - clean unused data, reduce redundancy, reduce inconsistency
- denormalization
  - combine data from multiple tables into a single table for faster querying of data for reports and analysis
- cleaning data
  - fixing irregularities in data in order to produce a credible and accurate analysis

**Inspection**
- detecting issues and errors
- validating against rules and constraints
- profiling data to inspect source data
- visualizing data using statistical methods
- data profiling (source data: structure, content, inter-relationship) -> anomalies and data quality issues.

**Cleaning data**
- missing values
- duplicate data
- irrelevant data
- data type conversion
- standardizing error
- syntax error
- outliers
---
**Tools for data Wrangling**
1. SreadSheet
2. OpenRefine
3. Google DataPrep
4. Watson Studio Refinery
5. Trifacta Wrangler
6. Python (Numpy, Pandas, Jypyter Notebook)
7. R (Dplyr, Data.table, Jsonlite)
---Depending on where the data must be sourced from, there are a number of methods and tools available for gathering data. These include query languages for extracting data from databases, APIs, Web Scraping, Data Streams, RSS Feeds, and Data Exchanges.

Once the data you need has been gathered and imported, your next step is to make it analytics-ready. This is where the process of Data Wrangling, or Data Munging, comes in.

Data Wrangling involves a whole range of transformations and cleansing activities performed on the data. Transformation of raw data includes the tasks you undertake to:

Structurally manipulate and combine data using Joins and Unions.

Normalize data, that is, clean the database of unused and redundant data.

Denormalize data, that is, combine data from multiple tables into a single table so that it can be queried faster.

Cleansing activities include:

Profiling data to uncover anomalies and quality issues.

Visualizing data using statistical methods in order to spot outliers.

Fixing issues such as missing values, duplicate data, irrelevant data, inconsistent formats, syntax errors, and outliers.

A variety of software and tools are available for the data wrangling process. Some of the popularly used ones include Excel Power Query, Spreadsheets, OpenRefine, Google DataPrep, Watson Studio Refinery, Trifacta Wrangler, Python, and R, each with their own set of features, strengths, limitations, and applications.
---
**Basics Querying Functions**
1. Counting
  - ``select (*) from tablename``
  - ``select count(distinct columnname) as newcolumnanme from tablename``
  - sum, avg, stddev, max, min
2. Slicing
  - ``select columnname from tablename where columnname in (,)``
3. Sorting data
  - `` order by columnname``
4. Filtering data
  - ``where columnname like '871%'``
5. Grouping data
  - `` select columnname1, columnname2 from tablename group by columnname``
  ---
  **Data Pipelines**
  1. Performance Threats
    - scalability in the face of increasing data sets and workload
    - application failures
    - scheduled jobs not functioning accurately
  2. Performance Metrics
    - latency
    - failures
    - resource ultilization
    - traffic
  3. Troubleshooting
    - collect information
    - check right versions
    - check logs and metrics
    - reproduce the issues
  4. Optimization for performance
    - system outages
    - capacity utilization
    - application slowdown
    - performance of queries
    - conflicting activities and queries being executed simultaneously
    - batch activities causing resource constraints
    - **capacity planning**
    - **database indexing**
    - **database partitioning**
    - **database normalization**
5. Monitoring system
---
In this lesson, you have learned,

In order for raw data to become analytics-ready, a number of transformation and cleansing tasks need to be performed on raw data. And that requires you to understand your dataset from multiple perspectives. One of the ways in which you can explore your dataset is to query it.

Basic querying techniques can help you explore your data, such as, counting and aggregating a dataset, identifying extreme values, slicing data, sorting data, filtering patterns, and grouping data.

In a data engineering lifecycle, the performance of data pipelines, platforms, databases, applications, tools, queries, and scheduled jobs, need to be constantly monitored for performance and availability.

The performance of a data pipeline can get impacted if the workload increases significantly, or there are application failures, or a scheduled job does not work as expected, or some of the tools in the pipeline run into compatibility issues.

Databases are susceptible to outages, capacity overutilization, application slowdown, and conflicting activities and queries being executed simultaneously.

Monitoring and alerting systems collect quantitative data in real time to give visibility into the performance of data pipelines, platforms, databases, applications, tools, queries, scheduled jobs, and more.

Time-based and condition-based maintenance schedules generate data that helps identify systems and procedures responsible for faults and low availability.
---
**Data Governance** is a collection of principles, practices, and processes to maintain the security, privacy, and integrity.

**Data Lifecycle**
1. Acquisition
2. Processing
3. Sharing
4. Retention and Disposal

**Governance**
1. Authentication and Access Control
2. Encryption and Data Masking
3. Data Erasure
4. Monitoring and Alerting
5. Hosting
---
Data Governance is a collection of principles, practices, and processes that help maintain the security, privacy, and integrity of data through its lifecycle.

Personal Information and Sensitive Personal Information, that is, data that can be traced back to an individual or can be used to identify or cause harm to an individual, needs to be protected through governance regulations.

General Data Protection Regulation, or GDPR, is one such regulation that protects the personal data and privacy of EU citizens for transactions that occur within EU member states.
Regulations, such as HIPAA (Health Insurance Portability and Accountability Act) for Healthcare, PCI DSS (Payment Card Industry Data Security Standard) for retail, and SOX (Sarbanes Oxley) for financial data are some of the industry-specific regulations.

Compliance covers the processes and procedures through which an organization adheres to regulations and conducts its operations in a legal and ethical manner.

Compliance requires organizations to maintain an auditable trail of personal data through its lifecycle, which includes acquisition, processing, storage, sharing, retention, and disposal of data.

Tools and technologies play a critical role in the implementation of a governance framework, offering features such as:

Authentication and Access Control.

Encryption and Data Masking.

Hosting options that comply with requirements and restrictions for international data transfers.

Monitoring and Alerting functionalities.

Data erasure tools that ensure deleted data cannot be retrieved.
***
**DevOps Methodology**
Gartner defines DataOps as a collaborative data management practice focused on improving the communication, integration, and automation of data flows between data managers and consumers across an organization. DataOps aims to create predictable delivery and change management of data, data models, and related artifacts. DataOps uses technology to automate data delivery with the appropriate levels of security, quality, and metadata to improve the use and value of data in a dynamic environment.”

(Source: https://blogs.gartner.com/nick-heudecker/hyping-dataops/)

A small team working on a simpler or limited number of use cases can meet business requirements efficiently. As data pipelines and data infrastructures get more complex, and data teams and consumers grow in size, you need development processes and efficient collaboration between teams to govern the data and analytics lifecycle. From data ingestion and data processing to analytics and reporting, you need to reduce data defects, ensure shorter cycle times, and ensure 360-degree access to quality data for all stakeholders.

DataOps helps you achieve this through metadata management, workflow and test automation, code repositories, collaboration tools, and orchestration to help manage complex tasks and workflows. Using the DataOps methodology ensures all activities occur in the right order the right security permissions. It helps set in a continual process that allows you to cut wastages, streamline steps, automate processes, increase throughput, and improve continually.

Several DataOps Platforms are available in the market, some of the popular ones being IBM DataOps, Nexla, Switchboard, Streamsets, and Infoworks.

DataOps Methodology:
The purpose of the DataOps Methodology is to enable an organization to utilize a repeatable process to build and deploy analytics and data pipelines. Successful implementation of this methodology allows an organization to know, trust, and use data to drive value.

It ensures that the data used in problem-solving and decision making is relevant, reliable, and traceable and improves the probability of achieving desired business outcomes. And it does so by tackling the challenges associated with inefficiencies in accessing, preparing, integrating, and making data available.

In a nutshell, the DataOps Methodology consists of three main phases:

The Establish DataOps Phase provides guidance on how to set up the organization for success in managing data.

The Iterate DataOps Phase delivers the data for one defined sprint.

The Improve DataOps Phase ensures learnings from each sprint is channeled back to continually improve the DataOps process.

Benefits of using the DataOps methodology:
Adopting the DataOps methodology helps organizations to organize their data and make it more trusted and secure. Using the DataOps methodology, organizations can:

Automate metadata management and catalog data assets, making them easy to access.

Trace data lineage to establish its credibility and for compliance and audit purposes.

Automate workflows and jobs in the data lifecycle to ensure data integrity, relevancy, and security.

Streamline the workflow and processes to ensure data access and delivery needs can be met at optimal speed.

Ensure a business-ready data pipeline that is always available for all data consumers and business stakeholders.

Build a data-driven culture in the organization through automation, data quality, and governance.

As a data practitioner, using the methodology can help you reduce development time, cut wastages and duplication of effort, increase your productivity and throughput, and ensure that your actions produce the best possible quality of data.

With DataOps, data professionals, consumers, and stakeholders can collaborate more effectively towards the shared goal of creating valuable insights for business. While implementing the methodology will require systemic change, time, and resources, but in the end, it makes data and analytics more efficient and reliable.

Interestingly, it also opens up additional career opportunities for you as a data engineer. DataOps Engineers are technical professionals that focus on the development and deployment lifecycle rather than the product itself. And as you grow in experience, you can move into more specialist roles within DataOps, contributing to defining the data strategy, developing and deploying business processes, establishing performance metrics, and measuring performance.
