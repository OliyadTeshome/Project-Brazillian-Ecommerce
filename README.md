# Project-Brazillian-Ecommerce

This repository contains the code and documentation for an Azure Data Pipeline designed to process and analyze Brazilian E-Commerce Public Dataset by Olist.

## Overview

This pipeline ingests raw data, transforms it into a usable format using a medallion architecture (Bronze, Silver, Gold), and stores it in Azure Data Lake Storage Gen2 (ADLS Gen2) for analysis.

## Architecture

![Architecture](https://github.com/user-attachments/assets/9f6ede44-cbc1-4285-a384-25dd97783e65)

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
