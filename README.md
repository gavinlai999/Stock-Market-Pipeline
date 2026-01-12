---

## 📌 Project Overview
This project demonstrates an **end-to-end real-time data pipeline** using the **Modern Data Stack**.  
We capture **live stock market data** from an external API, stream it in real time, orchestrate transformations, and deliver analytics-ready insights — all in one unified project.

![Architecture (1)](https://github.com/user-attachments/assets/6b49eb4d-4bf7-473d-9281-50c20b241760)


---

## ⚡ Tech Stack
- **Snowflake** → Cloud Data Warehouse  
- **DBT** → SQL-based Transformations  
- **Apache Airflow** → Workflow Orchestration  
- **Apache Kafka** → Real-time Streaming  
- **Python** → Data Fetching & API Integration  
- **Docker** → Containerization  
- **Power BI** → Data Visualization  

---

## ✅ Key Features
- Fetching **live stock market data** (not simulated) from an API  
- Real-time streaming pipeline with **Kafka**  
- Orchestrated ETL workflow using **Airflow**  
- Transformations using **DBT** inside Snowflake  
- Scalable cloud warehouse powered by **Snowflake**  
- Analytics-ready **Power BI dashboards**  

---

## 📂 Repository Structure

```text
real-time-stocks-pipeline/
├── producer/                     # Kafka producer (Finnhub API)
│   └── producer.py
├── consumer/                     # Kafka consumer (MinIO sink)
│   └── consumer.py
├── dbt_stocks/models/
│   ├── bronze
│   │   ├── bronze_stg_stock_quotes.sql
│   │   └── sources.yml
│   ├── silver
│   │   └── silver_clean_stock_quotes.sql
│   └── gold
│       ├── gold_candlestick.sql
│       ├── gold_kpi.sql
│       └── gold_treechart.sql
├── dag/
│   └── minio_to_snowflake.py
├── docker-compose.yml            # Kafka, Zookeeper, MinIO, Airflow, Postgres
├── requirements.txt
└── README.md                     # Documentation
```
---
