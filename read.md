# Azure Data Analytics Pipeline of Brazilian E-Commerce Public Dataset by Olist

This repository contains the code and resources for building an end-to-end data analytics pipeline on Microsoft Azure. The pipeline ingests data from various sources, transforms it using Azure Databricks, and finally visualizes it using Power BI via Azure Synapse Analytics.

## Architecture Overview
![Architecture](https://github.com/user-attachments/assets/c49ad9e3-c68b-463b-a651-1e9410ed2a20)

The pipeline consists of the following components:

1. **Data Sources:** Data is ingested from various sources, including:
   - **Databases**
     - **SQL Databases**
         1. **SQL Table:** Data extracted from relational databases (MySQLDB).
         2. **GitHub:** Data retrieved from GitHub repositories.
     - **NoSQL Databases**
         1. **MongoDB:** Provides a NoSQL database for storing tables used for data enrichment in Databricks.

2. **Azure Data Lake Storage Gen2 (ADLS Gen2):** Serves as the central data lake for storing raw and transformed data.
    - **Medallion Architecture**
![Medallion Architecture](https://github.com/user-attachments/assets/1c300dfb-650d-46ae-98ec-f16803a29777)

3. **Azure Data Factory:** Orchestrates the data ingestion process, moving data from source systems to Azure Data Lake Storage Gen2 (ADLS Gen2).
![ADF](https://github.com/user-attachments/assets/6b9cac31-2199-4716-8333-d21f54d70849)

4. **Azure Databricks:** A powerful Apache Spark-based analytics platform used for data transformation and enrichment.
    - **Workflow**
        - Read data from ADLS Gen2.
        - Perform basic transformation like cleaning, renaming & filtering.
        - Use join operation to integrate multiple datasets.
        - Enrich the data via MongoDB.
        - Perform aggregation & derive insights.
        - Write final data back to ADLS Gen2.
    - **Permission**
![Permission](https://github.com/user-attachments/assets/0b4dcef3-a43b-4804-a762-9678cd51a40c)
    - **Writing Back**
![Writing Back](https://github.com/user-attachments/assets/8f6a5509-d845-4e96-b66d-17ec90a12220)

5. **Azure Synapse Analytics:** A limitless analytics service that brings together enterprise data warehousing and big data analytics. It's used to query and prepare data for visualization.
6. **Power BI:** A business analytics service used to create interactive dashboards and reports for data visualization.







### Project Structure
<YOUR_REPOSITORY_DIRECTORY>/
    ├── data-factory/          # Azure Data Factory pipelines and linked services
    
    ├── databricks/            # Databricks notebooks and configurations
    
    ├── synapse/               # Synapse Analytics SQL scripts and configurations
    
    ├── powerbi/               # Power BI report files (.pbix)
    
    ├── scripts/               # Deployment and utility scripts
    
    ├── README.md              # Project documentation (this file)

              📂 project-root/
           ├── 📜 README.md  # Documentation
           
           ├── 📂 pipelines/  # ADF JSON pipeline configurations
           
           ├── 📂 notebooks/  # Databricks Notebooks
           
           ├── 📂 scripts/    # Helper scripts (Python, SQL)
           
           ├── 📂 data/       # Sample data files
           
           ├── 📂 reports/    # Power BI report files
           
           ├── 📷 Architecture.png  # Architecture diagram
