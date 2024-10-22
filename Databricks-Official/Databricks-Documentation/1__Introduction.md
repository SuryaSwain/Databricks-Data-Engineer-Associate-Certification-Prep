# 0. Introduction


## [What is Databricks?](https://docs.databricks.com/introduction/index.html)

- What is Databricks?
  - How does a data intelligence platform work?
  - What is Databricks used for?
  - Managed integration with open source
  - Tools and programmatic access

- How does Databricks work with Cloud providers?
  - [How does Databricks work with AWS?](https://docs.databricks.com/en/introduction/index.html#how-does-databricks-work-with-aws)
  - [How does Azure Databricks work with Azure?](https://learn.microsoft.com/en-us/azure/databricks/introduction/#how-does-azure-databricks-work-with-azure)
  - [How does Databricks work with Google Cloud?](https://docs.gcp.databricks.com/en/introduction/index.html#how-does-databricks-work-with-google-cloud)

- What are common use cases for Databricks?
  - Build an enterprise data lakehouse
  - ETL and data engineering
  - Machine learning, AI, and data science
  - Data warehousing, analytics, and BI
  - Data governance and secure data sharing
  - DevOps, CI/CD, and task orchestration
  - Real-time and streaming analytics

--------------------------------------------------------------------------

## Lakehouse Introduction

### [What is a data lakehouse?](https://docs.databricks.com/en/lakehouse/index.html)
- What is a data lakehouse?
- What is a data lakehouse used for?
- How does the Databricks lakehouse work?
  - Data ingestion
  - Data processing, curation, and integration
  - Data serving
- Capabilities of a Databricks lakehouse
- Lakehouse vs Data Lake vs Data Warehouse


### [ACID guarantees on Databricks](https://docs.databricks.com/en/lakehouse/acid.html)

- What are ACID guarantees on Databricks?
- How are transactions scoped on Databricks?
- How does Databricks implement atomicity?
- How does Databricks implement durability?
- How does Databricks implement consistency?
- How does Databricks implement isolation?
- Does Delta Lake support multi-table transactions?
- What does it mean that Delta Lake supports multi-cluster writes?


### [Medallion Architecture](https://docs.databricks.com/en/lakehouse/medallion.html)

- What is the medallion lakehouse architecture?
- Ingest raw data to the bronze layer
- Validate and deduplicate data in the silver layer
- Power analytics with the gold layer


### [Single Source of Truth](https://docs.databricks.com/en/lakehouse/ssot.html)

- What does it mean to build a single source of truth?
- How does the lakehouse control transactions and data access?
- Manage access to production data
- Leverage views in the lakehouse
- Share data with collaborators


### [Data discovery and collaboration in the lakehouse](https://docs.databricks.com/en/lakehouse/collaboration.html)

- How does Databricks implemented data discovery and collaboration in the lakehouse?
- Manage permissions at scale
- Discover data on Databricks
- Accelerate time to production with the lakehouse

--------------------------------------------------------------------------

## Apache Spark

### [Apache Spark on Databricks](https://docs.databricks.com/en/spark/index.html)

- Apache Spark on Databricks
- What is the relationship of Apache Spark to Databricks?
- How does Apache Spark work on Databricks?
- Can I use Databricks without using Apache Spark?
- Why use Apache Spark on Databricks?
- How can I learn more about using Apache Spark on Databricks?


### [Configure Spark Properties](https://docs.databricks.com/en/spark/conf.html)

- Set Spark configuration properties on Databricks
- Configure Spark properties for notebooks and jobs
- Configure Spark properties in Databricks SQL
- Configure Spark properties for Delta Live Tables pipelines
- Configure Spark properties for serverless notebooks and jobs


### [Tutorial: DataFrames](https://docs.databricks.com/en/getting-started/dataframes.html)

- What is a DataFrame?
- Requirements
- Step 1: Define variables and load CSV file
- Step 2: Create a DataFrame
- Step 3: Load data into a DataFrame from CSV file
- Step 4: View and interact with your DataFrame
- Step 5: Save the DataFrame
- Additional tasks: Run SQL queries in PySpark, Scala, and R
- DataFrame tutorial notebooks
- Additional resources

--------------------------------------------------------------------------

## [What is Delta?](https://docs.databricks.com/en/introduction/delta-comparison.html)

- What are the Delta things used for?
- Delta Lake: OS data management for the lakehouse
- Delta tables: Default data table architecture
- Delta Live Tables: Data pipelines
- Delta tables vs. Delta Live Tables
- Delta: Open source or proprietary?
- What are the other Delta things on Databricks?

--------------------------------------------------------------------------

## [Databricks concepts](https://docs.databricks.com/en/getting-started/concepts.html)

- Accounts and workspaces
- Billing: Databricks units (DBUs)
- Authentication and authorization
- Databricks interfaces
- Data management
- Computation management
- Data engineering
- AI and machine learning
- Data warehousing

--------------------------------------------------------------------------

## [Databricks architecture overview](https://docs.databricks.com/en/getting-started/overview.html)

- High-level architecture
- Serverless compute plane
- Classic compute plane
- Workspace storage
  - [Workspace storage bucket](https://docs.databricks.com/en/getting-started/overview.html#workspace-storage-bucket)
  - [Workspace storage account](https://learn.microsoft.com/en-us/azure/databricks/getting-started/overview#storage)
  - [Workspace storage buckets](https://docs.gcp.databricks.com/en/getting-started/overview.html#workspace-storage-buckets)


--------------------------------------------------------------------------

## [Databricks integrations overview](https://docs.databricks.com/en/getting-started/connect/index.html)

- Partner Connect
- Data sources
- BI tools
- Other ETL tools
- IDEs and other developer tools
- Git


--------------------------------------------------------------------------

## DatabricksIQ

### [DatabricksIQ-powered features](https://docs.databricks.com/en/databricksiq/index.html)

What is DatabricksIQ?
DatabricksIQ features: Trust and safety
How do I enable or disable Databricks Assistant?
Use Databricks Assistant to develop code
Create dashboards with Databricks Assistant
AI-generated table comments in Catalog Explorer
Use Databricks Assistant for help


### [DatabricksIQ trust and safety](https://docs.databricks.com/en/databricksiq/databricksiq-trust.html)


### [What is Databricks Assistant?](https://docs.databricks.com/en/notebooks/databricks-assistant-faq.html)

How can Databricks Assistant help?
Get coding help from Databricks Assistant
Create data visualizations using the Databricks Assistant
Services used by Databricks Assistant
Tips for improving the accuracy of results
What is the pricing for Databricks Assistant?
Give feedback
Geo availability of Assistant features
Privacy and security


### [Use Databricks Assistant](https://docs.databricks.com/en/notebooks/use-databricks-assistant.html)

For an account: Disable or enable Databricks Assistant features
For a workspace: Disable or enable Assistant features
Tour of the Assistant pane
Use Databricks Assistant in a notebook cell
Get help with code
Quick Fix
Diagnose errors in jobs (Public Preview)
Get answers from Databricks documentation
Tips for using Databricks Assistant
Additional information

--------------------------------------------------------------------------

## [Databricks release notes](https://docs.databricks.com/en/release-notes/index.html)








