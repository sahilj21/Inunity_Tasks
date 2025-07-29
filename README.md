InUnity Takeaway Assessment – Data Engineering Facilitator

Project Title: Sales & Customer Analytics Pipeline

This project implements a batch data engineering pipeline using PySpark and SQL in Databricks, processing a sales transactions dataset. It includes cleaning, transformation, analysis, and data storage in Delta format.

Dataset

- Source: [Kaggle Sales Transactions Dataset](https://www.kaggle.com/datasets)
- Format: CSV
- Sample columns: `ORDERNUMBER`, `CUSTOMERNAME`, `SALES`, `ORDERDATE`, `PRODUCTLINE`, `TERRITORY`, etc.

Objective

- Ingest raw CSV data into Databricks using PySpark.
- Perform data cleaning and transformation.
- Run analytical queries (SQL + PySpark).
- Generate insights like top customers, category-wise profit, monthly sales, etc.
- Store transformed output as partitioned Delta tables.

Pipeline Architecture

```text
CSV (Raw Data)
     ↓
PySpark DataFrame (Cleaning & Transformation)
     ↓
Temp View (for SQL Queries)
     ↓
Aggregations (monthly sales, top customers)
     ↓
Stored as Delta Lake (partitioned)

Inunity_Tasks (structure)
sales-intelligence-dashboard/
│
├── data/                    
│   └── sales.csv            # Mention how to get it in README
│
├── notebooks/              
│   └── sales_pipeline.ipynb
│
├── scripts/                 # PySpark modules
│   ├── data_ingestion.py
│   ├── data_cleaning.py
│   ├── aggregations.py
│   └── utils.py             # (Optional helper functions)
│
├── sql/                     # SQL queries
│   └── reporting_queries.sql
│
├── output/                  # Sample outputs (screenshots)
│   ├── top_customers.csv
│   └── monthly_sales.csv
│
├── README.md
├── requirements.txt         # Only if needed
└── main.py                  # Pipeline runner 
