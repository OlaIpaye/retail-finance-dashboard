# Retail Finance Dashboard
This portfolio project demonstrates end-to-end data engineering and analytics from raw data ingestion, and transformation to a polished business intelligence layer.

![exploring data in big query using SQL](<screenshots/1. Exploring dataset in big query.png>)

## Project Goal
To build a "single version of the truth" for a retail finance team. The pipeline ingests a real eCommerce dataset, cleans and models it using dbt, and visualizes financial KPIs in an interactive Power BI dashboard.

## Tools
 
| Layer | Tool |
|---|---|
| **Source Data** | Google BigQuery (TheLook eCommerce public dataset) |
| **Transformation** | dbt Core with dbt-bigquery adapter |
| **Visualisation** | Power BI |

## Dataset

**TheLook eCommerce** is a fictitious clothing retailer dataset hosted natively in BigQuery under "bigquery-public-data.thelook_ecommerce". It includes customers, products, orders, inventory, and logistics data. Crucially, it contains both "cost" and "sale_price" fields, allowing for real gross margin calculations, a core requirement for a finance-focused dashboard.

## Project Structure

- retail-finance-dashboard/
  - docs/
    - part1-bigquery-setup.md - GCP setup and dataset exploration
    - part2-dbt-setup.md - dbt installation and configuration
    - part3-staging-models.md - Bronze to Silver: cleaning and testing
    - part4-mart-models.md - Silver to Gold: star schema and fact_sales
    - part5-power-bi.md - Dashboard and KPIs
  - screenshots/ - Supporting images referenced in docs
  - thelook_project/ - dbt project (models, tests, macros)
  - README.md

### Data Architecture

```
bigquery-public-data.thelook_ecommerce (Source)
└─ [Bronze Layer] - Raw tables, untransformed
   ↓    dbt staging models
   └─ [Silver Layer] - Cleaned, typed, renamed columns
      ↓ dbt mart models
      └─ [Gold Layer] - Star schema — ready for Power BI
```

### Key KPIs

* Year-on-year revenue growth
* Gross profit margin %
* Revenue and margin by product category
* Revenue by customer geography
* Order volume trends over time

### Project Progress Report

| Part | Focus | Status |
|----------|----------|----------|
| Part 1 | **GCP setup & BigQuery dataset exploration** | Done |
| Part 2 | **dbt installation & configuration** | In Progress |
| Part 3 | **Staging models — Bronze to Silver** | Not Started |
| Part 4 | **Mart models - Silver to Gold** | Not Started |
| Part 5 | **Power BI dashboard** | Not Started |

#### Why dbt?
Rather than writing and running SQL scripts manually, dbt provides:

* Automatic dependency resolution between models
* A built-in testing framework for data quality
* Auto-generated documentation
* Clean, modular, version-controlled SQL

#### Project Deadline

3rd May 2026

#### Contact

- Email: [ipayeola@outlook.com](mailto:ipayeola@outlook.com)
- LinkedIn: [Oladimeji Ipaye](https://www.linkedin.com/in/oladimeji-ipaye/)

Feel free to reach out via email for questions or collaboration.
