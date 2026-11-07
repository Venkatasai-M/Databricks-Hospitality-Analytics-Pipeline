# Hospitality & Hotel Bookings End-to-End Data Engineering Pipeline

## Project Overview
This project demonstrates an end-to-end Data Engineering pipeline using the Medallion Architecture on Databricks with Spark, Delta Lake, and SQL. The goal is to ingest raw hotel booking transactions, cleanse and standardize the records, transform them into business-level aggregates, and build an Executive Hotel Performance Dashboard to track operational and revenue KPIs.

---

## Architecture & Workflow (Medallion Architecture)

1. **Bronze Layer (Raw Ingestion):**
   - Ingested raw hotel booking data from CSV (`hotel_bookings_raw.csv`).
   - Retained raw schema and applied initial data quality expectations without dropping data.

2. **Silver Layer (Cleaned & Standardized):**
   - Cleaned NULL values, handled cancellations, and removed inconsistent booking records.
   - Enforced schema constraints, derived calculated date flags, and prepared analytical tables.

3. **Gold Layer (Aggregated Business Metrics):**
   - Built optimized aggregate tables for executive reporting.
   - Created summary views focused on booking channels, cancellation trends, seasonal ADR (Average Daily Rate), and customer segments.

4. **Analytics & Visualization:**
   - Designed the **Executive Hotel Performance Dashboard** using Databricks SQL.
   - Generated key business visualizations: Revenue by Hotel Type, Monthly Booking Trends, Cancellation Analysis, and Lead Time Distributions.

---

## Key Business Insights Discovered
- **Revenue Driver:** City Hotels generate a higher volume of bookings, but Resort Hotels show significantly higher average daily spend during peak holiday seasons.
- **Cancellation Trends:** Bookings made with long lead times show higher cancellation rates, highlighting the need for dynamic deposit/cancellation policies.
- **Customer Segmentation:** Transient customers account for the majority of revenue, while corporate bookings offer stable low-cancellation patterns.

---

## Tech Stack
- **Platform:** Databricks
- **Storage & Engine:** Delta Lake, Apache Spark, Databricks SQL Warehouse
- **Languages:** SQL, Python
- **Reporting:** Databricks Dashboards & PDF Export
- **Version Control:** GitHub

---

## Repository Structure
```text
├── hotel_bookings_raw.csv                     # Raw input dataset
├── ETL_Pipeline.txt                           # Bronze, Silver, Gold transformations & SQL pipeline
├── Executive Hotel Performance Dashboard.pdf   # Exported executive dashboard report
└── README.md                                  # Complete project documentation
