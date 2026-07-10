# 📊 Wide World Importers - Power BI Sales Analytics

## 📌 Project Overview
End-to-End Power BI Business Intelligence Report analyzing the 
**Wide World Importers (WWI)** distribution dataset — a real-world-style 
dataset spanning **26,397 sales transactions** across customers, products, 
employees, and geography.

Built as part of the **NTI Creativa Data Analytics Diploma**
at Cairo University Hub | 2026.

---

## 🔄 Project Journey: Before → After

This project started from a completely blank slate — just a raw data model 
with no report built on top of it.

| | Before | After |
|---|--------|-------|
| Report Pages | 1 (empty) | 4 (fully designed) |
| Visuals | 0 | ~63 |
| DAX Measures | 0 | 24+ (organized into 5 dedicated measure tables) |
| Relationships | Broken (mismatched key columns) | Fully corrected Star Schema |
| Data Quality | Raw, generic column names, corrupted values | Fully cleaned, renamed, correctly typed |
| Custom Features | None | ExtractedColor (matched against an 871-color lookup table) |

---

## 🗄️ Data Sources & Model

**Star Schema** — 1 Fact table, 5 Dimension tables:

| Table | Rows | Description |
|-------|------|--------------|
| FactSale | 26,397 | Core sales transactions (Quantity, Profit, Tax, Totals) |
| DimCustomer | 402 | Customer details, category, credit limit |
| DimStockItem | 672 | Product catalog, brand, size, pricing |
| DimCity | 13,028 | Geographic data — city, state, country, territory |
| DimDate | 1,459 | Calendar + Fiscal calendar (2013–2016) |
| DimEmployee | 212 | Employee & salesperson records |

**Data Cleaning (Power Query):**
- Renamed all generic columns (`Column1`, `Column2`...) to meaningful names
- Fixed corrupted values (`"?"` placeholders, broken Excel date serials)
- Removed unnecessary columns (Photo, Barcode, Discount, Country...)
- Built a custom **ExtractedColor** column — automatically detects product 
  color from its name using an 871-entry color lookup table

**Relationships:**
Originally broken (FactSale only linked to DimCity, using mismatched columns). 
Rebuilt as a proper Star Schema — FactSale correctly related to all 5 dimensions.

**Fiscal Calendar:**
Confirmed the company's fiscal year starts **November 1st** (not the calendar 
default), verified directly from the data (Dec 30, 2016 = Fiscal Month 2). 
All Fiscal Time Intelligence measures were built around this.

---

## 📐 DAX Measures Library (24+ Measures, 5 Organized Tables)

| Measure Table | Examples |
|----------|----------|
| **Core Sales & Profit** | Total Sales, Total Profit, Profit Margin %, Total Quantity, Total Transactions, Average Order Value |
| **Time Intelligence** | Sales YoY %, Sales PY, Sales YTD, Sales MTD |
| **Fiscal** | Sales Fiscal YTD, Profit Fiscal YTD (custom Nov–Oct fiscal year) |
| **Ranking** | Employee Sales Rank, Customer Sales Rank, Product Sales Rank, Top 20% Customer Profit Share % |
| **Customer & Product Analysis** | Distinct Customers, Sales per Customer, Distinct Products Sold, Repeat Customer Rate |

---

## 📄 Report Pages

### 1. Executive Overview
KPIs (Total Sales, Total Profit, Profit Margin, Sales YoY) · Monthly Sales 
trend vs Prior Year · Top 5 Buying States · Sales YTD vs Fiscal YTD combo chart

### 2. Customer & Geography Insights
Distinct Customers, Sales per Customer · Treemap by State/City · Top 10 
Customers · Full customer detail table with conditional formatting

### 3. Salesforce & Product Performance
Total Transactions, Top Salesperson · Sales by Employee · Top 10 Products · 
Product Quantity vs Profit Margin scatter analysis

### 4. Strategic Insights & Recommendations
A dedicated storytelling page distilling the 4 most important business 
takeaways from the entire analysis, each backed by a supporting mini-chart.

---

## 🔑 Key Business Insights

- 💰 **$19.88M** Total Sales | **$9.92M** Profit | **49.92%** Profit Margin
- 📈 **13.93%** Sales growth Year-over-Year
- 📍 **California** alone drives **44.4%** of total sales
- 🏆 Top salesperson (Sophia Hinton) outperforms the team average by **11.7%**
- 📦 Just **10 core products** contribute **34.7%** of total profit
- 👥 Top **20%** of customers generate **47.9%** of total profit

---

## 🎨 Design

Custom-branded report theme (built on the "SaaS App Look" base theme), 
consistent header with institutional branding across all 4 pages.

---

## 🛠️ Tools & Technologies

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-yellow?style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query-blue?style=flat)

---

## 📁 Files

| File | Description |
|------|--------------|
| `WWI_Dashboard.pbix` | Full Power BI Report (final version) |
| `screenshots/` | Preview images of all 4 pages |

---

## 👤 Author

**Mohamed Mostafa Hassan Afify**
- 📧 mohamedmhafify@gmail.com
- 💼 [LinkedIn](https://linkedin.com/in/mohamedmhafify)

---

⭐ If you found this useful, please star the repository!
