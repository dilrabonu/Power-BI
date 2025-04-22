# 📊 Power BI Dashboard – Superstore Sales & Profit Performance

This Power BI project presents a professional, interactive dashboard created using the popular [Sample - Superstore dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final). The dashboard provides insights into sales, profit, customer behavior, and regional performance across various product categories.

---

## 🧩 Dataset Overview

- **Name:** Sample Superstore
- **Source:** Kaggle (CSV Format)
- **Size:** 9,994 records
- **Fields Include:**  
  - `Order Date`, `Ship Mode`, `Customer Name`, `Category`, `Sub-Category`  
  - `Region`, `Sales`, `Profit`, `Quantity`, `Discount`, `State`, `Segment`

---

## 🔧 Data Preparation (Power Query Editor)

The dataset was cleaned and transformed using Power BI's **Transform** and **Add Column** windows:

### Key Data Transformations:
- Promoted first row to headers
- Removed nulls and duplicate rows
- Detected and corrected data types
- Split text columns (e.g., full name or composite IDs)
- Extracted `Year`, `Month`, `Day` from `Order Date`
- Created new columns using `Add Column` tools
- Renamed columns for readability and analysis clarity

---

## 📈 Dashboard Features

The final dashboard includes the following:

### 💡 KPI Cards
- **🛒 Total Sales**  
- **💰 Total Profit**  
- **📦 Total Orders**  
- **👤 Unique Customers**

### 📊 Visuals & Charts
| Visual | Description |
|--------|-------------|
| **Sales by Category** | Clustered bar chart showing top-performing product categories |
| **Profit by Sub-Category** | Bar chart with conditional formatting (color-coded by profit) |
| **Sales Trend Over Time** | Line chart showing monthly sales performance |
| **Sales & Profit by State** | Map visualizing regional performance |

### 🧭 Slicers (Filters)
- Region
- Customer Segment
- Product Category

---

## 🎯 Key Insights

- 📌 **Technology** category drives the highest sales
- ❗ **Tables** in Furniture generate negative profit (cost concerns)
- 📈 Strong seasonal spikes in **Q4** indicate end-of-year purchase surges
- 🗺️ **California, New York, and Texas** are top-performing states

---

## 🛠 Tools & Technologies

- **Power BI Desktop**
- Power Query Editor
- Data modeling with relationships
- Visualization best practices (cards, filters, charts, maps)

---


