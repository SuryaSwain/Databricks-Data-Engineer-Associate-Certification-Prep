# Complemental Notes for Lecture 2. What is Databricks

## Data Lake vs. Data Warehouse vs. Data Lakehouse

| **Aspect**      | **Data Lake**                                                                                      | **Data Warehouse**                                                                         | **Data Lakehouse**                                                                         |
|-----------------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| **Definition**   | A storage repository for vast amounts of raw, unstructured, semi-structured, and structured data. | A structured and organized system designed for managing structured data for BI and reporting. |A hybrid architecture combining the flexibility of data lakes with the management and analytics capabilities of data warehouses.|
| **Data Type**    | Stores all types of data: structured (tables), semi-structured (JSON, XML), and unstructured (videos, images, logs). | Optimized for structured and transactional data from databases.                            | Supports structured, semi-structured, and unstructured data.                              |
| **Schema**      | **Schema-on-read**; applied only when data is read.                                               | **Schema-on-write**; data is cleaned and transformed before being stored in a predefined schema. | Offers both **schema-on-read** and **schema-on-write** options.                           |
| **Purpose**     | Primarily used for big data analytics, machine learning, and data exploration.                     | Best for running analytical queries, business reporting, and dashboarding.                | Allows for data exploration, machine learning, and advanced analytics while supporting BI and real-time analytics. |
| **Cost**        | Generally cost-effective due to scalability and the ability to store vast amounts of raw data.    | More expensive due to computation and management overhead.                                 | Can be more cost-efficient than maintaining separate systems (data lake + data warehouse) but involves more advanced management. |
| **Examples**    | Amazon S3, Azure Data Lake, Google Cloud Storage.                                                | Amazon Redshift, Google BigQuery, Snowflake.                                              | Databricks Lakehouse, Delta Lake, Snowflake (with some lakehouse features).               |

### When to Use:
- **Data Lake**: Ideal for low-cost storage of vast amounts of raw data for data science and exploratory analysis.
- **Data Warehouse**: Suited for optimized, high-performance analytics and business reporting.
- **Lakehouse**: Best for unifying data processing and analytics for both structured and unstructured data.


## Databricks Cloud Services across Cloud Providers (AWS, Azure, and Google Cloud)

When comparing **Databricks Cloud Services** across major cloud providers (AWS, Azure, and Google Cloud), the core Databricks platform remains consistent in providing powerful data processing, machine learning, and collaborative tools. However, each cloud provider offers unique integrations, features, and benefits that differentiate the experience. Here's a comparison of Databricks cloud services across the three providers:


### **Comparison of Key Features**

| **Feature**                  | **Databricks on AWS**                      | **Databricks on Azure**                     | **Databricks on Google Cloud**               |
|------------------------------|--------------------------------------------|--------------------------------------------|---------------------------------------------|
| **Storage**                   | Amazon S3 + Delta Lake                    | Azure Data Lake Storage (ADLS) + Delta Lake | Google Cloud Storage (GCS) + Delta Lake     |
| **Compute**                   | EC2 Instances                             | Azure Virtual Machines (VMs)               | Google Compute Engine (GCE) / GKE           |
| **ETL Integration**           | AWS Glue, Lambda                          | Azure Data Factory (ADF)                   | Google Cloud Dataflow, Pub/Sub              |
| **Data Warehousing**          | AWS Redshift                              | Azure Synapse Analytics                    | BigQuery                                    |
| **Machine Learning**          | Amazon SageMaker, AWS Lambda              | Azure Machine Learning                     | Vertex AI, Google Cloud ML Engine           |
| **Security**                  | AWS IAM, KMS, VPC                         | Azure Active Directory, Key Vault          | Google Cloud IAM, KMS, VPC                  |
| **Governance**                | Unity Catalog, RBAC, Encryption (AWS KMS) | Unity Catalog, RBAC, Encryption (Azure KMS)| Unity Catalog, RBAC, Encryption (Google KMS)|
| **Real-time Data Streaming**  | Amazon Kinesis                            | Azure Event Hubs                           | Google Pub/Sub                              |
| **Collaborative Notebooks**   | Integrated in all platforms               | Integrated in all platforms                | Integrated in all platforms                 |
| **Dashboards**                | Databricks SQL + AWS integrations         | Databricks SQL + Power BI integration      | Databricks SQL + Google Data Studio         |


### **Common Features Across Databricks on AWS, Azure, and Google Cloud**

Despite being deployed on different cloud platforms, Databricks maintains core functionalities that are consistent across **AWS**, **Azure**, and **Google Cloud**. Here’s a summary of the **common features** across all three cloud providers:

1. **Unified Data Analytics Platform**:
   - **Apache Spark Engine**: All platforms use Databricks' optimized version of **Apache Spark** for scalable, distributed data processing.
   - **Delta Lake**: Provides ACID transactions, time travel, schema enforcement, and data versioning on all platforms, enhancing data reliability for both streaming and batch data.

2. **Collaborative Workspaces**:
   - **Databricks Notebooks**: Unified notebooks supporting multiple languages (Python, SQL, Scala, R) that allow users to collaborate in real-time.
   - **Dashboards**: Built-in support for creating visualizations and dashboards directly from the notebooks.

3. **ETL & Data Engineering**:
   - **Data Pipelines**: All cloud versions support scalable **ETL** workflows to extract, transform, and load data.
   - **Auto-scaling**: Databricks clusters automatically scale up and down to handle varying workloads across all cloud providers.
   - **Job Scheduling**: Supports scheduling of **ETL jobs** and **workflows**.

4. **Machine Learning and AI**:
   - **MLflow**: Integrated machine learning lifecycle management tool for tracking experiments, packaging models, and automating model deployment.
   - **Pre-built ML Libraries**: Includes libraries for **deep learning** and **machine learning** (TensorFlow, PyTorch, Scikit-learn, etc.).
   - **Model Serving**: Managed services for deploying machine learning models and APIs.

5. **Data Streaming**:
   - **Structured Streaming**: Real-time data streaming is available across all platforms, allowing for real-time ingestion and processing of streaming data sources (e.g., Kafka, Event Hubs, Pub/Sub).
   - **Support for both Batch and Streaming**: Unified handling of batch and real-time (streaming) data.

6. **SQL Analytics**:
   - **Databricks SQL**: SQL-based interface across platforms that allows for querying large datasets, creating reports, and building dashboards.
   - **BI Tool Integration**: All cloud versions of Databricks can integrate with third-party business intelligence tools like Tableau, Power BI, and Looker.

7. **Security and Compliance**:
   - **Data Encryption**: Encryption at rest and in transit using native cloud provider encryption services (AWS KMS, Azure Key Vault, Google Cloud KMS).
   - **Identity Management**: Integrates with each cloud provider’s Identity and Access Management (IAM) systems for role-based access control (AWS IAM, Azure Active Directory, Google Cloud IAM).
   - **Compliance**: All platforms offer compliance with major industry standards, including **GDPR**, **HIPAA**, **SOC 2**, and **ISO**.

8. **Governance and Cataloging**:
   - **Unity Catalog**: A unified data governance tool to manage data access controls, audit logs, and metadata across all platforms.

9. **CI/CD Integration**:
   - Supports **CI/CD pipelines** via integration with tools like **Jenkins**, **Azure DevOps**, and **GitHub Actions** across all platforms.
   - Git-based **version control** is available for notebooks, jobs, and other assets.

10. **Cost Management**:
    - **Cost Optimizations**: All cloud providers offer features like cluster auto-scaling, spot instances/preemptible VMs, and usage-based pricing models to optimize costs for both compute and storage.

These common features allow Databricks to provide a consistent experience for **data engineering**, **machine learning**, and **analytics** regardless of the cloud platform. Each cloud provider further enhances Databricks with unique integrations, but the core platform functionalities remain the same across all environments.


### **Choosing the Right Cloud Provider for Databricks**

| **Provider**         | **Strengths**                                                         | **Considerations**                                                     | **Typical Use Cases**                                           |
|----------------------|-----------------------------------------------------------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **AWS**              | - Extensive service range<br>- Robust scalability<br>- Strong integration with AWS tools (e.g., S3, Redshift) | - Complex pricing<br>- Steeper learning curve for newcomers         | - Large-scale data processing<br>- Real-time analytics<br>- Machine learning workflows |
| **Azure**            | - Excellent integration with Microsoft ecosystem (e.g., Azure Data Lake, Power BI)<br>- Strong security and compliance | - Geographic availability may be limited<br>- Potential over-reliance on Azure services | - Enterprise analytics<br>- BI integration<br>- Advanced analytics in regulated industries |
| **Google Cloud**     | - Strong analytics focus with BigQuery<br>- Competitive pricing<br>- Innovative ML tools | - Smaller ecosystem than AWS/Azure<br>- May require significant changes for migration | - Data analytics and reporting<br>- Data science projects<br>- Cost-effective processing solutions |

#### **Key Factors to Consider**:

| **Factor**                     | **Description**                                                                 |
|--------------------------------|---------------------------------------------------------------------------------|
| **Existing Infrastructure**     | Stay within your current ecosystem for easier integration.                      |
| **Team Expertise**             | Match the provider to your team's skills.                                       |
| **Use Cases**                  | Align the provider’s strengths with your specific needs.                       |
| **Compliance & Security**      | Ensure the provider meets industry standards.                                   |
| **Cost**                       | Analyze long-term pricing models.                                              |
| **Performance & Scalability**  | Assess capabilities based on workload requirements.                             |
| **Support**                    | Consider available support and resources.                                      |

Choosing the right cloud provider for Databricks depends on your organization’s goals, existing systems, and specific project requirements.


### Conclusion:
Databricks offers consistent performance across all cloud providers, but each one provides unique integrations that may appeal to different business needs. Whether you prioritize seamless AI/ML workflows, large-scale data warehousing, or real-time analytics will help determine the best platform for your Databricks deployment.


## Databricks Workspace vs Runtime vs Clusters

### Databricks Workspace

1. **Definition**: 
   - A collaborative environment where data teams can develop, manage, and share their data projects.

2. **Key Features**:
   - **Notebooks**: Interactive documents for writing code, visualizing data, and documenting findings.
   - **Collaboration**: Multiple users can work on notebooks simultaneously for real-time collaboration.
   - **Data Management**: Integrates with various data sources for easy data access and manipulation.
   - **Job Scheduling**: Automates tasks by scheduling jobs to run notebooks or scripts.
   - **Access Control**: Provides user management and permission settings for security and collaboration.
   - **Organization**: Offers structured ways to organize projects, files, and data assets.

3. **Purpose**:
   - Focused on **collaboration, development, and project management**. It acts as the user interface for data teams to work on their projects together.

### Databricks Runtime

1. **Definition**: 
   - A pre-configured environment that includes Apache Spark and optimized libraries for executing data processing tasks.

2. **Key Features**:
   - **Core Engine**: Provides the underlying processing engine (Apache Spark) and libraries for computations.
   - **Performance Optimizations**: Enhancements that improve execution speed and resource utilization.
   - **Multiple Versions**: Users can select different runtime versions for compatibility with specific workloads.
   - **Delta Lake Support**: Includes support for ACID transactions and data versioning.

3. **Purpose**:
   - Focused on **data processing and execution**. It provides the necessary software environment for running data analytics, machine learning models, and other computations.

### Databricks Clusters

1. **Definition**: 
   - A set of virtual machines that run workloads and execute tasks in Databricks.

2. **Key Features**:
   - **Types**: Includes Interactive (for development) and Job (for scheduled tasks).
   - **Auto-Scaling**: Adjusts resources based on demand.
   - **Customizable Configurations**: Users can configure instance types and the number of nodes.
   - **Monitoring Tools**: Provides tools for performance tracking and resource management.

3. **Purpose**:
   - Focused on providing **compute resources**. Clusters execute tasks and manage workload execution efficiently.

### Summary of Differences

| Aspect                 | Databricks Workspace                              | Databricks Runtime                         | Databricks Clusters                       |
|-----------------------|--------------------------------------------------|-------------------------------------------|-------------------------------------------|
| **Definition**        | Collaborative environment for development        | Software environment for execution        | Set of virtual machines for workload execution |
| **Key Features**      | Notebooks, collaboration, data management, job scheduling, access control | Core components (Apache Spark, Delta Lake), performance optimizations, versioning | Types (interactive/job), auto-scaling, customizable configurations |
| **Purpose**           | Development, collaboration, and project management | Data processing and execution             | Provide compute resources for executing tasks |
| **User Interaction**  | Direct user interface for data scientists/engineers | Runs in the background, not directly interacted with by users | Managed by users when creating, starting, or stopping clusters |
| **Focus**             | User experience and teamwork                      | Computational efficiency and performance  | Resource management and scalability       |

### Conclusion

In summary, **Databricks Workspace** is where data professionals collaborate and manage their projects, **Databricks Runtime** provides the environment for executing data processing tasks, and **Databricks Clusters** are the compute resources that run those tasks. Together, they enable a seamless workflow for data analysis, machine learning, and big data processing.


## Apache Spark vs. Spark on Databricks

### Apache Spark
**Apache Spark** is an open-source, distributed computing framework designed for rapid and large-scale data processing. It offers a unified engine for diverse workloads, including batch processing, stream processing, and machine learning.

#### Key Features:
1. **Speed**: Leverages in-memory processing to significantly enhance performance compared to traditional disk-based systems.
2. **Unified Engine**: Capable of handling batch jobs, real-time data streams, interactive queries, and complex machine learning algorithms.
3. **Ease of Use**: Provides high-level APIs in multiple programming languages, including Scala, Python, Java, and R, facilitating accessibility for various users.
4. **Scalability**: Scales seamlessly from a single server to thousands of nodes, efficiently processing petabytes of data.
5. **Flexible Data Processing**: Supports various data formats—structured, semi-structured, and unstructured—enabling versatile data handling.
6. **Rich Ecosystem**: Includes a comprehensive suite of libraries:
   - **Spark SQL** for SQL queries and structured data processing.
   - **MLlib** for machine learning tasks.
   - **GraphX** for graph processing.
   - **Spark Streaming** for real-time analytics.

#### Architecture:
- **Driver Program**: The main control program that coordinates execution across the cluster.
- **Cluster Manager**: Manages resources and scheduling (e.g., YARN, Mesos, or Spark’s built-in cluster manager).
- **Executors**: Distributed processes on worker nodes responsible for executing tasks and holding data.

#### Use Cases:
- Extensive data analytics, machine learning model training, ETL (Extract, Transform, Load) processes, and real-time streaming applications.


### Spark on Databricks
**Spark on Databricks** is a cloud-based analytics platform built on Apache Spark, designed to enhance its capabilities with additional features tailored for collaborative data science and engineering.

#### Enhanced Features:
1. **Managed Service**: Automatically handles the provisioning, configuration, and management of Spark clusters, reducing operational overhead for users.
2. **Optimized Runtime**: Delivers performance optimizations specifically for cloud environments, improving resource management and execution speed.
3. **Delta Lake Integration**: Facilitates ACID transactions, schema enforcement, and data versioning, enabling reliable data lakes capable of managing both batch and streaming data effectively.
4. **Interactive Notebooks**: Provides a collaborative environment for real-time coding, documentation, and visualization, supporting multiple programming languages (Scala, Python, SQL, R).
5. **Auto-Scaling**: Dynamically adjusts the size of the cluster based on workload requirements, ensuring optimal resource utilization and cost-efficiency.
6. **Job Scheduling and Monitoring**: Offers integrated tools for scheduling jobs, tracking performance, and reviewing execution history directly within the platform.
7. **Built-In Visualization Tools**: Includes visualization capabilities to create charts and graphs directly in notebooks, streamlining the process of gaining insights from data.
8. **BI Tool Integration**: Seamlessly connects with popular Business Intelligence tools like Tableau and Power BI, enhancing data visualization and reporting capabilities.
9. **Enhanced Security**: Implements robust security features, including role-based access control (RBAC) and compliance protocols, ensuring data protection in enterprise environments.
10. **Machine Learning Support**: Integrates with various machine learning libraries and frameworks (e.g., MLlib, TensorFlow, PyTorch), simplifying the workflow for building and deploying models.

### Conclusion
While **Apache Spark** serves as a powerful engine for big data processing, **Spark on Databricks** amplifies this functionality with its managed services, performance optimizations, collaborative tools, and seamless integrations. This makes it a superior platform for data analytics and machine learning, especially in cloud environments, catering to the needs of modern data-driven organizations.


## Databricks File System (DBFS)

**Databricks File System (DBFS)** is a distributed file system integrated with Databricks, designed to facilitate data storage and access in a cloud environment. When you create a cluster in Databricks, DBFS is pre-installed, providing a convenient layer for managing files and data within your Spark applications.

### Key Points:
- **Abstraction Layer**: DBFS serves as an abstraction over underlying cloud storage solutions, such as Amazon S3, Azure Blob Storage, or Google Cloud Storage, allowing users to interact with files seamlessly without worrying about the specific storage technology.
- **Data Persistence**: Any files created or stored in DBFS are actually saved in the underlying cloud storage. This ensures that data persists even if the Databricks cluster is terminated, providing reliable and durable storage for your datasets.
- **Ease of Use**: Users can easily read and write data using familiar file paths and commands within Databricks notebooks, making it simple to manage datasets across different applications and workflows.
- **Data Access**: DBFS enables distributed access to files across the cluster, supporting efficient data processing in parallel across multiple nodes, which is essential for big data workloads.

### Conclusion
DBFS enhances the functionality of Apache Spark on Databricks by providing a robust, cloud-based file management system that simplifies data persistence and access, ensuring that your data remains safe and accessible even after clusters are shut down.