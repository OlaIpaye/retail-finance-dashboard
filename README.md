# Retail Finance Dashboard
This portfolio project demonstrates end-to-end data engineering and analytics from raw data ingestion, and transformation to a polished business intelligence layer.

## Project Goal
To build a "single version of the truth" for a retail finance team. The pipeline ingests a real eCommerce dataset, cleans and models it using dbt, and visualizes financial KPIs in an interactive Power BI dashboard.

## Stack
 
| Layer | Tool |
|---|---|
| Source Data | Google BigQuery (TheLook eCommerce public dataset) |
| Transformation | dbt Core with dbt-bigquery adapter |
| Visualisation | Power BI |

## Dataset

**TheLook eCommerce** is a fictitious clothing retailer dataset hosted natively in BigQuery under "bigquery-public-data.thelook_ecommerce". It includes customers, products, orders, inventory, and logistics data. Crucially, it contains both "cost" and "sale_price" fields, allowing for real gross margin calculations, a core requirement for a finance-focused dashboard.

### 