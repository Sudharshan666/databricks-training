````markdown
# Databricks Training & SQL Analytics

![Databricks](https://img.shields.io/badge/Databricks-Analytics-orange)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-BigData-red)
![PySpark](https://img.shields.io/badge/PySpark-DataEngineering-yellow)
![SQL](https://img.shields.io/badge/SQL-Database-blue)
![CSS](https://img.shields.io/badge/CSS-Styling-purple)
![Status](https://img.shields.io/badge/Status-In%20Progress-green)

---

# Overview

This repository contains complete hands-on practice materials and implementations for learning:

- Databricks
- Apache Spark
- PySpark
- Spark SQL
- Data Engineering
- ETL Pipelines
- Delta Lake
- Streaming
- SQL Analytics
- CSS Operations

The repository is designed for beginners and intermediate learners who want practical exposure to building data engineering workflows and analytics solutions using Databricks.

Reference Repository:  
https://github.com/charan7929/databricks-training

---

# Repository Structure

```text
databricks-training/
│
├── Databricks/
├── PySpark/
├── SparkSQL/
├── SQL/
├── RDD/
├── DataFrames/
├── DeltaLake/
├── ETL/
├── Streaming/
├── Optimization/
├── AzureDatabricks/
├── CSS/
├── Projects/
├── Datasets/
└── README.md
```

---

# Topics Covered

# 1. Databricks Fundamentals

- Introduction to Databricks
- Databricks Workspace
- Notebook Creation
- Cluster Creation & Management
- DBFS (Databricks File System)
- Workspace Utilities
- Mount Points

---

# 2. Apache Spark Basics

- Introduction to Apache Spark
- Spark Architecture
- Driver & Executor
- Spark Context
- Lazy Evaluation
- DAG Execution

---

# 3. PySpark

- Introduction to PySpark
- PySpark DataFrames
- DataFrame Operations
- Filtering & Sorting
- Aggregations
- Column Transformations
- Handling Null Values

## Example

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("Demo").getOrCreate()

df = spark.read.csv("/FileStore/data.csv", header=True, inferSchema=True)

df.show()
```

---

# 4. RDD (Resilient Distributed Dataset)

- Creating RDDs
- RDD Transformations
- RDD Actions
- map()
- flatMap()
- filter()
- reduceByKey()

## Example

```python
rdd = sc.parallelize([1,2,3,4,5])

rdd.map(lambda x: x*x).collect()
```

---

# 5. Spark SQL

- SQL Queries in Databricks
- Temporary Views
- Global Views
- Joins
- Group By
- HAVING Clause
- Window Functions
- SQL Functions

## Example

```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department;
```

---

# 6. SQL Analytics

## SQL Basics

- SELECT Statements
- WHERE Clause
- ORDER BY

## Aggregation Functions

- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()

## Filtering Groups

- HAVING Clause

## SQL Joins

- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL OUTER JOIN

---

# 7. DataFrame Operations

- select()
- withColumn()
- drop()
- distinct()
- union()
- joins()
- groupBy()
- orderBy()

---

# 8. Joins in PySpark

- Inner Join
- Left Join
- Right Join
- Full Outer Join
- Cross Join
- Self Join

## Example

```python
emp.join(dept, emp.dept_id == dept.id, "inner")
```

---

# 9. Window Functions

- row_number()
- rank()
- dense_rank()
- lead()
- lag()

## Example

```python
from pyspark.sql.window import Window
from pyspark.sql.functions import row_number

windowSpec = Window.partitionBy("dept").orderBy("salary")

df.withColumn("rank", row_number().over(windowSpec))
```

---

# 10. ETL Pipeline

## Extract

- Read CSV Files
- Read JSON Files
- Read Database Tables

## Transform

- Data Cleaning
- Data Validation
- Removing Duplicates
- Business Logic Implementation

## Load

- Writing Processed Data
- Saving Delta Tables
- Exporting Reports

---

# 11. Delta Lake

- Delta Tables
- ACID Transactions
- Time Travel
- Schema Enforcement
- Schema Evolution
- Merge Operations

## Example

```python
df.write.format("delta").save("/delta/employees")
```

---

# 12. Data Cleaning

- Handling Missing Values
- Type Casting
- Removing Duplicates
- Standardization
- Data Validation

---

# 13. File Formats

- CSV
- JSON
- Parquet
- ORC

---

# 14. Streaming

- Structured Streaming
- Real-Time Data Processing
- Kafka Integration
- Streaming Pipelines

## Example

```python
stream_df = spark.readStream.format("csv").load("/stream")
```

---

# 15. Performance Optimization

- Caching
- Persistence
- Partitioning
- Repartition
- Broadcast Join
- Catalyst Optimizer
- Tungsten Engine

---

# 16. Azure Databricks

- Azure Storage Integration
- Azure Data Lake
- Mounting Storage Accounts
- Access Keys & Secrets

---

# 17. CSS Operations

## Basic CSS

- CSS Syntax
- Selectors
- Colors
- Background Color
- Font Styling
- Text Alignment

## CSS Box Model

- Margin
- Padding
- Border
- Width
- Height

## CSS Styling Example

```css
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
}

h1 {
  color: #2c3e50;
  text-align: center;
}

.container {
  margin: 20px;
  padding: 15px;
  border: 1px solid #ccc;
}
```

---

# 18. Real-Time Projects

- Sales Data Analysis
- Customer Analytics
- Employee Management System
- Banking Transactions
- E-Commerce Analytics

---

# Technologies Used

- Databricks
- Apache Spark
- PySpark
- Spark SQL
- Python
- SQL
- Delta Lake
- Azure Cloud
- Kafka
- CSS
- GitHub

---

# How to Run

## Step 1: Clone Repository

```bash
git clone https://github.com/your-username/databricks-training.git
```

---

## Step 2: Open Databricks

- Create Cluster
- Import Notebooks
- Upload Dataset Files

---

## Step 3: Execute Notebooks

Run notebooks sequentially based on topics.

---

# Learning Outcomes

After completing this repository, you will be able to:

- Work with Databricks efficiently
- Process big data using Spark
- Build ETL pipelines
- Use PySpark DataFrames
- Write Spark SQL queries
- Perform SQL Analytics
- Handle streaming data
- Optimize Spark jobs
- Work with Delta Lake
- Understand CSS operations and styling

---

# Future Enhancements

- Machine Learning Integration
- CI/CD for Databricks
- Advanced Spark Optimization
- Data Warehousing
- Cloud Deployment
- Advanced CSS & Frontend Integration

---

# Current Progress

- Databricks Fundamentals Completed
- SQL Fundamentals Completed
- Aggregation Concepts Completed
- Joins Practice Completed
- ETL Pipeline Practice Completed
- Delta Lake Concepts Added
- CSS Basic Operations Added
- Streaming Concepts In Progress

---

# Contributions

Suggestions and improvements are welcome.

---

# Author

**Sudharshan**  
B.Tech CSE Student | Data Engineering Learner

---

# License

This repository is created for educational and learning purposes.

---
````
