# Amazon-sales-excel-dashboard
An interactive Excel-based data analysis and dashboard project evaluating order transactions, customer segments, regional targets, and logistical performance for Amazon e-commerce sales.
## 📊 Project Overview

Key transformations and feature engineering techniques applied:
Data Integration (XLOOKUP): Utilized to map Customer Name from the Customer Master and Product Category from the Product Master into the central transactions sheet using IDs.
Logistics Tracking: Calculated Delivery Time (in days) using basic date metrics:$$\text{Delivery Time} = \text{Delivery Date} - \text{Order Date}
Performance Classification: Segmented shipping performance conditionally using IF statements to tag fast-tracked orders (Delivery Performance = "Fast").
Financial Filtering: Built out metrics for Effective Sales to isolate successful financial income streams from cancelled orders, ensuring accounting accuracy:
                  $$\text{Effective Sales} = \text{IF}(\text{Delivery Status} = \text{"Cancelled"}, 0, \text{Total Amount})$$
                  
This repository contains a comprehensive sales analysis project that demonstrates end-to-end data processing inside Microsoft Excel—spanning from raw relational data tables to fully structured analytical views and aggregated KPIs. 

By leveraging advanced Excel functions and Pivot Tables, the project tracks order logistics, evaluates delivery fulfillment speeds, and compares sales performance metrics across five different geographical regions against their preset sales targets.

## 🗂️ Repository Structure
```text
├── data/
│   ├── customer_master.csv             # Customer profiles and demographic info
│   ├── product_master.csv              # Product catalog with cost pricing and categories
│   ├── region_goals.csv                # Sales performance targets per region
│   └── cleaned_dataset.csv             # Compiled transactional log with XLOOKUPs
├── analytics/
│   └── pivot_tables_and_calculations.csv # Extracted pivot summaries and metrics
└── Amazon_Sales_Dashboard.xlsx          # Main Excel Workbook containing the interactive dashboard
