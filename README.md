markdown
# Databricks Sales Analysis Project

A beginner-friendly project demonstrating data processing, analysis, and machine learning using Databricks.

## Overview

This repository contains a comprehensive project that showcases:
- ETL workflows with Apache Spark
- Reliable data storage with Delta Lake
- Machine learning tracking with MLflow
- Data analysis and visualization

Designed as a portfolio piece for junior data professionals, it highlights real-world Databricks features in an accessible way.

## Key Technologies

| Technology       | Purpose                          |
|------------------|----------------------------------|
| Databricks       | Unified analytics platform       |
| Apache Spark     | Distributed data processing      |
| Delta Lake       | ACID-compliant data storage      |
| MLflow           | Experiment tracking              |
| Python & SQL     | Data manipulation and queries    |

## Project Structure
databricks-sales-analysis/
├── Sales_Analysis.ipynb # Main Databricks notebook
├── data/ # Dataset directory
│ └── Superstore.csv # Sample dataset (from Kaggle)
├── README.md # Project documentation
└── screenshots/ # Visual documentation

text

## Dataset

**Source:** [Superstore Sales Dataset on Kaggle](https://www.kaggle.com/datasets)

**Columns Include:**
- Order ID, Order Date, Ship Date
- Customer ID, Product Name
- Sales, Quantity, Discount, Profit
- Region, Category, etc.

## Setup Instructions

1. **Create Account**: Sign up for [Databricks Community Edition](https://community.cloud.databricks.com/)
2. **Set Up Cluster**:
   - Create a single-node cluster
   - Use latest runtime version
3. **Import Data**:
   ```python
   # Example upload code
   dbutils.fs.put("/FileStore/tables/Superstore.csv", local_file_path)
Run Notebook: Import and execute the notebook step-by-step
    ```

## Project Timeline
Day 1: Configuration & Data Exploration
Objectives:

Set up Databricks environment

Load dataset into Spark DataFrame

Perform initial exploration

Code Example:

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("SalesAnalysis").getOrCreate()
df = spark.read.csv("/FileStore/tables/Superstore.csv", header=True, inferSchema=True)
display(df.limit(5))
df.printSchema()
```
- Progress Update: Successfully loaded and explored the superstore table in Sales_Analysis notebook using the serverless environment. Challenge: Learned to troubleshoot cell execution by ensuring proper connection to the warehouse. Screenshot included below.

## Day 2: Data Cleaning & Delta Lake
Objectives:

Handle missing values and type conversions

Create calculated columns

Implement Delta Lake storage

## Day 3: Analysis & Machine Learning
Objectives:

Execute SQL queries for business insights

Generate visualizations

Build and track ML model

## Day 4: Documentation & Deployment
Objectives:

Export polished notebook

Complete documentation

Deploy to GitHub

## Results & Insights
To be updated upon project completion

## Screenshots
![Día 1 Screenshot](Screenshots Project/Day1_Screenshot.png)

## Lessons Learned
Key takeaways will be documented here

## Future Improvements
Integrate with cloud storage (S3/ADLS)

Implement advanced ML models

Add workflow scheduling

## License
MIT License - See LICENSE file for details