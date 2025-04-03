# Azure Data Analytics Pipeline with Databricks and Synapse

This repository contains the code and resources for building an end-to-end data analytics pipeline on Microsoft Azure. The pipeline ingests data from various sources, transforms it using Azure Databricks, and finally visualizes it using Power BI via Azure Synapse Analytics.

## Architecture Overview

![Architecture Diagram](<YOUR_IMAGE_LINK_HERE>)  *(Replace `<YOUR_IMAGE_LINK_HERE>` with the actual link to your architecture image)*

The pipeline consists of the following components:

- **Data Sources:** Data is ingested from various sources, including:
    - **SQL Table:** Data extracted from relational databases.
    - **GitHub:** Data retrieved from GitHub repositories.
- **Azure Data Factory:** Orchestrates the data ingestion process, moving data from source systems to Azure Data Lake Storage Gen2 (ADLS Gen2).
- **Azure Data Lake Storage Gen2 (ADLS Gen2):** Serves as the central data lake for storing raw and transformed data.
- **Azure Databricks:** A powerful Apache Spark-based analytics platform used for data transformation and enrichment.
- **MongoDB:** Provides a NoSQL database for storing tables used for data enrichment in Databricks.
- **Azure Synapse Analytics:** A limitless analytics service that brings together enterprise data warehousing and big data analytics. It's used to query and prepare data for visualization.
- **Power BI:** A business analytics service used to create interactive dashboards and reports for data visualization.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following:

- **Azure Subscription:** An active Azure subscription. If you don't have one, you can create a free account.
- **Azure CLI or PowerShell:** Installed and configured to interact with your Azure subscription.
- **Azure Data Factory:** Deployed in your Azure subscription.
- **Azure Data Lake Storage Gen2 (ADLS Gen2):** Deployed in your Azure subscription.
- **Azure Databricks Workspace:** Deployed in your Azure subscription.
- **MongoDB Atlas Cluster:** A MongoDB Atlas cluster with the necessary data for enrichment.
- **Azure Synapse Analytics Workspace:** Deployed in your Azure subscription.
- **Power BI Desktop:** Installed on your local machine for visualization.

### Deployment Steps

1. **Clone the Repository:**
   ```bash
   git clone <YOUR_REPOSITORY_URL>
   cd <YOUR_REPOSITORY_DIRECTORY>

2. **Configure Azure Resources:**

Create the necessary Azure resources using the Azure portal, Azure CLI, or PowerShell.
Update the connection strings and configurations in the code with your specific resource details (e.g., storage account names, database credentials, Databricks workspace URL, etc.).
[Editable Section: Add specific details about configuration steps for each resource here.]

3. **Deploy Data Factory Pipelines:**
   
Import the Data Factory pipelines from the repository into your Azure Data Factory instance.
Configure the linked services and datasets to connect to your data sources and ADLS Gen2.
[Editable Section: Add specific instructions for importing and configuring Data Factory resources.]

4. **Configure Databricks Jobs:**

Import the Databricks notebooks from the repository into your Databricks workspace.
Update the notebook parameters and configurations to match your environment.
Create Databricks jobs to execute the notebooks for data transformation and enrichment.
[Editable Section: Add specific instructions for configuring Databricks notebooks and jobs.]

5. **Set up Synapse Analytics:**

Create external tables in Synapse Analytics pointing to the transformed data in ADLS Gen2.
Develop SQL queries and views to prepare the data for Power BI.
[Editable Section: Add specific SQL scripts or instructions for setting up Synapse Analytics.]

6. **Connect Power BI to Synapse Analytics:**

Connect Power BI Desktop to your Synapse Analytics workspace.
Create visualizations and dashboards based on the prepared data.
[Editable Section: Add specific instructions for connecting Power BI and creating visualizations.]

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
