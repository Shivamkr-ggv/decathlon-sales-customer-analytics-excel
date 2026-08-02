# 🏆 Decathlon Sales & Customer Analytics Dashboard | Excel Project

An end-to-end Excel dashboard project that analyzes Decathlon's retail sales operations — revenue trends, customer behavior, product performance, and retention — to help business stakeholders make faster, data-driven decisions.

![Final Dashboard](screenshots/Decathlon_Sales_Dashboard_Overview.png)

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Problem](#-business-problem)
- [Dataset](#-dataset)
- [Tools & Skills Used](#-tools--skills-used)
- [Project Workflow](#-project-workflow)
  - [1. Data Cleaning & Preparation](#1-data-cleaning--preparation)
  - [2. Data Structuring](#2-data-structuring)
  - [3. Metric Formulas](#3-metric-formulas)
  - [4. Pivot Table Analysis](#4-pivot-table-analysis)
  - [5. Dashboard Design](#5-dashboard-design)
- [Key KPIs](#-key-kpis)
- [Dashboard Insights](#-dashboard-insights)
- [Repository Structure](#-repository-structure)
- [How to Use This Project](#-how-to-use-this-project)
- [Key Learnings](#-key-learnings)
- [Connect With Me](#-connect-with-me)

---

## 📖 Project Overview

Retailers like Decathlon generate massive volumes of daily transaction data, but without proper analysis this data rarely translates into actionable insight. This project builds a **fully interactive Excel dashboard** — powered by PivotTables, Pivot Charts, and formulas — that turns 30,000 raw order-level records into a single-screen decision-making tool for retail management.

The final deliverable is a dynamic **Decathlon Sales & Customer Analytics Dashboard** with year-based slicers, monthly filters, and visual KPIs covering revenue, orders, customers, AOV, and retention trends.

---

## 🎯 Business Problem

> **We need to create a Decathlon Sales & Customer Analytics Dashboard to consolidate raw transactional data into a single, self-service reporting view. This dashboard will help business stakeholders monitor revenue performance, customer behavior, and product trends, and make faster, data-driven decisions.**

The dashboard needed to answer the following business questions:

- Which **sports categories and products** are driving the most revenue and orders?
- How is revenue trending **month-on-month and year-on-year** (2024–2026)?
- Who are the customers (by **gender, segment, and membership type**) and how do they contribute to sales?
- What is the **customer retention rate**, and how does it change over time?
- Which **months, categories, or channels** need marketing or inventory attention?

---

## 🗃 Dataset

**File:** `Decathlon_Sales_Raw_Dataset.xlsx`
**Records:** 30,000 order-level transactions (2024–2026, synthetic)

| Column | Description |
|---|---|
| Order_ID / Order_Date / Order_Time | Unique order identifier and timestamp |
| Customer_ID / Customer_Name | Customer identity fields |
| Gender / Age / Age_Group | Customer demographic fields |
| City / State | Customer location |
| Membership_Type / Customer_Segment | Loyalty tier (Basic/Premium) and segment (New/Loyal) |
| Product_ID / Product_Name / Product_Category / Brand / Sport_Type | Product details |
| Quantity / Unit_Price / Discount_Percent / Discount_Amount | Order line items |
| Sales_Amount / Final_Amount / Cost_Price / Profit | Financial fields |
| Store_ID / Store_Name / Sales_Channel / Payment_Method | Store and channel details |
| Salesperson / Delivery_Type / Delivery_Days | Fulfillment details |
| Customer_Rating / Return_Status / Return_Reason | Post-purchase experience fields |
| Promotion_Campaign / Quarter / Month / Year | Marketing and time fields |

*Note: This is a synthetic dataset generated for learning and portfolio purposes and does not represent actual Decathlon business data.*

---

## 🛠 Tools & Skills Used

- **Microsoft Excel** (Excel Tables, PivotTables, Pivot Charts)
- **Excel Formulas** (SUMIFS, calculated fields) for AOV, YoY Growth, and Retention Rate
- **PivotTables & PivotCharts**
- **Slicers & Interactive Filters** (Year and Month)
- **Dashboard Design Principles** (KPI cards, chart layout, color theory)

---

## 🔄 Project Workflow

### 1. Data Cleaning & Preparation
The raw 30,000-row dataset was imported into Excel and structured as a formatted Excel Table. Fields were checked for blanks, duplicate records, and inconsistent formats before being used in calculations.

### 2. Data Structuring
Fields were organized into logical groups — **Order, Customer, Product, Store/Channel, and Time** — so PivotTables could summarize cleanly across each dimension without additional lookups.

### 3. Metric Formulas
Custom formulas were created to power the KPI cards and trend charts:

**Year-on-Year (YoY) Growth:**
```
= (This_Year_Sales - Last_Year_Sales) / Last_Year_Sales
```

**Average Order Value (AOV):**
```
= Total_Sales / Total_Orders
```

**Customer Retention Rate:**
```
= Repeat_Customers / Total_Customers
```

These formulas power the **YoY growth badges**, the **AOV KPI card**, and the **retention rate trend line** in the final dashboard.

### 4. Pivot Table Analysis
Multiple PivotTables were built on top of the dataset to summarize:
- Total sales, orders, customers, and AOV — with YoY % change
- Sales by product category, sports type, and gender
- Month-wise trend of customers, orders, and AOV
- Year-wise retention rate

![Pivot Table Report](screenshots/Decathlon_Pivot_Table_Analysis.png)

### 5. Dashboard Design
All pivot outputs were converted into charts (line, donut, bar) and assembled onto a single dashboard sheet with a **Year slicer (2024/2025/2026)** and **Month buttons (Jan–Dec)** for interactivity, giving stakeholders a self-service reporting tool.

---

## 📊 Key KPIs

| KPI | Value |
|---|---|
| **Total Sales** | ₹36.7 Cr (▲ 40.8%) |
| **Total Orders** | 30,000 (▲ 40.1%) |
| **Total Customers** | 8,998 (▲ 13.5%) |
| **Average Order Value (AOV)** | ₹12,236 (▲ 0.5%) |
| **Overall Customer Retention Rate** | 64.58% |
| **Top Sports Category** | Cycling — ₹8.1 Cr in sales |

---

## 💡 Dashboard Insights

- **Cycling is the clear top-performing category**, generating ₹8.1 Cr in sales — more than double the next closest category — followed by Outdoor (₹4.1 Cr), Running (₹3.5 Cr), Gym (₹3.3 Cr), and Hiking (₹3.3 Cr).
- **Gender contribution is nearly even**, with Female customers (₹18.4 Cr) contributing marginally more than Male customers (₹18.3 Cr) — sales are not gender-skewed.
- **Yearly sales growth is slowing**: revenue grew from ₹13.0 Cr (2024) to ₹13.1 Cr (2025, +1.06%), then declined to ₹10.6 Cr (2026, -18.88%) — a signal worth investigating for the 2026 slowdown.
- **Customer retention has trended downward across the year** — starting at 16.60% in January and dipping to 12.81% by November, before a slight rebound in December (14.66%), suggesting a need for stronger mid-to-late-year re-engagement campaigns.
- **Average Order Value stayed largely flat** (▲ 0.5% YoY at ₹12,236), indicating growth has come mainly from new orders and customers rather than higher spend per order.
- **Product category sales are fairly evenly distributed** outside of Cycling, with Fitness, Football, and Badminton all contributing similarly in the ₹2.7–3.3 Cr range — useful for balanced inventory planning.

---

## 📁 Repository Structure

```
Decathlon-Sales-Customer-Analytics-Excel/
│
├── README.md                                          # Project documentation (this file)
├── Decathlon_Sales_Analysis_Workbook.xlsx             # Final Excel file (Data, Pivots, Dashboard)
├── Decathlon_Sales_Raw_Dataset.xlsx                   # Raw dataset (30,000 rows x 39 columns)
├── Decathlon_Sales_Analysis_Problem_Statement.pdf     # Business requirement / problem statement
│
└── screenshots/
    ├── Decathlon_Sales_Dashboard_Overview.png         # Final interactive dashboard
    ├── Decathlon_Pivot_Table_Analysis.png             # PivotTable report view
    └── Decathlon_Dataset_Structure_Overview.png       # Raw dataset structure view
```

---

## 🚀 How to Use This Project

1. Clone or download this repository.
2. Open `Decathlon_Sales_Analysis_Workbook.xlsx` in **Microsoft Excel (2016 or later recommended for full Slicer support)**.
3. Go to the **Dashboard** sheet to interact with the Year slicer and Month filters.
4. Explore the **Pivot_Analyze** sheet to see the underlying PivotTable logic.
5. Refer to `Decathlon_Sales_Analysis_Problem_Statement.pdf` for the full business requirements behind the project.

---

## 🎓 Key Learnings

- Structuring a **large (30K-row) transactional dataset** into a clean Excel Table for reliable PivotTable analysis.
- Writing **Excel formulas** for dynamic business metrics — YoY Growth, AOV, and Customer Retention Rate.
- Designing a **recruiter/stakeholder-friendly dashboard layout** — KPI cards up top, filters accessible, charts grouped logically.
- Translating a **business problem statement** directly into measurable KPIs and visuals.

---

## 🔗 Connect With Me

If you found this project useful or have feedback, feel free to connect:

- **LinkedIn:** [add your LinkedIn URL here]
- **Email:** [add your email here]

⭐ If you like this project, consider giving this repository a star!
