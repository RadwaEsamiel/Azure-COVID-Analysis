# Azure-COVID-Analysis

## COVID-19 Data Engineering Solution Using Azure

### Overview
This project implements a data engineering solution using Azure Data Factory (ADF) to ingest, process, and store COVID-19 data from various sources. It supports reporting and future prediction models, leveraging multiple Azure technologies for an end-to-end data pipeline.

### Objectives
- Ingest COVID-19 and population data from different sources.
- Process and transform data for analysis and reporting.
- Implement ADF pipelines for data integration and transformation.
- Orchestrate workflows and establish dependencies between processes.
- Monitor and manage pipelines using Azure monitoring tools.

### Technologies Used
- **Azure Data Factory (ADF)**: Core tool for orchestrating data pipelines.
- **Azure Data Lake Storage Gen2 & Blob Storage**: For scalable storage of raw and processed data.
- **Azure SQL Database**: For structured data storage.
- **Azure Databricks**: For advanced data transformation.
- **Power BI**: For data visualization and trend analysis.
- **Azure DevOps**: For CI/CD integration and deployment of ADF artifacts.

### Data Ingestion
- **Azure Blob Storage & Data Lake Gen2**: Ingest population data to support machine learning models.
- **HTTP Clients (APIs)**: Ingest COVID-19 data from public datasets using HTTP clients.
- **Automation**: A dynamic pipeline reads from a JSON file to automate data ingestion and copying into Azure Data Lake.

### Data Transformation
- **Cases & Deaths Transformation**: Filtering, renaming, pivoting, and lookup operations to prepare data for analysis.
- **Hospital Admissions (Daily & Weekly)**: Aggregated and enriched hospital admissions data, split into daily and weekly streams, and transformed for analysis.

### Data Processing
- **Azure Databricks**: Performs advanced transformations via notebooks integrated with ADF pipelines for large-scale processing.

### Data Persistence
- **Azure SQL Database**: Stores transformed data for querying and reporting. Key tables include:
  - `cases_and_deaths`
  - `hospital_admissions_daily`
  - `hospital_admissions_weekly`
  - `population_by_age`

### Data Orchestration
- **Triggers**: Event-based, scheduled, and tumbling window triggers automate pipeline execution.
- **Pipeline Dependencies**: Manage workflow from data ingestion to transformation and loading.

### Power BI Reports
Key visualizations include:
- **Case Fatality Rate (CFR)**: Deaths as a percentage of cases.
- **Top 10 Countries**: By hospital occupancy vs population, and total cases vs population.
- **Hospital Admissions vs ICU Occupancy**: Insights into healthcare demand.
- **Map Visualization**: Bubble sizes represent total cases per country.
- **Demographics**: Shows top age groups by population per country.

### CI/CD Integration
- **Azure DevOps**: Manages version control and automated release pipelines for deploying ADF artifacts across environments.

### Outcome
The project provides a scalable framework for ingesting, processing, and reporting COVID-19 data trends, with potential for expansion into predictive analysis using machine learning models.
