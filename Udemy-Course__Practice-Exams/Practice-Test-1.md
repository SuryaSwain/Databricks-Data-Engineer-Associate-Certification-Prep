# Practice Test 1

There are 45 multiple-choice questions on each practice exam. The questions will be distributed by high-level topic in the following way:

- Databricks Lakehouse Platform – 24% (11/45)
- ELT with Spark SQL and Python – 29% (13/45)
- Incremental Data Processing – 24% (11/45)
- Production Pipelines – 16% (7/45)
- Data Governance – 7% (3/45)

---

### Question 1

Which of the following commands can a data engineer use to compact small data files of a Delta table into larger ones?

  * [ ] PARTITION BY
  * [ ] ZORDER BY
  * [ ] COMPACT
  * [ ] VACUUM
  * [x] OPTIMIZE

- **Overall explanation**:  
  Delta Lake can improve the speed of read queries from a table. One way to improve this speed is by compacting small files into larger ones. You trigger compaction by running the OPTIMIZE command.

- **Reference**:  
  [Delta OPTIMIZE Command](https://docs.databricks.com/sql/language-manual/delta-optimize.html)

- **Study materials** from our exam preparation course on Udemy:  
  * [Lecture]()
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 2

A data engineer is trying to use Delta time travel to rollback a table to a previous version, but the data engineer received an error that the data files are no longer present.

Which of the following commands was run on the table that caused deleting the data files?

  * [x] VACUUM
  * [ ] OPTIMIZE
  * [ ] ZORDER BY
  * [ ] DEEP CLONE
  * [ ] DELETE

- **Overall explanation**:  
  Running the **VACUUM** command on a Delta table deletes unused data files older than a specified data retention period. As a result, the ability to time travel back to any version older than that retention threshold is lost.

- **Reference**:  
  [Delta Lake VACUUM command documentation](https://docs.databricks.com/sql/language-manual/delta-vacuum.html)

- **Study materials** from our exam preparation course on Udemy:
  * [Lecture]()
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 3

In Delta Lake tables, which of the following is the primary format for the data files?

  * [ ] Delta
  * [x] Parquet
  * [ ] JSON
  * [ ] Hive-specific format
  * [ ] Both, Parquet and JSON

- **Overall explanation**:  
  Delta Lake builds upon standard data formats. Data in a Delta Lake table is stored in one or more **Parquet** files on the storage, along with transaction logs stored in **JSON** format.

- **Reference**:  
  [Delta Lake documentation](https://docs.databricks.com/delta/index.html)

- **Study materials** from our exam preparation course on Udemy:
  * [Lecture]()
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 4

Which of the following locations hosts the Databricks web application?

  * [ ] Data plane
  * [x] Control plane
  * [ ] Databricks Filesystem
  * [ ] Databricks-managed cluster
  * [ ] Customer Cloud Account

- **Overall explanation**:  
  According to the Databricks Lakehouse architecture, Databricks services such as the web application (UI), cluster manager, workflow service, and notebooks are deployed in the **control plane**.

- **Reference**:  
  [Databricks Overview](https://docs.databricks.com/getting-started/overview.html)

- **Study materials** from our exam preparation course on Udemy:
  * [Lecture]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 5

In Databricks Repos (Git folders), which of the following operations can a data engineer use to update the local version of a repo from its remote Git repository?

  * [ ] Clone
  * [ ] Commit
  * [ ] Merge
  * [ ] Push
  * [x] Pull

- **Overall explanation**:  
  The **Pull** operation in Git is used to fetch and download content from a remote repository and update the local repository to match that content.

- **References**:  
  [Databricks Repos documentation](https://docs.databricks.com/repos/index.html)  
  [Git pull documentation](https://github.com/git-guides/git-pull)

- **Study materials** from our exam preparation course on Udemy:
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 6

According to the Databricks Lakehouse architecture, which of the following is located in the customer's cloud account?

  * [ ] Databricks web application
  * [ ] Notebooks
  * [ ] Repos
  * [x] Cluster virtual machines
  * [ ] Workflows

- **Overall explanation**:  
  When a customer sets up a Spark cluster, the **cluster virtual machines** are deployed in the data plane, which resides in the customer's cloud account.

- **Reference**:  
  [Databricks Overview](https://docs.databricks.com/getting-started/overview.html)

- **Study materials** from our exam preparation course on Udemy:
  * [Lecture]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 7

Which of the following best describes Databricks Lakehouse?

  * [x] Single, flexible, high-performance system that supports data, analytics, and machine learning workloads.
  * [ ] Reliable data management system with transactional guarantees for organization’s structured data.
  * [ ] Platform that helps reduce the costs of storing organization’s open-format data files in the cloud.
  * [ ] Platform for developing increasingly complex machine learning workloads using a simple, SQL-based solution.
  * [ ] Platform that scales data lake workloads for organizations without investing in on-premises hardware.

- **Overall explanation**:  
  **Databricks Lakehouse** is a unified analytics platform that combines the best elements of data lakes and data warehouses. It supports data engineering, analytics, and AI workloads on one platform.

- **Reference**:  
  [Databricks Lakehouse overview](https://www.databricks.com/glossary/data-lakehouse)

- **Study materials** from our exam preparation course on Udemy:
  * [Lecture]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 8

If the default notebook language is SQL, which of the following options can a data engineer use to run Python code in this SQL Notebook?

  * [ ] They need first to import the Python module in a cell.
  * [ ] This is not possible! They need to change the default language of the notebook to Python.
  * [ ] Databricks detects cell language automatically, so they can write Python syntax in any cell.
  * [x] They can add `%python` at the start of a cell.

- **Overall explanation**:  
  By default, cells use the notebook's default language, but you can override this by using a language magic command (e.g., `%python`, `%sql`, `%scala`, `%r`) at the start of a cell to specify the desired language.

- **Reference**:  
  [Databricks Notebooks documentation](https://docs.databricks.com/notebooks/notebooks-code.html)

- **Study materials** from our exam preparation course on Udemy:
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 9

Which of the following tasks is **not** supported by Databricks Repos (Git folders) and must be performed in your Git provider?

  * [ ] Clone, push to, or pull from a remote Git repository.
  * [ ] Create and manage branches for development work.
  * [ ] Create notebooks and edit notebooks and other files.
  * [ ] Visually compare differences upon commit.
  * [x] Delete branches

- **Overall explanation**:  
  **Deleting branches** and other tasks like creating pull requests must be performed in your Git provider. Some tasks like merging and rebasing branches have recently been supported in Databricks Repos.

- **Reference**:  
  [Databricks Repos documentation](https://docs.databricks.com/repos/index.html)

- **Study materials** from our exam preparation course on Udemy:
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 10

Which of the following statements is **NOT** true about Delta Lake?

  * [x] Delta Lake builds upon standard data formats: Parquet + XML
  * [ ] Delta Lake provides ACID transaction guarantees
  * [ ] Delta Lake provides scalable data and metadata handling
  * [ ] Delta Lake provides audit history and time travel
  * [ ] Delta Lake supports unified streaming and batch data processing

- **Overall explanation**:  
  It is not true that Delta Lake builds upon the XML format. It builds upon **Parquet** and **JSON** formats.

- **Reference**:  
  [Delta Lake Overview](https://docs.databricks.com/delta/index.html)

- **Study materials** from our exam preparation course on Udemy:  
  * [Lecture]()
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 11

How long is the default retention period of the VACUUM command?

  * [ ] 0 days
  * [x] 7 days
  * [ ] 30 days
  * [ ] 90 days
  * [ ] 365 days

- **Overall explanation**:  
  By default, the retention threshold of the **VACUUM** command is **7 days**. This ensures that files less than 7 days old are not deleted to prevent issues with long-running operations that may still reference those files.

- **Reference**:  
  [Delta VACUUM Command](https://docs.databricks.com/sql/language-manual/delta-vacuum.html)

- **Study materials** from our exam preparation course on Udemy:  
  * [Lecture]()
  * [Hands-on]()

- **Domain**: Databricks Lakehouse Platform

---

### Question 12

The data engineering team has a Delta table called employees that contains employees' personal information, including their gross salaries.  
Which of the following code blocks will keep in the table only the employees having a salary greater than 3000?

  * [ ] `DELETE FROM employees WHERE salary > 3000;`
  * [ ] `SELECT CASE WHEN salary <= 3000 THEN DELETE ELSE UPDATE END FROM employees;`
  * [ ] `UPDATE employees WHERE salary > 3000 WHEN MATCHED SELECT;`
  * [ ] `UPDATE employees WHERE salary <= 3000 WHEN MATCHED DELETE;`
  * [x] `DELETE FROM employees WHERE salary <= 3000;`

- **Overall explanation**:  
  To keep only the employees with a salary greater than 3000, you must delete the employees having a salary less than or equal to 3000. Use the **DELETE** statement as follows:
  ```sql
  DELETE FROM table_name WHERE condition;
  ```

- **Reference**:  
  [Delta DELETE Command](https://docs.databricks.com/sql/language-manual/delta-delete-from.html)

- **Domain**: ELT with Spark SQL and Python

---

### Question 13

A data engineer wants to create a relational object by pulling data from two tables. The relational object must be used by other data engineers in other sessions on the same cluster only. To save on storage costs, the data engineer wants to avoid copying and storing physical data.  
Which of the following relational objects should the data engineer create?

  * [ ] Temporary view
  * [ ] External table
  * [ ] Managed table
  * [x] Global Temporary view
  * [ ] View

- **Overall explanation**:  
  To avoid copying and storing physical data, the data engineer must create a **view** object. A view in Databricks is a virtual table with no physical data, just a saved SQL query against actual tables.  
  The view type should be **Global Temporary view**, which can be accessed in other sessions on the same cluster. Global Temporary views are stored in the `global_temp` database.

- **Reference**:  
  [CREATE VIEW Syntax](https://docs.databricks.com/sql/language-manual/sql-ref-syntax-ddl-create-view.html)

- **Study materials** from our exam preparation course on Udemy:  
  * [Lecture]()
  * [Hands-on]()

- **Domain**: ELT with Spark SQL and Python

---

### Question 14

A data engineer has developed a code block to completely reprocess data based on the following if-condition in Python:

```python
if process_mode = "init" and not is_table_exist:
   print("Start processing ...")
```

This if-condition is returning an invalid syntax error.  
Which of the following changes should be made to the code block to fix this error?

  * [ ] `if process_mode = "init" & not is_table_exist:`
  * [ ] `if process_mode = "init" and not is_table_exist = True:`
  * [ ] `if process_mode = "init" and is_table_exist = False:`
  * [ ] `if (process_mode = "init") and (not is_table_exist):`
  * [x] `if process_mode == "init" and not is_table_exist:`

- **Overall explanation**:  
  In Python, the equality operator is `==` and not `=`. The correct syntax for the condition should be:
  ```python
  if process_mode == "init" and not is_table_exist:
      print("Start processing ...")
  ```

- **Reference**:  
  [Python Conditions](https://www.w3schools.com/python/python_conditions.asp)

- **Domain**: ELT with Spark SQL and Python

---

### Question 15

Fill in the blank to successfully create a table in Databricks using data from an existing PostgreSQL database:

```sql
CREATE TABLE employees
  USING ____________
  OPTIONS (
    url "jdbc:postgresql:dbserver",
    dbtable "employees"
  )
```

  * [x] org.apache.spark.sql.jdbc
  * [ ] postgresql
  * [ ] DELTA
  * [ ] dbserver
  * [ ] cloudfiles

- **Overall explanation**:  
  Using the JDBC library, Spark SQL can extract data from any existing relational database that supports JDBC, including databases like MySQL, Postgres, SQLite, and more. The correct JDBC option for PostgreSQL is `org.apache.spark.sql.jdbc`.

- **Reference**:  
  [Spark SQL JDBC Options](https://learn.microsoft.com/en-us/azure/databricks/external-data/jdbc)

- **Study materials** from our exam preparation course on Udemy:  
  * [Lecture]()

- **Domain**: ELT with Spark SQL and Python

---

### Question 16

Which of the following commands can a data engineer use to create a new table along with a comment?

- [x] 
    ```sql
    CREATE TABLE payments
    COMMENT "This table contains sensitive information"
    AS SELECT * FROM bank_transactions
    ```

- [ ] 
    ```sql
    CREATE TABLE payments
    COMMENT("This table contains sensitive information")
    AS SELECT * FROM bank_transactions

- [ ] 
    ```sql
    CREATE TABLE payments
    AS SELECT * FROM bank_transactions
    COMMENT "This table contains sensitive information"
    ```
- [ ] 
    ```sql
    CREATE TABLE payments
    AS SELECT * FROM bank_transactions
    COMMENT("This table contains sensitive information")
    ```

- [ ] 
    ```sql
    COMMENT("This table contains sensitive information")
    CREATE TABLE payments
    AS SELECT * FROM bank_transactions
    ```

- **Overall explanation**:  
  The CREATE TABLE clause supports adding a descriptive comment for the table. This allows for easier discovery of table contents.

- **Syntax**:  
  ```sql
  CREATE TABLE table_name  
  COMMENT "here is a comment"  
  AS query
  ```

- **Reference**:  
  [CREATE TABLE Syntax](https://docs.databricks.com/sql/language-manual/sql-ref-syntax-ddl-create-table-using.html)

- **Study materials** from our exam preparation course on Udemy:  
  * [Lecture]()
  * [Hands-on]()

- **Domain**:  
  ELT with Spark SQL and Python

---

### Question 17

A junior data engineer usually uses the `INSERT INTO` command to write data into a Delta table. A senior data engineer suggested using another command that avoids writing duplicate records.

Which of the following commands is the one suggested by the senior data engineer?

- [x] `MERGE INTO`
  
- [ ] `APPLY CHANGES INTO`

- [ ] `UPDATE`

- [ ] `COPY INTO`

- [ ] `INSERT OR OVERWRITE`

- **Overall explanation**:  
  `MERGE INTO` allows you to merge a set of updates, insertions, and deletions based on a source table into a target Delta table. With `MERGE INTO`, you can avoid inserting duplicate records when writing into Delta tables.

- **References**:  
  [MERGE INTO Syntax](https://docs.databricks.com/sql/language-manual/delta-merge-into.html)  
  [Data Deduplication with MERGE](https://docs.databricks.com/delta/merge.html#data-deduplication-when-writing-into-delta-tables)

- **Study materials** from our exam preparation course on Udemy:  
  * Hands-on  

- **Domain**:  
  ELT with Spark SQL and Python  

---

### Question 18

A data engineer is designing a Delta Live Tables pipeline. The source system generates files containing changes captured in the source data. Each change event has metadata indicating whether the specified record was inserted, updated, or deleted, in addition to a timestamp column indicating the order in which the changes happened. The data engineer needs to update a target table based on these change events.

Which of the following commands can the data engineer use to best solve this problem?

- [ ] `MERGE INTO`

- [x] `APPLY CHANGES INTO`

- [ ] `UPDATE`

- [ ] `COPY INTO`

- [ ] `cloud_files`

- **Overall explanation**:  
  The events described represent Change Data Capture (CDC) feed. CDC is logged at the source as events that contain both the data of the records along with metadata information, including an operation column indicating whether the specified record was inserted, updated, or deleted, and a sequence column that is usually a timestamp indicating the order in which the changes happened. You can use the `APPLY CHANGES INTO` statement to leverage Delta Live Tables CDC functionality.

- **Reference**:  
  [Change Data Capture with Delta Live Tables](https://docs.databricks.com/workflows/delta-live-tables/delta-live-tables-cdc.html)

- **Study materials** from our exam preparation course on Udemy:  
  * Lecture  
  * Hands-on  

- **Domain**:  
  ELT with Spark SQL and Python  

---

### Question 19

In PySpark, which of the following commands can you use to query the Delta table `employees` created in Spark SQL?

- [ ] `pyspark.sql.read(SELECT * FROM employees)`

- [ ] `spark.sql("employees")`

- [ ] `spark.format(“sql”).read("employees")`

- [x] `spark.table("employees")`

- [ ] Spark SQL tables cannot be accessed from PySpark.

- **Overall explanation**:  
  The `spark.table()` function returns the specified Spark SQL table as a PySpark DataFrame.

- **Reference**:  
  [SparkSession.table() Documentation](https://spark.apache.org/docs/2.4.0/api/python/_modules/pyspark/sql/session.html#SparkSession.table)

- **Study materials** from our exam preparation course on Udemy:  
  * Hands-on  

- **Domain**:  
  ELT with Spark SQL and Python  

---

### Question 20

Which of the following code blocks can a data engineer use to create a user-defined function (UDF)?

- [ ] 
    ```sql
    CREATE FUNCTION plus_one(value INTEGER)
    RETURN value +1
    ```

- [ ] 
    ```sql
    CREATE UDF plus_one(value INTEGER)
    RETURNS INTEGER
    RETURN value +1;
    ```

- [ ] 
    ```sql
    CREATE UDF plus_one(value INTEGER)
    RETURN value +1;
    ```

- [x] 
    ```sql
    CREATE FUNCTION plus_one(value INTEGER)
    RETURNS INTEGER
    RETURN value + 1;
    ```

- [ ] 
    ```sql
    CREATE FUNCTION plus_one(value INTEGER)
    RETURNS INTEGER
    value + 1;
    ```

- **Overall explanation**:  
  The correct syntax to create a UDF is:

  ```sql
  CREATE [OR REPLACE] FUNCTION function_name ( [ parameter_name data_type [, ...] ] )
  RETURNS data_type
  RETURN { expression | query }
  ```

- **Reference**:  
  [User Defined Functions Documentation](https://docs.databricks.com/udf/index.html)

- **Study materials** from our exam preparation course on Udemy:  
  * Hands-on  

- **Domain**:  
  ELT with Spark SQL and Python  

--- 

### Question 21

When dropping a Delta table, which of the following explains why only the table's metadata will be deleted, while the data files will be kept in the storage?

- [x] The table is external
- [ ] The table is deep cloned
- [ ] The user running the command has no permission to delete the data files
- [ ] The table is managed
- [ ] Delta prevents deleting files less than retention threshold, just to ensure that no long-running operations are still referencing any of the files to be deleted

**Overall explanation**:  
External (unmanaged) tables are tables whose data is stored in an external storage path by using a LOCATION clause. When you run `DROP TABLE` on an external table, only the table's metadata is deleted, while the underlying data files are kept.

**Reference**:  
[What is an unmanaged table?](https://docs.databricks.com/lakehouse/data-objects.html#what-is-an-unmanaged-table)

**Study materials** from our exam preparation course on Udemy:  
- [Lecture]()  
- [Hands-on]()  

**Domain**:  
ELT with Spark SQL and Python

---

### Question 22

Given the two tables `students_course_1` and `students_course_2`, which of the following commands can a data engineer use to get all the students from the above two tables without duplicate records?

- [x] 
    ```sql
    SELECT * FROM students_course_1
    UNION
    SELECT * FROM students_course_2
    ```
- [ ] 
    ```sql
    SELECT * FROM students_course_1
    CROSS JOIN
    SELECT * FROM students_course_2
    ```
- [ ] 
    ```sql
    SELECT * FROM students_course_1
    INTERSECT
    SELECT * FROM students_course_2
    ```
- [ ] 
    ```sql
    SELECT * FROM students_course_1
    OUTER JOIN
    SELECT * FROM students_course_2
    ```
- [ ] 
    ```sql
    SELECT * FROM students_course_1
    INNER JOIN
    SELECT * FROM students_course_2
    ```

**Overall explanation**:  
With `UNION`, you can return the result of `subquery1` plus the rows of `subquery2`. 

**Syntax**:  
```sql
subquery1
UNION [ ALL | DISTINCT ]
subquery2
```
If `ALL` is specified, duplicate rows are preserved. If `DISTINCT` is specified, the result does not contain any duplicate rows. This is the default.

Note that both subqueries must have the same number of columns and share at least a common type for each respective column.

**Reference**:  
[SQL UNION](https://docs.databricks.com/sql/language-manual/sql-ref-syntax-qry-select-setops.html)

**Study materials** from our exam preparation course on Udemy:  
- [Hands-on]()  

**Domain**:  
ELT with Spark SQL and Python

---

### Question 23

Given the following command:

```sql
CREATE DATABASE IF NOT EXISTS hr_db ;
```

In which of the following locations will the `hr_db` database be located?

- [x] dbfs:/user/hive/warehouse
- [ ] dbfs:/user/hive/db_hr
- [ ] dbfs:/user/hive/databases/db_hr.db
- [ ] dbfs:/user/hive/databases
- [ ] dbfs:/user/hive

**Overall explanation**:  
Since we are creating the database here without specifying a `LOCATION` clause, the database will be created in the default warehouse directory under `dbfs:/user/hive/warehouse`.

**Reference**:  
[CREATE DATABASE Syntax](https://docs.databricks.com/sql/language-manual/sql-ref-syntax-ddl-create-schema.html)

**Study materials** from our exam preparation course on Udemy:  
- [Lecture]()  
- [Hands-on]()  

**Domain**:  
ELT with Spark SQL and Python

---

### Question 24

Given the following table `faculties`:

Fill in the below blank to get the students enrolled in less than 3 courses from the array column `students`.

```sql
SELECT
  faculty_id,
  students,
  ___________ AS few_courses_students
FROM faculties
```

- [ ] 
    ```sql
    TRANSFORM (students, total_courses < 3)
    ```
- [ ] 
    ```sql
    TRANSFORM (students, i -> i.total_courses < 3)
    ```
- [ ] 
    ```sql
    FILTER (students, total_courses < 3)
    ```
- [x] 
    ```sql
    FILTER (students, i -> i.total_courses < 3)
    ```
- [ ] 
    ```sql
    CASE WHEN students.total_courses < 3 THEN students
    ELSE NULL
    END
    ```

**Overall explanation**:  
`filter(input_array, lambda_function)` is a higher-order function that returns an output array from an input array by extracting elements for which the predicate of a lambda function holds.

**Example**:  
Extracting odd numbers from an input array of integers:
```sql
SELECT filter(array(1, 2, 3, 4), i -> i % 2 == 1);
```
Output: `[1, 3]`

**References**:  
- [Filter Function](https://docs.databricks.com/sql/language-manual/functions/filter.html)  
- [Higher-Order Lambda Functions](https://docs.databricks.com/optimizations/higher-order-lambda-functions.html)  

**Study materials** from our exam preparation course on Udemy:  
- [Hands-on]()  

**Domain**:  
ELT with Spark SQL and Python

---

### Question 25

Given the following Structured Streaming query:

```python
(spark.table("orders")
        .withColumn("total_after_tax", col("total")+col("tax"))
    .writeStream
        .option("checkpointLocation", checkpointPath)
        .outputMode("append")
         .______________ 
        .table("new_orders")
)
```

Fill in the blank to make the query execute a micro-batch to process data every 2 minutes:

- [ ] trigger(once="2 minutes") 
- [x] trigger(processingTime="2 minutes")
- [ ] processingTime("2 minutes") 
- [ ] trigger("2 minutes")
- [ ] trigger()

**Overall explanation**:  
In Spark Structured Streaming, in order to process data in micro-batches at the user-specified intervals, you can use the `processingTime` keyword. It allows you to specify a time duration as a string.

**Reference**:  
[Configure Structured Streaming Trigger Intervals](https://docs.databricks.com/structured-streaming/triggers.html#configure-structured-streaming-trigger-intervals)

**Study materials** from our exam preparation course on Udemy:  
- [Lecture]()  
- [Hands-on]()  

**Domain**:  
Incremental Data Processing

--- 

### Question 26  

Which of the following is used by Auto Loader to load data incrementally?  
- [ ] DEEP CLONE  
- [ ] Multi-hop architecture  
- [ ] COPY INTO  
- [x] **Spark Structured Streaming**  
- [ ] Databricks SQL  

**Overall Explanation**:  
Auto Loader is based on Spark Structured Streaming. It provides a Structured Streaming source called cloudFiles.  

**Reference**:  
[Auto Loader Documentation](https://docs.databricks.com/ingestion/auto-loader/index.html)  

**Study Materials**:  
- [Lecture](link-to-lecture)  
- [Hands-on](link-to-hands-on)  

**Domain**: Incremental Data Processing  

---  

### Question 27  

Which of the following statements best describes Auto Loader?  
- [ ] Auto Loader allows applying Change Data Capture (CDC) feed to update tables based on changes captured in source data.  
- [x] **Auto Loader monitors a source location, in which files accumulate, to identify and ingest only new arriving files with each command run. While the files that have already been ingested in previous runs are skipped.**  
- [ ] Auto Loader allows cloning a source Delta table to a target destination at a specific version.  
- [ ] Auto Loader defines data quality expectations on the contents of a dataset and reports the records that violate these expectations in metrics.  
- [ ] Auto Loader enables efficient insert, update, deletes, and rollback capabilities by adding a storage layer that provides better data reliability to data lakes.  

**Overall Explanation**:  
Auto Loader incrementally and efficiently processes new data files as they arrive in cloud storage.  

**Reference**:  
[Auto Loader Documentation](https://docs.databricks.com/ingestion/auto-loader/index.html)  

**Study Materials**:  
- [Lecture](link-to-lecture)  
- [Hands-on](link-to-hands-on)  

**Domain**: Incremental Data Processing  

---  

### Question 28  

A data engineer has defined the following data quality constraint in a Delta Live Tables pipeline:  
`CONSTRAINT valid_id EXPECT (id IS NOT NULL) _____________`  

Fill in the above blank so records violating this constraint will be added to the target table and reported in metrics:  
- [ ] ON VIOLATION ADD ROW  
- [ ] ON VIOLATION FAIL UPDATE  
- [ ] ON VIOLATION SUCCESS UPDATE  
- [ ] ON VIOLATION NULL  
- [x] **There is no need to add ON VIOLATION clause. By default, records violating the constraint will be kept, and reported as invalid in the event log.**  

**Overall Explanation**:  
By default, records that violate the expectation are added to the target dataset along with valid records, but violations will be reported in the event log.  

**Reference**:  
[Delta Live Tables Expectations](https://learn.microsoft.com/en-us/azure/databricks/workflows/delta-live-tables/delta-live-tables-expectations)  

**Study Materials**:  
- [Hands-on](link-to-hands-on)  

**Domain**: Incremental Data Processing  

---  

### Question 29  

The data engineering team has a DLT pipeline that updates all the tables once and then stops. The compute resources of the pipeline continue running to allow for quick testing.  

Which of the following best describes the execution modes of this DLT pipeline?  
- [ ] The DLT pipeline executes in Continuous Pipeline mode under Production mode.  
- [ ] The DLT pipeline executes in Continuous Pipeline mode under Development mode.  
- [ ] The DLT pipeline executes in Triggered Pipeline mode under Production mode.  
- [x] **The DLT pipeline executes in Triggered Pipeline mode under Development mode.**  
- [ ] More information is needed to determine the correct response.  

**Overall Explanation**:  
Triggered pipelines update each table with whatever data is currently available and then shut down.  

In Development mode, the Delta Live Tables system eases the development process by:  
- Reusing a cluster to avoid the overhead of restarts. The cluster runs for two hours when development mode is enabled.  
- Disabling pipeline retries so you can immediately detect and fix errors.  

**Reference**:  
[Delta Live Tables Concepts](https://docs.databricks.com/workflows/delta-live-tables/delta-live-tables-concepts.html)  

**Study Materials**:  
- [Hands-on](link-to-hands-on)  

**Domain**: Incremental Data Processing  

---  

### Question 30  

Which of the following will utilize Gold tables as their source?  
- [ ] Silver tables  
- [ ] Auto Loader  
- [ ] Bronze tables  
- [x] **Dashboards**  
- [ ] Streaming jobs  

**Overall Explanation**:  
Gold tables provide business-level aggregates often used for reporting and dashboarding, or even for machine learning.  

**Reference**:  
[Medallion Architecture](https://www.databricks.com/glossary/medallion-architecture)  

**Study Materials**:  
- [Lecture](link-to-lecture)  

**Domain**: Incremental Data Processing  

---

### Question 31

Given the following streaming table `events`:

Fill in the blank to query the existing streaming table.

```sql
SELECT *
FROM ___________
```

- [ ] 
    ```sql
    spark.readStream("events")
    ```
- [ ] 
    ```sql
    spark.read
        .table("events")
    ```
- [x] 
    ```sql
    spark.readStream
        .table("events")
    ```
- [ ] 
    ```sql
    spark.readStream()
        .table("events")
    ```
- [ ] 
    ```sql
    spark.stream
        .read("events")
    ```

**Overall explanation**:  
To read from a streaming table in Spark Structured Streaming, use `spark.readStream.table("table_name")`. This allows you to query the streaming data.

**References**:  
- [Databricks Structured Streaming Documentation](https://docs.databricks.com/structured-streaming/index.html)  
- [Delta Lake on Databricks](https://docs.databricks.com/delta/index.html)  

**Study materials** from our exam preparation course on Udemy:  
- [Hands-on]()  

**Domain**:  
Incremental Data Processing

---

### Question 32

In multi-hop architecture, which of the following statements best describes the Bronze layer?

- [ ] It maintains data that powers analytics, machine learning, and production applications  
- [x] It maintains raw data ingested from various sources  
- [ ] It represents a filtered, cleaned, and enriched version of data  
- [ ] It provides a business-level aggregated version of data  
- [ ] It provides a more refined view of the data.

**Overall explanation**:  
The Bronze layer contains raw data ingested from various sources, serving as the foundation for subsequent data transformations and processing.

**References**:  
- [Databricks Glossary](https://www.databricks.com/glossary/medallion-architecture)  

**Study materials** from our exam preparation course on Udemy:  
- [Hands-on]()  

**Domain**:  
Incremental Data Processing

---

### Question 33

Given the following Structured Streaming query:

```sql
(spark.readStream
        .format("cloudFiles")
        .option("cloudFiles.format", "json")
        .load(ordersLocation)
     .writeStream
        .option("checkpointLocation", checkpointPath)
        .table("uncleanedOrders")
)
```

Which of the following best describes the purpose of this query in a multi-hop architecture?

- [x] The query is performing raw data ingestion into a Bronze table  
- [ ] The query is performing a hop from a Bronze table to a Silver table  
- [ ] The query is performing a hop from Silver table to a Gold table  
- [ ] The query is performing data transfer from a Gold table into a production application  
- [ ] This query is performing data quality controls prior to Silver layer  

**Overall explanation**:  
This query utilizes Auto Loader (cloudFiles) to ingest raw JSON data from `ordersLocation` into the Bronze layer, specifically into the `uncleanedOrders` table.

**References**:  
- [Databricks Auto-Loader Documentation](https://docs.databricks.com/ingestion/auto-loader/index.html)  
- [Databricks Glossary](https://www.databricks.com/glossary/medallion-architecture)  

**Study materials** from our exam preparation course on Udemy:  
- [Hands-on]()  

**Domain**:  
Incremental Data Processing

---

### Question 34

A data engineer has defined the following data quality constraint in a Delta Live Tables pipeline:

```sql
CONSTRAINT valid_id EXPECT (id IS NOT NULL) _____________
```

Fill in the above blank so records violating this constraint will be dropped:

- [ ] `ON VIOLATE DROP`
- [ ] `ON VIOLATE IGNORE`
- [x] `ON VIOLATE DROP`
- [ ] `ON VIOLATE RAISE ERROR`

**Overall explanation**:  
In Delta Live Tables, the `ON VIOLATE DROP` clause allows the pipeline to automatically remove records that do not satisfy the defined constraints, ensuring data quality.

**References**:  
- [Databricks DLT Documentation](https://docs.databricks.com/workflows/delta-live-tables/delta-live-tables-constraints.html)  

**Study materials** from our exam preparation course on Udemy:  
- [Hands-on]()  

**Domain**:  
Data Quality in Pipelines

---

### Question 35

A data engineer has defined the following data quality constraint in a Delta Live Tables pipeline:

```sql
CONSTRAINT valid_id EXPECT (id IS NOT NULL) _____________
```

Fill in the above blank so records violating this constraint will be dropped and reported in metrics.

**Options:**
- [x] 
    ```sql
    ON VIOLATION DROP ROW
    ```
- [ ] 
    ```sql
    ON VIOLATION FAIL UPDATE
    ```
- [ ] 
    ```sql
    ON VIOLATION DELETE ROW
    ```
- [ ] 
    ```sql
    ON VIOLATION DISCARD ROW
    ```
- [ ] 
    There is no need to add ON VIOLATION clause. By default, records violating the constraint will be discarded and reported as invalid in the event log.

**Overall explanation**:  
With `ON VIOLATION DROP ROW`, records that violate the expectation are dropped, and violations are reported in the event log.

**Reference**:  
[Delta Live Tables Expectations](https://learn.microsoft.com/en-us/azure/databricks/workflows/delta-live-tables/delta-live-tables-expectations)

**Study materials** from our exam preparation course on Udemy:  
- Hands-on

**Domain**:  
Incremental Data Processing

---

### Question 36

Which of the following compute resources is available in Databricks SQL?

**Options:**
- [ ] Single-node clusters
- [ ] Multi-nodes clusters
- [ ] On-premises clusters
- [x] SQL warehouses
- [ ] SQL engines

**Overall explanation**:  
Compute resources are infrastructure resources that provide processing capabilities in the cloud. A SQL warehouse is a compute resource that lets you run SQL commands on data objects within Databricks SQL.

**Reference**:  
[Databricks SQL Admin - SQL Endpoints](https://docs.databricks.com/sql/admin/sql-endpoints.html)

**Study materials** from our exam preparation course on Udemy:  
- Hands-on

**Domain**:  
Production Pipelines

---

### Question 37

Which of the following is the benefit of using the Auto Stop feature of Databricks SQL warehouses?

**Options:**
- [ ] Improves the performance of the warehouse by automatically stopping idle services
- [x] Minimizes the total running time of the warehouse
- [ ] Provides higher security by automatically stopping unused ports of the warehouse
- [ ] Increases the availability of the warehouse by automatically stopping long-running SQL queries
- [ ] Databricks SQL does not have Auto Stop feature

**Overall explanation**:  
The Auto Stop feature stops the warehouse if it’s idle for a specified number of minutes.

**Reference**:  
[Databricks SQL Admin - SQL Endpoints](https://docs.databricks.com/sql/admin/sql-endpoints.html)

**Study materials** from our exam preparation course on Udemy:  
- Hands-on

**Domain**:  
Production Pipelines

---

### Question 38

Which of the following alert destinations is Not supported in Databricks SQL?

**Options:**
- [ ] Slack
- [ ] Webhook
- [x] SMS
- [ ] Microsoft Teams
- [ ] Email

**Overall explanation**:  
SMS is not supported as an alert destination in Databricks SQL. In contrast, email, webhook, Slack, and Microsoft Teams are supported alert destinations in Databricks SQL.

**Reference**:  
[Databricks SQL Admin - Alert Destinations](https://docs.databricks.com/sql/admin/alert-destinations.html)

**Study materials** from our exam preparation course on Udemy:  
- Hands-on

**Domain**:  
Production Pipelines

---

### Question 39  
A data engineering team has a long-running multi-task job. The team members need to be notified when the run of this job completes.

Which of the following approaches can be used to send emails to the team members when the job completes?  
- [ ] They can use Job API to programmatically send emails according to each task status.  
- [x] **They can configure email notifications settings in the job page.**  
- [ ] There is no way to notify users when the job completes.  
- [ ] Only Job owner can be configured to be notified when the job completes.  
- [ ] They can configure email notifications settings per notebook in the task page.  

**Overall Explanation**:  
Databricks Jobs supports email notifications to notify users in case of job start, success, or failure. Simply click "Edit email notifications" from the details panel in the Job page. From there, you can add one or more email addresses.  

**Reference**: [Databricks Jobs Documentation](https://docs.databricks.com/workflows/jobs/jobs.html#alerts-job)  

**Study Materials**:  
- Hands-on  

**Domain**: Production Pipelines  

---

### Question 40  
A data engineer wants to increase the cluster size of an existing Databricks SQL warehouse.

Which of the following is the benefit of increasing the cluster size of Databricks SQL warehouses?  
- [x] **Improves the latency of the queries execution.**  
- [ ] Speeds up the startup time of the SQL warehouse.  
- [ ] Reduces cost since large clusters use Spot instances.  
- [ ] The cluster size of SQL warehouses is not configurable. Instead, they can increase the number of clusters.  
- [ ] The cluster size cannot be changed for existing SQL warehouses. Instead, they can enable the auto-scaling option.  

**Overall Explanation**:  
Cluster Size represents the number of cluster workers and the size of compute resources available to run your queries and dashboards. To reduce query latency, you can increase the cluster size.  

**Reference**: [Databricks SQL Admin Documentation](https://docs.databricks.com/sql/admin/sql-endpoints.html#cluster-size-1)  

**Study Materials**:  
- Hands-on  

**Domain**: Production Pipelines  

---

### Question 41  
Which of the following describes Cron syntax in Databricks Jobs?  
- [ ] It’s an expression to represent the maximum concurrent runs of a job.  
- [x] **It’s an expression to represent a complex job schedule that can be defined programmatically.**  
- [ ] It’s an expression to represent the retry policy of a job.  
- [ ] It’s an expression to describe the email notification events (start, success, failure).  
- [ ] It’s an expression to represent the run timeout of a job.  

**Overall Explanation**:  
To define a schedule for a Databricks job, you can either interactively specify the period and starting time or write a Cron Syntax expression. The Cron Syntax allows you to represent a complex job schedule that can be defined programmatically.  

**Reference**: [Databricks Jobs Documentation](https://docs.databricks.com/workflows/jobs/jobs.html#schedule-a-job)  

**Study Materials**:  
- Hands-on  

**Domain**: Production Pipelines  

---

### Question 42  
The data engineering team has a DLT pipeline that updates all the tables at defined intervals until manually stopped. The compute resources terminate when the pipeline is stopped.

Which of the following best describes the execution modes of this DLT pipeline?  
- [x] **The DLT pipeline executes in Continuous Pipeline mode under Production mode.**  
- [ ] The DLT pipeline executes in Continuous Pipeline mode under Development mode.  
- [ ] The DLT pipeline executes in Triggered Pipeline mode under Production mode.  
- [ ] The DLT pipeline executes in Triggered Pipeline mode under Development mode.  
- [ ] More information is needed to determine the correct response.  

**Overall Explanation**:  
Continuous pipelines update tables continuously as input data changes. Once an update is started, it continues to run until the pipeline is shut down.  

In Production mode, the Delta Live Tables system:  
- Terminates the cluster immediately when the pipeline is stopped.  
- Restarts the cluster for recoverable errors (e.g., memory leak or stale credentials).  
- Retries execution in case of specific errors (e.g., a failure to start a cluster).  

**Reference**: [Delta Live Tables Concepts](https://docs.databricks.com/workflows/delta-live-tables/delta-live-tables-concepts.html)  

**Study Materials**:  
- Hands-on  

**Domain**: Production Pipelines  

---

### Question 43  
Which part of the Databricks Platform can a data engineer use to grant permissions on tables to users?  
- [ ] Data Studio  
- [ ] Cluster event log  
- [ ] Workflows  
- [ ] DBFS  
- [x] **Data Explorer**  

**Overall Explanation**:  
Data Explorer in Databricks SQL allows you to manage data object permissions. This includes granting privileges on tables and databases to users or groups of users.  

**Reference**: [Databricks Data Access Control Documentation](https://docs.databricks.com/security/access-control/data-acl.html#data-explorer)  

**Study Materials**:  
- Hands-on  

**Domain**: Data Governance  

---

### Question 44  
Which of the following commands can a data engineer use to grant full permissions to the HR team on the table employees?  
- [ ] GRANT FULL PRIVILEGES ON TABLE employees TO hr_team  
- [ ] GRANT FULL PRIVILEGES ON TABLE hr_team TO employees  
- [x] **GRANT ALL PRIVILEGES ON TABLE employees TO hr_team**  
- [ ] GRANT ALL PRIVILEGES ON TABLE hr_team TO employees  
- [ ] GRANT SELECT, MODIFY, CREATE, READ_METADATA ON TABLE employees TO hr_team  

**Overall Explanation**:  
ALL PRIVILEGES is used to grant full permissions on an object to a user or group of users. It is translated into all the below privileges:  
- SELECT  
- CREATE  
- MODIFY  
- USAGE  
- READ_METADATA  

**Reference**: [Databricks Table ACLs Documentation](https://docs.databricks.com/security/access-control/table-acls/object-privileges.html#privileges)  

**Study Materials**:  
- Lecture  
- Hands-on  

**Domain**: Data Governance  

---

### Question 45  
A data engineer uses the following SQL query:  
```sql
GRANT MODIFY ON TABLE employees TO hr_team
```

Which of the following describes the ability given by the MODIFY privilege?  
- [ ] It gives the ability to add data from the table.  
- [ ] It gives the ability to delete data from the table.  
- [ ] It gives the ability to modify data in the table.  
- [x] **All the above abilities are given by the MODIFY privilege.**  
- [ ] None of these options correctly describe the ability given by the MODIFY privilege.  

**Overall Explanation**:  
The MODIFY privilege gives the ability to add, delete, and modify data to or from an object.  

**Reference**: [Databricks Table ACLs Documentation](https://docs.databricks.com/security/access-control/table-acls/object-privileges.html#privileges)  

**Study Materials**:  
- Lecture  
- Hands-on  

**Domain**: Data Governance  

---  