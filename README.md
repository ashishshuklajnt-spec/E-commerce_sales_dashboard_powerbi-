## 📊 Ecommerce Sales Dashboard (Power BI)

An interactive **Ecommerce Sales Dashboard** built in **Power BI**, analyzing orders, revenue, profit, and customer behavior across categories, states, and payment modes using a relational data model and DAX measures.

---

## 📌 Project Overview

This project turns raw order and transaction data into a single interactive Power BI report. Two tables — **Orders** and **Details** — are linked in a one-to-many relationship and modeled with DAX to surface revenue, profit, and quantity trends across time, geography, product category, and payment method.

The report supports slicing by **quarter** and **state**, so the same visuals can be explored at a national or regional level without touching the underlying data.

---

## 🎯 Objectives

- Track core KPIs: Amount, Profit, Quantity, and Average Order Value (AOV)
- Analyze profit trends across months
- Identify top and bottom performing product sub-categories
- Understand customer payment preferences
- Break down sales by product category and by top customers
- Enable state- and quarter-level filtering for regional analysis

---

## 🖼️ Dashboard Preview

### Full Dashboard

![Ecommerce Dashboard Overview](screenshots-powerbi/dashboard_overview.png)

### KPI & Category Breakdown

![KPI and Category Breakdown](screenshots-powerbi/kpi_breakdown.png)

### Monthly Profit & Sub-Category Performance

![Monthly Profit and Sub-Category Performance](screenshots-powerbi/monthly_profit_subcategory.png)

---

## 🗃️ Data Model

Two tables connected in a **one-to-many relationship** on Order ID:

![Data Model](screenshots-powerbi/data_model.png)

| Table | Fields |
|---|---|
| **Orders_table_powerbi** (1) | City, CustomerName, Order Date, Order ID, State |
| **Details_table_powerbi** (\*) | Amount, AOV *(DAX measure)*, Category, Order ID, PaymentMode, Profit, Quantity |

`AOV` (Average Order Value) is a calculated DAX field on the Details table:
```dax
AOV = [Amount] / [Quantity]
```

---

## 🧩 What the Dashboard Covers

- **KPI Cards** — Total Amount, Total Profit, Total Quantity, Average Order Value
- **Profit by Month** — trend across the full year, highlighting loss months
- **Profit by Sub-Category** — Printers, Bookcases, Saree, Accessories, Tables
- **Quantity by Payment Mode** — COD, UPI, Debit Card, Credit Card, EMI split
- **Quantity by Category** — Clothing, Electronics, Furniture
- **Sales by Customer** — top customers by order amount
- **Sales by State** — regional performance
- **Slicers** — filter the entire report by Quarter or State

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Data modeling, DAX, report design |
| **DAX** | Calculated measures (e.g. AOV) |
| **Power Query** | Data shaping & transformation |

---

## 📁 Repository Structure

```
ecommerce-sales-dashboard
│
├── ecommerce_sales_dashboard.pbix    -- Power BI report file
│
├── screenshots-powerbi
│   ├── dashboard_overview.png
│   ├── kpi_breakdown.png
│   ├── monthly_profit_subcategory.png
│   └── data_model.png
│
└── README.md
```

---

## 💡 Key Insights

- **COD (Cash on Delivery)** is the dominant payment mode at **44%** of orders, followed by UPI at 21%.
- **Clothing** drives the largest share of quantity sold at **63%**, well ahead of Electronics (21%) and Furniture (17%).
- **Printers** is the strongest sub-category by profit; **Tables** contributes the least.
- Profit dipped into the negative in **May, July, September, and December** — worth investigating discounting or return patterns in those months.
- **November** is the strongest profit month of the year.
- Sales are concentrated among a small number of top customers, suggesting an opportunity to grow the broader customer base.

---

## 🚀 Skills Demonstrated

- Power BI Report Design
- Data Modeling (relationships, cardinality)
- DAX Measures
- Power Query / data transformation
- KPI Design
- Interactive Filtering (slicers)
- Business Intelligence & Dashboarding

---

## ⚙️ How to Open This Project

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
2. Clone or download this repository.
3. Open `ecommerce_sales_dashboard.pbix` in Power BI Desktop.
4. Use the Quarter and State slicers on the report to explore the data interactively.

---

## 🔮 Possible Extensions

- Add a second report page for customer-level deep dive (RFM segmentation)
- Add year-over-year comparison once multi-year data is available
- Publish to Power BI Service and embed a live report link
- Add tooltips/drill-through pages for state-level detail

---

## 👤 Author

**Ashish**
Dashboard built with Power BI Desktop

⭐ If you found this project useful, consider giving it a star!
