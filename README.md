# FMCG Lakehouse Data Engineering Project

##  Overview
This project implements an end-to-end Lakehouse architecture for an FMCG company scenario where a large enterprise (Atlikon) acquires a startup (Sports Bar).

The goal is to consolidate fragmented OLTP data into a unified analytics-ready platform using Databricks.

---

##  Architecture
- Amazon S3 – Landing & staging
- Databricks Free Edition
- Medallion Architecture (Bronze → Silver → Gold)
- Delta Lake
- SQL Views for BI
- Databricks Dashboard & Genie AI

---

## 🔁 Data Flow
S3 (CSV Files)
↓
Bronze (Raw Ingestion)
↓
Silver (Cleansing, Deduplication, Standardization)
↓
Gold (Star Schema + Aggregates)
↓
Dashboard & AI Insights


---

## 🧱 Data Model
- Fact Table: `fact_orders`
- Dimensions:
  - `dim_customers`
  - `dim_products`
  - `dim_date`
  - `dim_gross_price`

---

## 📊 Dashboard
Built using Databricks Dashboards on a denormalized Gold view:
- Monthly revenue trend
- Top products by revenue
- Revenue share by channel
- Customer & category analysis

Screenshots available in `/dashboards`.

---

## ⚙️ Orchestration
- Databricks Jobs
- Parameterized notebooks
- Incremental loads for fact tables
- Idempotent MERGE logic using Delta Lake

---

## 🛠 Tech Stack
- Python (PySpark)
- SQL
- Delta Lake
- Amazon S3
- Databricks Free Edition
- Medallion Architecture

---


