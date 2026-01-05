# ⚡ End-to-End Data Engineering & ML Pipeline with PySpark

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Spark](https://img.shields.io/badge/Apache%20Spark-3.5.1-orange?logo=apachespark)
![Status](https://img.shields.io/badge/Status-Educational-green)

A comprehensive tutorial and implementation demonstrating how to harness **Apache Spark** and **PySpark** for a complete data workflow. This project covers data ingestion, complex transformations, SQL analytics, and building a Machine Learning model using Spark MLlib—all optimized for a single-node environment like Google Colab.

## 📋 Overview

This project simulates a real-world big data scenario using a dataset of user subscriptions. It demonstrates the power of Spark's distributed processing (simulated locally) to handle:
1.  **ETL Operations:** Cleaning, casting, and enriching raw data.
2.  **Advanced Analytics:** Using Window functions and SQL queries.
3.  **Machine Learning:** Predicting user subscription types ("Premium" vs. others) using Logistic Regression.
4.  **Data Persistence:** Efficient storage using Parquet.

## 🏗️ Pipeline Architecture

The workflow follows these distinct stages:

```mermaid
graph LR
    A[Raw Data] --> B(Spark DataFrame);
    B --> C{Transformations};
    C -->|Feature Eng| D[Window Functions & UDFs];
    C -->|Enrichment| E[Join with Country Data];
    E --> F[ML Pipeline];
    F --> G[Logistic Regression Model];
    E --> H[Parquet Storage];
