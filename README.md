# formula1_project_datapipeline

#### In this project, we used the Azure Cloud Services to design and orchestrate a data pipeline to perform data engineering operations (Ingestion, Transformation, Analysis, Load) on a Formula 1 Racing Dataset



# DATA
![formula1_ergast_db_data_model](https://github.com/nishchalvaishnav/formula1_project_datapipeline/assets/131749093/837c7090-554f-4f77-a4b2-7baf29336636)

# Tools
Python
PySpark
Azure Databricks
Azure Data Factory (ADF)
Azure Data Lake Storage Gen2 (ADLS)
Delta Lake

# Architecture
#### The solution used in this project is based on the "Modern analytics architecture with Azure Databricks" from the Azure Architecture Center:
![azure-databricks-modern-analytics-architecture](https://github.com/nishchalvaishnav/formula1_project_datapipeline/assets/131749093/9d02c72f-09cc-4a74-afb8-8cec1b5478ef)

# Project Structure
#### data - contains sample raw data from Ergast API.
#### set-up - notebooks to mount ADLS storages (raw, ingested, presentaton) in Databricks.
#### raw - contains SQL file to create ingested tables using Spark SQL.
#### ingestion - contains notebooks to ingest all the data files from raw layer to ingested layer. Handles the incremental data for files results, pitstopes, laptimes and qualifying.
#### trans - contains notebooks to transform the data from ingested layer to presentation layer. Notebook performs transformations to setup for analysis.
#### analysis - contains SQL files for finding the dominant drivers and teams and to prepare the results for visualization.
#### includes - includes notebooks containing helper functions used in transformations.
#### utils - contains SQL file to drop all databases for incremental load.
