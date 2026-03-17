# 🚖 GoodCab – End-to-End Data Engineering Project

## 📌 Overview

GoodCab is an end-to-end data engineering project that simulates a real-world transportation system.
The project builds a scalable data pipeline using **Databricks, PySpark, and AWS S3**, following the **Medallion Architecture (Bronze → Silver → Gold)**.

---

## 🏗️ Architecture

![Architecture](architecture.png)

### 🔹 Flow:

Application → Relational DB → S3 → Databricks → Dashboard

* **Bronze Layer** → Raw data ingestion (Batch + Streaming)
* **Silver Layer** → Data cleaning, validation, transformation
* **Gold Layer** → Business-level aggregations for analytics

---

## ⚙️ Tech Stack

* **Languages:** Python, SQL
* **Frameworks:** PySpark, Databricks
* **Storage:** AWS S3, Delta Lake
* **Processing:** Structured Streaming, Auto Loader
* **Visualization:** Power BI / Databricks SQL

---

## 🔄 Data Pipeline

### 🥉 Bronze Layer

* Ingested raw data from S3
* Implemented:

  * Batch ingestion (City data)
  * Streaming ingestion (Trips data using Auto Loader)
* Enabled schema evolution and metadata tracking

---

### 🥈 Silver Layer

* Cleaned and transformed raw data
* Implemented:

  * Data validation rules (ratings, date checks)
  * Schema standardization
  * CDC (Change Data Capture) using SCD Type 1
* Built:

  * **City Dimension Table**
  * **Calendar Dimension Table**
  * **Trips Fact Table**

---

### 🥇 Gold Layer

* Created business-ready aggregated tables:

  * Daily city metrics (revenue, trips)
  * Peak hour analysis
  * Customer segmentation
  * City performance ranking

---

## 📊 Dashboard

* Built interactive dashboard showing:

  * Total trips & revenue
  * Peak demand hours
  * City-wise performance
  * Customer segmentation

---

## 🚀 Key Features

* ✅ End-to-end pipeline (ingestion → transformation → analytics)
* ✅ Streaming + Batch processing
* ✅ Incremental loading using Auto Loader
* ✅ Data Quality Checks
* ✅ CDC implementation (SCD Type 1)
* ✅ Scalable Medallion Architecture

---

## 📂 Sample Queries

```sql
SELECT city_id, COUNT(*) AS total_trips
FROM transportation.silver.trips
GROUP BY city_id;
```

---

## 🎯 Use Cases

* Ride-sharing analytics (Uber/Ola-like systems)
* Demand forecasting
* Revenue analysis
* Customer behavior analysis

---

## 🧠 Learnings

* Built real-world ETL pipeline
* Hands-on with Databricks & Spark
* Implemented streaming + CDC
* Designed scalable data architecture

---

## 📌 Future Improvements
* Real-time dashboarding
* Data quality monitoring tools
* CI/CD pipeline for deployment

---

## 🤝 Connect With Me

* LinkedIn:www.linkedin.com/in/rahul-kumar-yadav-b978a92a1
* Email:rahulyadavbitmesra4@gmail.com

⭐ If you like this project, give it a star!
