# Instacart Data Analysis & ETL Project

# Overview

This project demonstrates an end-to-end data engineering and analytics workflow using the Instacart Online Grocery dataset. 
The goal is to extract, transform, and load the data, then perform exploratory analysis and visualizations to uncover insights about customer purchasing behavior.


#Dataset

The dataset used is the Instacart Online Grocery Dataset
 from Kaggle. It contains:

orders.csv — Information about each order (order_id, user_id, order_dow, order_hour_of_day, etc.)

products.csv — Product metadata (product_id, product_name, aisle_id, department_id)

aisles.csv — Aisle names and IDs

departments.csv — Department names and IDs

order_products__prior.csv & order_products__train.csv — Products included in each order and reorder information

# Project Workflow
1. Extract

Loaded CSV files into Pandas DataFrames.

Checked for missing values and inspected dataset structure.

2. Transform

Handled missing values (days_since_prior_order).

Optimized memory for large tables.

Merged tables to create an enriched fact table: order + product + aisle + department + reorder flag.

Engineered new features:

reorder_rate — fraction of orders where a product was reordered.

Aggregated metrics for orders by day of week.

3. Load

Saved cleaned and enriched datasets as CSV for future analysis or database ingestion.

Optional: Could be loaded into SQL/Postgres for production-ready ETL pipelines.

4. Analytics & Visualization

Top 10 Most Reordered Products

Visualizes which products are most likely to be reordered by customers.

Orders by Day of Week

Shows customer ordering trends across the week.

(Optional: Extend with market basket analysis, customer segmentation, or hourly ordering patterns.)

Technologies Used

Python — Pandas, NumPy

Visualization — Matplotlib, Seaborn

Data Storage — CSV (optionally SQL/Postgres)

Jupyter Notebook — Interactive development and documentation
