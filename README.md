# Retail Sales Data Pipeline

## Project Overview
This project is a hands-on implementation of a retail sales data pipeline using Azure data services. It covers the full end-to-end process—from ingesting raw data from multiple source systems to transforming, validating, loading data into an Azure SQL Database, and visualizing insights in Power BI. The project is designed to provide practical experience with modern data engineering practices, focusing on scalability, security, and best practices for data quality.

## Key Objectives

- **Data Ingestion:** Extract data from multiple sources:
  - RESTful API
  - CSV files
  - On-Premises SQL Server
- **Data Storage:** Use ADLS Bronze for raw data and ADLS Silver for cleansed data.
- **Data Transformation:** Utilize ADF Data Flows for data cleansing and mapping.
- **Data Loading:** Load data into Azure SQL Database for reporting.
- **Data Visualization:** Build dashboards in Power BI.
- **Data Validations :** Implement quality checks.

## Architecture

The high-level architecture includes:
1. **Source Systems:** REST API, CSV files, and On-Prem SQL Server.
2. **Data Storage:** ADLS Bronze (raw) and Silver (transformed).
3. **Data Transformation:** Azure Data Factory for orchestrating pipelines.
4. **Target System:** Azure SQL Database.
5. **Visualization:** Power BI for reporting.
6. **Additional Components:** Integration runtimes, data validation, Schema enforcement.

<img width="979" alt="Screenshot 2025-03-17 at 2 06 56 AM" src="https://github.com/user-attachments/assets/79dbb3c7-da99-4dc1-9f2a-9d60a8d0992e" />

## Project Components

- **SQL Scripts:** DDL and DML for table creation and sample data.
- **ADF Pipelines & Data Flows:** JSON exports of pipeline configurations.
- **Architecture Diagram:** A draw.io diagram of the solution.
- **Documentation:** This README and additional docs.
- **Power BI Reports:** PBIX files for dashboards.

## Data Set

Dataset Source: [Kaggle AI Shop Dataset](https://www.kaggle.com/datasets/varunkumari/ai-shop-dataset)
## Azure Portal Resources
### **Azure Data Lake Storage (ADLS) - Bronze Container Overview**
![ADLS Bronze Container](./Screenshots/adls-bronze.png)

## Azure Data Factory (ADF) Pipeline
### **Pipeline Execution Screenshot**
![ADF Pipeline Execution](./Screenshots/adf-pipeline-execution.png)

### **Data Transformation - ADF Data Flow**
![ADF Data Flow](./Screenshots/adf-dataflow.png)

## Azure SQL Database
### **Tables in Azure SQL**
#### **Customers Table**
![Customers Table](./Screenshots/azure-sql-customers.png)

#### **Sales Table**
![Sales Table](./Screenshots/azure-sql-sales.png)

#### **Products Table**
![Products Table](./Screenshots/azure-sql-products.png)

## How to Run the Project
### **Clone the Repository**
```sh
git clone https://github.com/phanikota08/AZ_RetailSales.git


## Screen Shots 

