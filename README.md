# Project-Brazillian-Ecommerce

This repository contains the code and documentation for an Azure Data Pipeline designed to process and analyze Brazilian E-Commerce Public Dataset by Olist.

## Overview

This pipeline ingests raw data, transforms it into a usable format using a medallion architecture (Bronze, Silver, Gold), and stores it in Azure Data Lake Storage Gen2 (ADLS Gen2) for analysis.

## Architecture

![Architecture](https://github.com/user-attachments/assets/41da69c5-442c-4c2c-b1c8-846ba1325493)

**Explanation of Components**

* **Data Source :** Raw Data from Github via http link & SQL_Database via python.
* **Azure Data Factory:** Orchestrates the ingestion of data from the API to ADLS Gen2.
* **ADLS Gen2:** Azure Data Lake Storage Gen2, used for storing data at different stages:
    * **Bronze (3):** Raw data.
    * **Silver (2):** Cleaned and transformed data.
    * **Gold (1):** Aggregated and enriched data.
* **Azure Databricks:** Performs data transformation and processing, moving data from Bronze to Silver to Gold layers.
* **Azure Synapse Analytics:** Used for querying and analyzing the Gold layer data for reporting.
* **Visualization (Power BI):** Tool used for creating interactive dashboards and reports.

### Medallion Architecture:
![image](https://github.com/user-attachments/assets/cb33d04e-c5cf-4bd8-ad6b-f76486da4cea)


