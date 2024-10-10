# Day 1 Notes: Databricks Lakehouse Platform


## *Udemy Course: Databricks Certified Data Engineer Associate - Preparation* -- **Section 1: Introduction**


### 1. Course Overview

- Instructor
  * Name: **Derar Alhussein**, 
  * Persona: *Senior Big Data Engineer*, 
  * Experience: 10+ years of experience working on software and data science projects including large data projects on Databricks
  * Based: France
  * Holds: 5 certifications from Databricks
  * Linkedin: https://www.linkedin.com/in/DerarAlhussein

- Course outline
  * Databricks Lakehouse Platform
  * ELT with Spark SQL and Python
  * Incremental Data Processing
  * Production Pipelines
  * Data Governance

- Prerequisities
  * SQL language
  * basic Python

### 2. What is Databricks

- What is Databricks 
  
  * Multi-cloud Lakehouse Platform based on Apache Spark

- What is Lakehouse

  <div style="text-align: center;">
    <img src="../images/what is lakehouse.jpg" style="width:640px" >
  </div>

  A data lakehouse is a unified analytics platform that 
  combines the best elements of data lakes and data warehouses,
  deliver the openness, flexibility and machine learning support of data lakes 
  with the reliability, strong governance and performance of data warehouses.
  So in the lake house you work on that engineering, analytics and AI all in one platform.

- Architecture of Databricks Lakehouse
  
  It is divided into three important layers: the cloud service, the runtime and the workspace.

  <div style="text-align: center;">
    <img src="../images/Architecture of Databricks Lakehouse.jpg" style="width:400px" >
  </div>

  * First, the **cloud service**: Databricks is multi-cloud, available on Microsoft Azure, Amazon Web Services and Google Cloud.

  * Then there is the Databricks **runtime**, which is a set of core components like Apache Spark, Delta Lake and other system libraries. We will see Delta Lake in detail in the next module. 
    
    Databricks uses the infrastructure of your cloud provider to provision virtual machines or nodes of a cluster. And this cluster comes pre-installed with Databricks runtime. 

  * On top of all this, there is the Databricks **workspace** allowing you to interactively implement and run your data engineering, analytics and AI workloads.

- How Databricks resources are deployed in your cloud provider

  There are two high level components: the control plan and the data plan.

  <div style="text-align: center;">
    <img src="../images/the control plan and the data plan.jpg" style="width:400px" >
  </div>

  * The control plan resides in Databricks account while the data plan is in your own cloud subscription.

  * Whenever you create a databricks workspace, it is deployed in the **control plan** along with Databricks services like Databricks UI, Cluster Manager, workflow service and notebooks. We will have the chance during this course to see all these services.

  * On the other hand, a storage account is deployed in the **data plan** in your own subscription. It is used for Databricks File System or DBFS. We will talk about DBFS in just a minute. In addition, when you want to set up a spark cluster, the cluster virtual machine will be also deployed in the data plan. So to summarize, the compute and the storage will be always in your own cloud account.

  Databricks will provide you with the tools you need to use and control your infrastructure.

- Spark on Databricks

  Databricks has been founded by the same engineers that developed Spark because it is based on Apache Spark.

  * The data is distributed and processed in-memory of multiple nodes in a cluster.

  * Databricks supports all the languages supported by Spark which are Scala, Python, SQL, R and Java as well.

  * It has also support for batch processing and stream processing in Spark.

  * In addition, on Databricks, you can process data no matter if it is structured, semi-structured, or even unstructured like images and videos.

- Databricks File System (DBFS)

  Since Apache Spark processes data in a distributed manner, 
  Databricks offers a native support of a distributed file system called *Databricks File System* or **DBFS**. 
  So whenever you create a cluster in Databricks, it comes pre-installed with DBFS.

  We usually use file systems to persist data and files. 
  However, DBFS is just an *abstraction layer*, 
  while it uses the underlying cloud storage to persist the data.

  <div style="text-align: center;">
    <img src="../images/DBFS uses the underlying cloud storage.jpg" style="width:400px" >
  </div>

  To illustrate this, if you create a file in your cluster and store it in DBFS, 
  this file is actually persisted in the underlying cloud storage, 
  like your Azure storage or your S3 buckets.
  So even after the cluster is terminated, all the data is safe in your cloud storage.


### 3. Get started with Community Edition


### 4. Free trial on Azure


### 5. Exploring Workspace


### 6. Course Materials


### 7. Creating Cluster


### 8. Notebooks Fundamentals


### 9. Databricks Repos (Git folders)


## *Udemy Course: Databricks Certified Data Engineer Associate - Preparation* -- **Section 2: Databricks Lakehouse Platform**


### 10. Delta Lake


### 11. Understanding Delta Tables (Hands On)


### 12. Advanced Delta Lake Features


### 13. Apply Advanced Delta Features (Hands On)


### 14. Relational entities


### 15. Databases and Tables on Databricks (Hands On)


### 16. Set Up Delta Tables


### 17. Views


### 18. Working with Views (Hands On)


