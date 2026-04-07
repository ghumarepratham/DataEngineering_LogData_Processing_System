# Log Data Processing System – Data Engineering Project

## Overview
This project builds an end-to-end data pipeline to process application-like log data using APIs. It converts raw semi-structured JSON data into structured insights such as error rates and user activity. The pipeline follows industry-standard practices like Medallion Architecture, incremental processing, and automated workflows and API Polling.

---

## Architecture
```
                            Source  
                             ↓
                            ADF 
                             ↓ 
                            ADLS
                             ↓ 
                            Databricks 
                             ↓ 
                            Bronze 
                             ↓ 
                            Silver
                             ↓ 
                            Gold
                             ↓ 
                            ADLS
                             ↓
                            Power BI   
```


## Medallion Architecture:  
```
Bronze → Silver → Gold

- Bronze: Raw API data ingestion (posts & comments)  
- Silver: Data cleaning, transformation, and error detection  
- Gold: Aggregated insights (error rates, user activity)  
```


## Technologies Used
```
- Azure Data Lake Gen2 (ADLS)  
- Azure Databricks (PySpark)  
- Delta Lake (ACID tables)  
- Azure Data Factory (ADF – pipelines & Scheduled triggers)  
- Unity Catalog  
- Power BI  
```


## Pipeline Flow
```
1. Fetch data from REST APIs (posts & comments)  
2. Store raw data in ADLS (Bronze layer)  
3. Load data into Delta tables in Databricks  
4. Clean and transform data in Silver layer  
5. Apply rule-based logic to detect errors from text  
6. Create aggregated Gold tables  
7. Visualize insights in Power BI  
```


## Automation & API Polling
```
- ADF pipeline runs on schedule (API polling)  
- Data stored in timestamp-based   
- Incremental load handled  
- Databricks notebooks triggered automatically by ADF 
```


## Key Concepts Implemented
```
- Medallion Architecture  
- API Polling  
- Incremental Load    
- Data Cleaning & Transformation  
- Rule-based Error Detection  
- Managed & External Tables  
- Unity Catalog  
```

## Output 
```
- Error Rate Analysis  
- User Activity Tracking  
- Store structured data in Lakehouse
- Created aggregated tables   
```


## Highlights
```
✔ End-to-end pipeline  
✔ Automated workflows  
✔ Scalable design  
✔ Real-world data engineering concepts   
```
