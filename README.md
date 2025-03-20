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
<img width="1158" alt="Screenshot 2025-03-20 at 3 44 52 PM" src="https://github.com/user-attachments/assets/03ce032a-fffe-487d-b002-e25732fe8d24" />


## Azure Data Factory (ADF) Pipeline
### **Pipeline Execution Screenshot**
<img width="1439" alt="Screenshot 2025-03-20 at 3 16 33 PM" src="https://github.com/user-attachments/assets/48431774-a233-45cf-97b1-f96fe637875f" />


### **Data Transformation - ADF Data Flow**
<img width="1131" alt="Screenshot 2025-03-20 at 3 47 51 PM" src="https://github.com/user-attachments/assets/cb7aca20-cd79-4607-9b55-0cb16ca81483" />


## Azure SQL Database
### **Tables in Azure SQL**
<img width="1425" alt="Screenshot 2025-03-20 at 3 50 02 PM" src="https://github.com/user-attachments/assets/6d3e7038-20eb-48f4-b387-ed06e25afa84" />

#### **Customers Table**
<img width="1428" alt="Screenshot 2025-03-20 at 3 51 03 PM" src="https://github.com/user-attachments/assets/038be134-c293-411f-9952-1c2f5f3dc81c" />


#### **Sales Table**
<img width="1429" alt="Screenshot 2025-03-20 at 3 51 39 PM" src="https://github.com/user-attachments/assets/47e72579-a3ff-467c-880d-c1be79260781" />


#### **Products Table**
<img width="1422" alt="Screenshot 2025-03-20 at 3 52 14 PM" src="https://github.com/user-attachments/assets/25f06ed1-5370-43b3-8ab8-e5c6fa0e6f5b" />


## How to Run the Project

Clone the Repository:

- ** Execution Steps:

- Upload source CSV files (Customers & Products) to ADLS Bronze.

- Extract JSON data from GitHub and move it to ADLS Bronze.

- Configure and execute ADF Pipelines for transformation and loading.

- Validate data in Azure SQL Database.

- Use Power BI to build and visualize reports.

## ADF Pipeline & Data Flow

- Below are the key stages of the pipeline and transformation:

- Copy Data from HTTPS API → Load JSON to ADLS

- Transformation in the data flow 

- Get Metadata → Validate data structures

- ForEach Activity → Copy to azure SQL

## Data Flow Transformation:

- Filter and clean data from DS_Customers_Bronze, DS_Products_Bronze, DS_Sales_Bronze

- Apply transformations (Aggregations, Derived Columns, Selections)

- Load cleaned data into DS_Customers_Silver, DS_Products_Silver, DS_Sales_Silver

## Azure SQL Database Tables

- Final processed data is stored in Azure SQL Database with the following tables:

- dbo.Customers (Customer details)

- dbo.Products (Product details)

- dbo.Sales (Sales transactions)




### **Clone the Repository**
```sh
git clone https://github.com/phanikota08/AZ_RetailSales.git


## Screen Shots 

