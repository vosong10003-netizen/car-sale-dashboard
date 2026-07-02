# 🚗 Classic Models — Car Sale Dashboard

An interactive sales analytics dashboard built from a relational SQL database, visualized using Chart.js in a single-file HTML application.

## 📊 Overview

This project transforms raw transactional data from the **Classic Models** database into a clean, dark-themed dashboard with real-time charts and KPI cards — replicating the type of report typically built in Power BI or Tableau, but entirely in the browser with no dependencies beyond a CDN.

## ✨ Features

- **KPI Cards** — Total Revenue ($9.60M), Profit ($2.07M), Orders (318), Customers (97)
- **Monthly Trend Line** — Revenue & Profit across Jan 2003 – May 2005
- **Doughnut Chart** — Revenue share by product line
- **Grouped Bar Chart** — Revenue vs Profit side-by-side per product line
- **Horizontal Bar Chart** — Top 10 countries by revenue
- **Product Table** — Top 10 products ranked with mini progress bars

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python + SQLite | Data extraction & aggregation from SQL dump |
| Chart.js 4.4 | All chart rendering |
| HTML / CSS | Single-file dashboard, no frameworks |

## 📁 Project Structure

```
car-sale-dashboard/
├── car_sale_dashboard.html   # Complete dashboard (open in any browser)
├── data.sql                  # Source MySQL database dump (classicmodels)
└── Car Sale.pbix             # Original Power BI file
```

## 🚀 Getting Started

No installation needed. Just open `car_sale_dashboard.html` in any modern browser.

```bash
open car_sale_dashboard.html
```

## 📈 Data Source

The dataset is the **Classic Models** sample database — a fictional retailer of scale model cars with tables for customers, orders, order details, products, employees, offices, and payments.

**Key metrics extracted:**
- Total revenue: **$9.60M** across 318 orders
- Most valuable product line: **Classic Cars** ($2.10M, 22% of revenue)
- Top market: **USA** ($3.14M, 33% of revenue)
- Top product: **2001 Ferrari Enzo** ($190,755)

## 📷 Preview

> Dark-themed dashboard with purple/blue accent colors, 5 chart types, and a ranked product table.

## 🔍 How It Was Built

1. Parsed the MySQL `.sql` dump using Python (regex-based row extraction)
2. Loaded data into SQLite for aggregation queries
3. Exported aggregated results and hard-coded them into Chart.js datasets
4. Styled with a dark `#0f1117` background matching modern BI tool aesthetics
