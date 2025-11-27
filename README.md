# Retail Sales Data Exploration (SQL Server)

This repository contains a structured SQL Server script designed to perform end-to-end exploratory analysis on a retail sales dataset modeled using a star schema. The script helps in understanding the dataset, validating its consistency, and generating foundational business insights before building dashboards or advanced analytical models.

---

## Overview

The SQL script follows a clear, step-by-step analysis workflow:

1. Exploring database objects  
2. Profiling dimension tables  
3. Evaluating date ranges and customer ages  
4. Computing business KPIs  
5. Performing magnitude analysis  
6. Ranking products and customers  

Each step contributes to building a complete picture of the data and its business relevance.

---

## 1. Database Exploration

Examines metadata using `INFORMATION_SCHEMA` views:

- Lists all tables in the database.
- Retrieves column-level information.
- Establishes an overview of the schema structure and available objects.

---

## 2. Dimension Analysis

Explores key attributes from dimension tables:

- Customer demographics (country, gender, birthdate)
- Product attributes (category, subcategory, product name)

This helps identify grouping and segmentation opportunities for further analysis.

---

## 3. Date Range Exploration

Analyzes the temporal scope of the dataset:

- Finds earliest and latest order dates
- Computes the range in years and months
- Identifies youngest and oldest customers based on birthdate

---

## 4. Measures and KPI Calculation

Computes core business metrics:

- Total sales revenue
- Total quantity sold
- Average selling price
- Number of unique orders
- Total number of customers and ordering customers
- Total number of products

A combined KPI report is also generated using `UNION ALL` for quick reference.

---

## 5. Magnitude Analysis

Breaks down metrics by key dimensions:

- Customer count by country  
- Customer count by gender  
- Product count by category  
- Average product cost by category  
- Revenue contribution by category  
- Revenue contribution per customer  

Useful for understanding dominant categories, geographies, and customer segments.

---

## 6. Ranking Analysis

Identifies top and bottom performers:

- Top 5 highest revenue-generating products  
- Bottom 5 lowest performing products  
- Top 10 highest revenue customers  
- Three customers with the fewest orders  

These insights highlight extremes in business performance.

---

## Purpose

This script acts as a complete exploratory foundation for:

- Data quality validation  
- Business understanding  
- Dashboard creation (Power BI, Tableau, etc.)  
- Analytical model preparation  

---

## Requirements

- SQL Server (SQL Server 2017 or later recommended)
- A star-schema dataset containing:
  - `gold.fact_sales`
  - `gold.dim_customers`
  - `gold.dim_products`

---

## How to Use

1. Connect to your SQL Server environment.  
2. Execute the script section by section.  
3. Review outputs to understand the dataset and validate its structure.  
4. Use the insights as a foundation for further analytics or reporting.

---

## License

This project is available under the **MIT License**.

