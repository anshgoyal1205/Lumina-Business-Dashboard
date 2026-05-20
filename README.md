# Lumina-Business-Dashboard
Interactive Power BI dashboard analyzing sales, profit &amp; store performance across 4 pages with DAX measures, dynamic filters and Top/Bottom product toggle.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Project Overview

The **Lumina Business Dashboard** is a 4-page interactive Power BI report built to track and analyse sales performance, store-wise revenue, time-based trends, and profitability metrics for a fictional retail business — Lumina Co.

The dashboard is designed to support data-driven decision-making by presenting KPIs, variance analysis, and profit breakdowns in a clean, navigable interface.

---

## 📁 Dashboard Pages

| # | Page | Description |
|---|------|-------------|
| 1 | **Index** | Landing page with KPI summary, page navigation cards, and key business insights |
| 2 | **Store Analysis** | Revenue vs target by store, variance analysis, month filter |
| 3 | **Time Frame Analysis** | Quarterly trends, weekday vs weekend revenue, monthly target comparison |
| 4 | **Profit Analysis** | Profit by category, gender, age group, weekday, and Top/Bottom product toggle |

---

## 🗃️ Data Model

The report uses a **star schema** with the following tables:

**Fact Table:**
- `fact_table` — Order Date, Customer ID, Product ID, Sales Person ID, Quantity Sold, Quantity Returned, Payment Method

**Dimension Tables:**
- `customers_table` — Customer ID, First Name, Gender, Age, Customer Age Group, Date of Birth
- `products_table` — Product ID, Product Name, Category, Sales Price, Cost Price
- `sales_persons_table` — Sales Person ID, First Name, Last Name, Store Name, Date of Birth
- `monthly_store_targets` — Store ID, Month, Monthly Target
- `Dimension Date` — Date, Day Name, Day No, Month Name, Month No

**Calculated Tables:**
- `Key Measures` — All DAX measures stored in a dedicated measures table
- `Breakdown` — Field parameter for dynamic axis (Location / Customer)
- `TopBottom` — Parameter table for Top/Bottom product toggle

---

## 🔧 Tools & Technologies

- **Power BI Desktop**
- **DAX** — Calculated measures and columns
- **Power Query (M)** — Data transformation and cleaning
- **Field Parameters** — Dynamic axis switching
- **Bookmarks & Page Navigation** — Interactive UX

---

## 📐 DAX Measures Used

| Measure | Description |
|---------|-------------|
| `Total Revenue` | Sum of sales revenue |
| `Total Target` | Sum of monthly store targets |
| `Total Profit` | Revenue minus COGS |
| `COGS` | Total cost of goods sold |
| `% Profit Margin` | Profit / Revenue × 100 |
| `% Variance` | (Revenue - Target) / Target × 100 |
| `Variance` | Revenue - Target |
| `Above Target` | Flag for stores exceeding target |
| `MoM Growth` | Month-on-Month revenue growth % |
| `QoQ Growth` | Quarter-on-Quarter revenue growth % |
| `Avg Rev Per QTR` | Average revenue per quarter |
| `Total Qty Sold` | Total quantity sold |
| `Qty Returned` | Total quantity returned |
| `Refund Rate` | Returned / Sold × 100 |
| `Returned Rate` | Return rate measure |
| `Total Refund` | Total refund value |
| `Ranking` | Store ranking by revenue |
| `Ranking 2` | Secondary ranking measure |
| `Top Bottom Rank` | Dynamic rank for Top/Bottom toggle |
| `Variance Color` | Conditional color for variance visuals |
| `Avg Rev Color` | Conditional color for avg revenue line |
| `Variance % Indicator` | Indicator for variance direction |

---

## ✨ Key Features

- **Dynamic Top/Bottom Toggle** — Switch between Top 5 and Bottom 5 products by profit using a slicer connected to a parameter table
- **Field Parameter — Breakdown** — Dynamically switch X-axis between Location and Customer on the Profit Distribution chart
- **Page Navigation** — Button-based navigation across all 4 pages
- **Month Filter** — Filter Store Analysis by individual months
- **Conditional Formatting** — Variance values color-coded (teal = positive, orange = negative)
- **MoM % Labels** — Month-on-Month growth percentage labels on Profit by Month chart
- **Category ToolTip Page** — Custom tooltip page for enhanced interactivity

---

## 📊 Key Business Insights

- 💰 **Total Revenue: 5.4M** — exceeded annual target by **3.7%**
- 📈 **Total Profit: 2.30M** with a profit margin of **42.18%**
- 🏆 **Best performing store: Miller** — 646.1K revenue
- ⚠️ **Underperforming store: Novak PLC** — 175.1K below target (-24.6% variance)
- 🥤 **Soft Drink** is the top profit category at **0.72M (31% of total profit)**
- 👥 **Female customers** contribute slightly higher profit at **51.47%** vs Male 48.53%
- 📅 **August** recorded peak revenue at **486K**
- 📆 **Thursday** is the best performing weekday at **340.67K**
- 👴 **51+ age group** generates highest profit margin at **974K**
- 🏪 **10 active stores** | **600 distinct customers**
- 🥇 **Top product: Begin Brew** at **95K profit**

---

## 📂 Dataset Details

| Table | Approx. Rows | Key Fields |
|-------|-------------|------------|
| fact_table | Transactional data | Orders, Sales, Returns |
| customers_table | 600 customers | Demographics, Age Group |
| products_table | Multiple products | Category, Price, Cost |
| sales_persons_table | 10 stores | Store-wise staff |
| monthly_store_targets | 10 stores × 12 months | Monthly targets |
| Dimension Date | Full date table | Day, Month, Quarter |

---

## 🚀 How to Use

1. Download the `.pbix` file
2. Open in **Power BI Desktop** (free download from Microsoft)
3. Navigate using the **sidebar buttons** (Index page) or **top navigation buttons** (other pages)
4. Use slicers to filter by Month, Store Name, or Category
5. Use the **Top/Bottom toggle** on the Profit page to switch between best and worst performing products
6. Use the **Breakdown slicer** to switch Profit Distribution between Location and Customer view

---

## 👤 Author

**Ansh Goyal**
📧 anshgoyal1205@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/ansh-goyal-180b19212)

