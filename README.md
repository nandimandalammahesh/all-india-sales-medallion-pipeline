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


