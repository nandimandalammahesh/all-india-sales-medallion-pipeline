# all-india-sales-medallion-pipeline

# All India Sales Data Pipeline — Medallion Architecture

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-FF0000?style=for-the-badge&logo=delta&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0089D6?style=for-the-badge&logo=microsoftazure&logoColor=white)

**A production-grade ETL pipeline built with Medallion Architecture showcasing end-to-end data engineering best practices.**

### 🎯 Project Overview
This project demonstrates a complete **Bronze → Silver → Gold** Medallion Architecture pipeline for **All India Sales Analytics** in the Consumer Durables domain (Washing Machines, Refrigerators, ACs, etc.).

- **100% synthetic data** — No real company, customer, or IFB data is used.
- Designed to look and feel exactly like real production pipelines used by top companies.
- Perfect for **resume**, **interview discussions**, and **portfolio showcase**.

**Domain**: All-India Dealer Network Sales (Daily batch processing)

### ✨ Key Features
- **Medallion Architecture** (Bronze → Silver → Gold)
- **Delta Lake** with MERGE (SCD Type 1) for Silver layer
- **Robust Data Quality (DQ)** checks with detailed rejection reporting
- **Partitioning + Z-Order** optimization
- **Derived business KPIs** (Net Revenue, Efficiency metrics, etc.)
- **Production-ready logging** and error handling
- **Two Gold tables** ready for Power BI / Tableau
- Fully automated single-file pipeline

### 🏗️ Architecture

| Layer   | Purpose                              | Key Operations                          | Storage Format |
|---------|--------------------------------------|-----------------------------------------|----------------|
| **Bronze**  | Raw landing zone                    | Append-only, immutable                  | Delta          |
| **Silver**  | Cleansed & enriched single source   | DQ rules, deduplication, MERGE, derived columns | Delta (partitioned) |
| **Gold**    | Aggregated KPIs for BI/Reporting    | Monthly state-wise + product performance | Delta (partitioned) |

### 🛠️ Tech Stack
- **Azure Databricks** (Community or Enterprise)
- **PySpark** + **Delta Lake**
- **Python 3**
- **ADLS Gen2** compatible (paths configured for demo)
- **Delta MERGE**, Window functions, Partitioning, Z-Order

### 📁 Project Structure


### 🚀 How to Run

1. Open **Databricks** → Create New Notebook
2. Paste the entire code from `all_india_sales_medallion_pipeline.py`
3. Run all cells
4. The pipeline will:
   - Generate synthetic All-India sales data
   - Process through Bronze → Silver → Gold
   - Print beautiful DQ report + previews
5. Export notebook as **.py** and push to GitHub

> **Note**: Works perfectly on **Databricks Community Edition** (no paid features required).

### 📊 Sample Outputs (What interviewers love to see)

- Data Quality Report with rejection rate
- Silver layer with net_revenue, month_year, etc.
- Gold tables:
  - `state_zonal_kpis` → State-wise monthly performance
  - `product_category_kpis` → All-India product performance

### 💼 Interview Talking Points
- How I implemented **Medallion Architecture** in production style
- Why I used **Delta MERGE** instead of overwrite
- Data Quality framework & business rule enforcement
- Partitioning strategy for query performance
- How this pipeline can be scheduled with **Databricks Workflows**

### 🔒 Important Note
> This project uses **completely synthetic data** generated on-the-fly.  
> No real company information, customer data, or IFB Industries logic is included.  
> Built purely for learning, portfolio, and interview purposes.

---

**Made with ❤️ by Nandimandalam Mahesh**

⭐ **Star this repo** if it helped you!  
Feel free to fork and customize for your own domain.

**Ready to impress in your next Databricks / Data Engineering interview?** 🚀

