# Day 1 Notes: Databricks Lakehouse Platform


## *Udemy Course: Databricks Certified Data Engineer Associate - Preparation* -- **Section 1: Introduction**


### Lesson 1. Course Overview

- Instructor
  * Name: **Derar Alhussein**, 
  * Persona: *Senior Big Data Engineer*, 
  * Experience: 10+ years of experience working on software and data science projects including large data projects on Databricks
  * Based: France
  * Holds: 5+ certifications from Databricks
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

### Lesson 2. What is Databricks

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

- [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34664668#overview)

### Lesson 3. Get started with Community Edition

  - Community edition is a lightweight Databricks environment for personal use and training.
  - [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34722722#overview)


### Lesson 4. Free trial on Azure

  - If you have a cloud account, you can use it to register for a 14-day Databricks full trial.

  - A full trial in your cloud is recommended 
  since it includes production grade functionalities 
  that are not available in the limited community edition.

  - Microsoft offers a free tier for 12 months, 
  allowing you to explore and try out Azure services 
  free of charge and up to specified limits for each service.

  - [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34725890#overview)


### Lesson 5. Exploring Workspace

  - [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34727098#overview)


### Lesson 6. Course Materials

  - Github Repository: https://github.com/derar-alhussein/Databricks-Certified-Data-Engineer-Associate

  - [Course Materials DBC](../resources/Course-Materials.dbc)

  - [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34742090#overview)


### Lesson 7. Creating Cluster

  - Navigate to "Compute" in the left side bar. ...

  - A **cluster** is a set of nodes or computers working together like a single entity. 
  It consists of a master node called the driver and some other worker nodes.
  The driver node is responsible for coordinating the workers and their parallel execution of tasks.

  - Your cluster could be multi node, that is having multiple workers, or simply a single node. 
  A single node cluster, has no workers and run Spark jobs on the driver node.

  - For the *access mode*, you can allow your cluster to be shared by multiple users. 
  However, only SQL and Python workloads will be supported.

  - **Databricks Runtime** is the virtual machine's image that comes with preinstalled libraries, 
  which has a specific version of Spark, Scala and other libraries.

  - In addition, you can choose to activate **Photon**, 
  which is a vectorized query engine developed in C++ to enhance Spark performance.

  - You can select the configuration of your worker nodes. 
  These are different virtual machine sizes provided by your cloud provider,

  - **DBU** stands for Databricks Unit and it is a unit of a processing capability per hour

  - Changing the cluster configuration may require a restart of the cluster.

  - In the cluster page, you can notice two things.
    
    * The Event log, that shows all the events that have happened with the cluster. 
    For example, when the cluster was created or terminated, if it is edited or if it is running fine. 
    This helps to track the activity on a cluster.
    * In the driver log, you will get the log generated within the cluster notebooks and libraries.

  - [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34728190)


### Lesson 8. Notebooks Fundamentals

  - Notebooks are coding environments allowing you 
  to interactively developing and executing code on databricks.
  You can also collaborate between different team members by sharing the notebook.

  - Before running any computation, we need 
  to attach your notebook to a cluster on which your code will be running.

  - If you have previously used Jupyter Notebook, 
  you will notice that the basic functionality is the same, 
  but with additional features and capabilities that you might enjoy.

  - Databricks notebooks support Python, SQL, Scala and R. 
    * A language is selected when a notebook is created, but this can be changed at any time.
    * In a notebook, you can change the language of a specific cell.

  - *Magic commands* are built in commands that provide the same output regardless of the notebook language. This is called **Language Magic Command** that allows the execution of code in a language other than the
      - `%sql` to run SQL 
      - `%md` for markdown
      - `%run` to run another notebook from the current notebook. For example, 
        ```
        %run ./Includes/Setup
        ```
      - `%fs` to deal with file system operations like LS for listing files in a given directory. For example,
        ```
        %fs ls '/databricks-datasets'
        ```
  
  - Another way to deal with filesystem operations is to use databricks utilities, also known as `dbutils`. `dbutils` provides a number of utility commands for configuring and interacting with the environment.
    * `dbutils.help()` function to get some help for each utility.
    * `dbutils.fs.help()`
    * Databricks notebooks also support auto completion using the 'Tab' key.
    * `dbutils.fs.ls('/databricks-datasets')`
    * In fact, dbutils is more useful than the %fs magic command since you can use dbutils as part of python code.
      ```python
      files = dbutils.fs.ls('/databricks-datasets')
      display(files)
      ```

  - The **DBC** or the *Databricks Cloud file* is a zip file that contains a collection of directories and notebooks. 
  This file can be uploaded into any databricks workspace to move or share notebooks.

  - In Databricks notebooks, you can access the revision history of all the changes being made on a notebook.

  - [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34742270#overview)


### Lesson 9. Databricks Repos (Git folders)

  - Databricks Repos provides source control for your data projects by integrating with GitHub providers.

  - In order to work with Databricks Repos, we must first configure git integration in your workspace.

  - [Watch Video](https://external-teksystems.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34844752#overview)


## *Udemy Course: Databricks Certified Data Engineer Associate - Preparation* -- **Section 2: Databricks Lakehouse Platform**


### Lesson 10. Delta Lake


### Lesson 11. Understanding Delta Tables (Hands On)


### Lesson 12. Advanced Delta Lake Features


### Lesson 13. Apply Advanced Delta Features (Hands On)


### Lesson 14. Relational entities


### Lesson 15. Databases and Tables on Databricks (Hands On)


### Lesson 16. Set Up Delta Tables


### Lesson 17. Views


### Lesson 18. Working with Views (Hands On)


