# 🚀 Azure ETL Pipeline: Data Extraction, Transformation & Load

## 📌 Project Overview
This project implements an **ETL pipeline** using **Azure Data Factory, Databricks, and PySpark** to extract data from **SQL Server & GitHub**, process it through **Medallion Architecture (Bronze → Silver → Gold)**, and manage **incremental loads (SCD Type 1 - Upsert)** efficiently.

## 🏗️ Architecture & Workflow
### 🔹 **Data Sources**  
- **SQL Server** (Relational database)
- **GitHub** (Raw JSON data extraction)

### 🔹 **Pipeline Workflow**
1️⃣ **Data Ingestion** – Extracting data using **Azure Data Factory (ADF)**  
2️⃣ **Data Processing** – Copying data into a **staging table**  
3️⃣ **Incremental Data Handling** – Managing changes using **SCD Type 1 (Upsert)**  
4️⃣ **Transformations in Databricks** – Using **PySpark** and **Delta Lake**  
5️⃣ **Final Output** – Storing data in **fact & dimension tables** for analytics  

### 🔹 **Medallion Architecture Implementation**
- **Bronze Layer** → Raw ingested data
- **Silver Layer** → Cleaned & structured data
- **Gold Layer** → Aggregated & analytics-ready data

## 🛠️ Technologies Used
- **Azure Data Factory** – Data orchestration & pipeline execution
- **Azure Databricks** – Data transformation with **PySpark**
- **Delta Lake & Delta Tables** – Efficient storage & performance optimization
- **SQL Server** – Storing processed structured data

## 📌 Key Features
✅ **Incremental data loads** using a watermark column  
✅ **Slowly Changing Dimensions (SCD Type 1 - Upsert)**  
✅ **Optimized data pipeline execution**  
✅ **Parallel execution handling in ADF & Databricks**  

## 🏆 Challenges & Solutions
### 🔹 Handling Incremental Loads
- Implemented **watermark table** to track `last_load` timestamp
- Ensured **SCD Type 1 Upsert** to update records efficiently

### 🔹 Parallel Execution Issues
- Resolved data conflicts using **deduplication strategies** in fact_sales
- Ensured consistent schema evolution in **Delta Tables**

