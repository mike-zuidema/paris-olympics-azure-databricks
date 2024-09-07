# Data Engineering Project: Paris Olympics 2024 Data Pipeline

## Project Overview
This project is focused on building a scalable data pipeline that extracts, transforms, and loads (ETL) data related to the Paris Olympics 2024. The primary goal was to gain experience with a variety of Azure data engineering tools. The pipeline handles raw data from HTTP sources, processes it using Azure Databricks and PySpark, and loads the transformed data into an Azure SQL database via Azure Synapse Analytics.

---

## Tools and Technologies Used
- **Kaggle**: Source of the raw data related to Paris Olympics 2024.
- **Azure Data Factory**: Used for orchestrating and moving the raw data from HTTP sources to Azure Storage Gen2.
- **Azure Storage Gen2**: Blob storage used for storing raw and transformed data.
- **Azure Databricks**: Employed for running a compute cluster to perform data transformations using PySpark within a Jupyter notebook.
- **PySpark**: The primary tool for transforming, partitioning, and cleaning the data.
- **Azure Synapse Analytics**: Used to spin up an Azure SQL Server, load transformed data into database tables, and run basic analyses.
- **Azure SQL Database**: The final destination for the transformed data, enabling easy querying and analysis.

---

## Project Workflow

### 1. **Data Extraction**
   - **Source**: Kaggle’s Paris Olympics 2024 dataset.
   - **Process**: 
     - Data was moved from the HTTP source (GitHub repo) to Azure Storage Gen2 using Azure Data Factory.
     - Data stored as raw files in a blob storage container.

### 2. **Data Transformation**
   - **Tool**: Azure Databricks (Jupyter notebook using Python and PySpark).
   - **Process**:
     - Connected Databricks to the raw data stored in Azure Storage Gen2.
     - Utilized PySpark to clean and transform the data:
       - Applied filtering, data normalization, and feature engineering.
       - Partitioned the data for efficient storage and processing.
     - Transformed data was written back to Azure Storage Gen2 in a separate directory.

### 3. **Data Loading and Analysis**
   - **Tool**: Azure Synapse Analytics.
   - **Process**:
     - Spun up an Azure SQL server.
     - Data from the transformed storage directory was loaded into Azure SQL Database.
     - Ran SQL queries to perform basic analysis on the tables, verifying the integrity of the data.

---

## Key Learning Objectives
The main purpose of this project was to explore and gain experience with multiple data engineering tools, especially within the Azure ecosystem. Many tools used in this project could perform overlapping functions; however, different tools were utilized to broaden my understanding of the available data engineering solutions:
- **Azure Data Factory** vs **Databricks** for ETL processes.
- **PySpark** for large-scale data transformations.
- **Azure Synapse** for data warehousing and SQL-based analysis.
- Integration and orchestration between various Azure services.

---

## Results
- Successfully implemented a data pipeline for the Paris Olympics 2024 dataset.
- Data was transformed and analyzed, yielding insights through basic SQL queries.
- Experience gained with Azure services, including Blob Storage, Databricks, Data Factory, and Synapse Analytics.

---

## Future Enhancements
- **Automation**: Automating the entire pipeline using Azure Data Factory triggers and scheduling for real-time updates.
- **Optimization**: Experiment with different storage formats (e.g., Parquet) to optimize the performance.
- **Visualization**: Integrate with Power BI or another tool to create dashboards for a visual representation of the results.
