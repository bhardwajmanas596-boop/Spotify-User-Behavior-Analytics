# Spotify User Behavior & Engagement Analytics

## 📌 Project Overview
This repository showcases an end-to-end data analytics project exploring a dataset of 50,000 Spotify user records. The project identifies key business insights surrounding customer retention (churn metrics), ad-to-premium conversion rates, demographic behavior, and feature requests. 

To demonstrate industry-standard data engineering and business intelligence practices, this project utilizes a **decoupled development architecture**. A local **MySQL Database** serves as the data warehousing layer for core extraction and query building, while **Power BI** manages advanced ETL data transformations, modeling, and interactive reporting.

---

## 🛠️ Tech Stack & Skills Showcased
* **Database Management:** MySQL (DDL Schema creation, Data Aggregation, Groupings, and Conditional Logic)
* **ETL Pipeline:** Power BI & Power Query (Feature engineering, field extraction, text-string normalization)
* **Analytical Modeling:** DAX (Data Analysis Expressions) for dynamic business metrics
* **Core Competencies:** Relational Database Schemas, Portfolio Presentation, Executive Data Storytelling

---

## 📊 Database Layer & SQL Production Queries
The dataset was engineered inside a local MySQL database instance. Initial data verification was conducted to isolate critical records, followed by optimization scripts to resolve query performance issues (such as aggregation boundaries and `GROUP BY` structural rules).

The production script file contains three core strategic queries:

### 1. Retention & Active Subscriber Summary
Tracks the overall distribution of active versus inactive users to map basic platform health.
```sql
SELECT subscription_status, COUNT(*) AS user_count 
FROM spotify_users 
GROUP BY subscription_status;
