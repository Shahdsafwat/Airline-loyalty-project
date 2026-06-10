# ✈️ Airline Loyalty Program — End-to-End Data Engineering & BI Project

## 📌 Overview
A complete end-to-end Data Engineering and Business Intelligence solution built on a Canadian Airline Loyalty Program dataset. This project covers the full modern data stack — from raw CSV ingestion through a structured 3-layer ETL pipeline, a Star Schema dimensional model, a semantic layer in SSAS Tabular, and a 5-page interactive Power BI dashboard.

Built as part of the **NTI Digital Egypt Youth HireReady Program — Track I016 (Data Engineering & Analytics)**.

---

## 🗂️ Dataset
| File | Rows | Description |
|------|------|-------------|
| Customer Loyalty History | 16,737 | Customer demographics, loyalty tier, CLV, enrollment & cancellation |
| Customer Flight Activity | 392,936 | Monthly flight records: flights, distance, points accumulated & redeemed |
| Calendar | 2,557 | Date dimension spanning 2012–2018 |

---

## 🏗️ Architecture

CSV Source Files → ODS Layer → STG Layer → DWH Layer → SSAS Tabular → Power BI

---

## 🔧 Tech Stack
- **ETL:** SQL Server Integration Services (SSIS)
- **Database:** SQL Server — ODS · STG · DWH
- **Semantic Layer:** SSAS Tabular (DAX)
- **Reporting:** Power BI (Live Connection to SSAS)
- **Language:** T-SQL · DAX · SSIS Expressions

---

## 📐 Data Modeling — Star Schema
| Dimension | Type |
|-----------|------|
| DIM_Date | Conformed + Role Playing x3 |
| DIM_City + DIM_Country | Snowflake |
| DIM_Gender | Static / Fixed |
| DIM_Education | Static / Fixed |
| DIM_Marital_Status | Static / Fixed |
| DIM_Enrollment_Type | Junk Dimension |
| Loyalty_Number in FACT | Degenerate Dimension |

---

## 📊 Dashboard Pages
| Page | Purpose |
|------|---------|
| Overview | Executive KPIs — churn rate, active customers, CLV, flight volume |
| Customers | Segmentation by tier, gender, education, enrollment trend |
| Flights | Seasonality, tier volumes, province distribution |
| Loyalty | Points economy, CLV by tier, redemption analysis |
| Geography | Customer distribution across Canadian provinces and cities |

---

## 💡 Key Business Insights
- **Aurora Paradox:** Aurora tier = highest CLV ($10,673) AND highest churn (13.1%)
- **Seasonality:** July peak (1.96 flights/month) vs February trough (0.82)
- **Low Redemption:** Only 1.54% of 796.55M accumulated points redeemed
- **Growth:** Total flights +28% from 2017 to 2018 (223K to 285K)
- **Concentration:** 78% of customers in 3 provinces — Ontario · BC · Quebec

---

## 📈 Project Stats
- **392,936** fact records processed
- **16,737** unique customers
- **3** ETL layers (ODS → STG → DWH)
- **7** dimension tables
- **15+** DAX measures
- **5** Power BI pages
- **3** SSIS packages
- **3** SSIS packages
