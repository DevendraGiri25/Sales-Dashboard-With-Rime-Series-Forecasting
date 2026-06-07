# 📊 Sales Performance Dashboard — Power BI + Time Series Analysis

## 📌 Project Overview

An interactive **Sales Performance Dashboard** built using **Power BI**, incorporating **Time Series Analysis** to track revenue trends, identify seasonal patterns, analyse regional performance, and forecast future sales across product categories.

This project demonstrates end-to-end business intelligence skills — from raw data cleaning and transformation to building a fully interactive dashboard with actionable insights.

---

## 🎯 Business Problem Statement

> *"Sales teams lack a centralized, visual view of their performance across time, regions, and product categories — making it hard to identify trends, spot underperforming areas, and plan for future growth."*

This dashboard solves that problem by providing:
- A **single view** of all key sales metrics
- **Time-based trend analysis** to track growth over months and quarters
- **Forecasting** to predict future revenue
- **Interactive filters** to slice data by region, product, and date

---

## 🗂️ Dataset Details

| Field | Details |
|---|---|
| **Source** | Kaggle (publicly available sales dataset) |
| **Type** | Retail / E-Commerce Sales Data |
| **Time Period** | Multi-year historical data |
| **Key Columns** | Order Date, Sales, Profit, Region, Category, Sub-Category, Customer Segment 

## ✨ Key Features

- 📈 **Time Series Analysis** — Monthly and quarterly sales trends visualized over multiple years
- 🔮 **Sales Forecasting** — Built-in Power BI forecast line predicting future revenue trajectory
- 🗺️ **Regional Performance** — Sales breakdown by region with comparative bar charts
- 🛍️ **Product Category Analysis** — Revenue and profit analysis across categories and sub-categories
- 🎛️ **Dynamic Slicers & Filters** — Filter entire dashboard by Date, Region, Category, and Segment
- 📊 **KPI Cards** — Quick snapshot of Total Sales, Total Profit, Profit Margin %, and YoY Growth

---

## 🖥️ Dashboard Visuals

| Visual | Purpose |
|---|---|
| KPI Cards | Total Sales, Total Profit, Profit Margin, YoY Growth |
| Time Series Line Chart | Monthly & quarterly sales trend over time |
| Forecast Line | Predicted future sales trajectory |
| Bar / Column Charts | Regional and category-wise performance comparison |
| Slicers & Filters | Dynamic filtering by Date, Region, Product Category |


---

## 🔑 Key Business Insights Discovered

1. **Seasonal Peak in Q4** — Sales consistently spike during October–December, indicating strong year-end demand
2. **Technology Category leads revenue** — Contributes the highest sales among all product categories
3. **West Region dominates** — Accounts for the highest share of total revenue across all years
4. **Furniture has low profit margins** — Despite decent sales volume, profit margins are significantly lower than other categories
5. **Steady YoY Growth trend** — Time series forecast indicates continued upward growth trajectory for the next quarter

---

## 🧮 Key DAX Measures

```DAX
-- Total Sales
Total Sales = SUM(Sales[Sales])

-- Total Profit
Total Profit = SUM(Sales[Profit])

-- Profit Margin %
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0) * 100

-- Month-over-Month Growth
MoM Growth % = 
DIVIDE(
    [Total Sales] - CALCULATE([Total Sales], DATEADD(Dates[Date], -1, MONTH)),
    CALCULATE([Total Sales], DATEADD(Dates[Date], -1, MONTH))
) * 100

-- Year-to-Date Sales
YTD Sales = TOTALYTD(SUM(Sales[Sales]), Dates[Date])

-- Previous Year Sales
PY Sales = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Dates[Date]))

-- Year-over-Year Growth %
YoY Growth % = DIVIDE([Total Sales] - [PY Sales], [PY Sales]) * 100
```

---

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard creation, visualization, forecasting |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Custom measures and KPI calculations |
| **Excel / CSV** | Raw data source from Kaggle |
| **Time Series Analysis** | Trend identification and sales forecasting |

---

## 📂 Repository Structure

```
PowerBI-Sales-Dashboard/
│
├── README.md                        ← Project documentation
├── Sales_Dashboard.pbix             ← Power BI dashboard file
│
├── dataset/
│   └── sales_data.csv               ← Kaggle dataset (cleaned)
│
└── screenshots/
    ├── dashboard_main.png           ← Main dashboard overview
    ├── time_series.png              ← Time series + forecast
    └── regional_analysis.png        ← Regional breakdown
```

## 🎓 Skills Demonstrated

- ✅ Data Cleaning & Transformation (Power Query)
- ✅ DAX Formula Writing (KPIs, Time Intelligence)
- ✅ Time Series Analysis & Forecasting
- ✅ Business Dashboard Design
- ✅ Data Storytelling & Insight Generation
- ✅ Regional & Category-Level Data Segmentation

---

## 👤 Author

**Devendra Giri**
MBA — Finance & Business Analytics
Department of Business Management, Nagpur

[LinkedIn](www.linkedin.com/in/devendragiri25)
[Email](devendragiri1225@gmail.com)

---

## 📃 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ **If you found this project helpful, please give it a star!** ⭐
