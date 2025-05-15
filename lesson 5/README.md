
# 📊 Power BI Dashboard – Global Superstore Sales Analysis

This project presents an **interactive Power BI dashboard** built using the **Global Superstore dataset**, offering insightful analytics into sales, profit, discount, and customer behavior across multiple regions, categories, and cities.

## 📁 Dataset
- Source: [Superstore Excel Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- Type: Excel (.xlsx)
- Fields: Order ID, Product, Category, Region, Sales, Profit, Discount, Order Date, Customer, Segment, etc.

---

## 🎯 Project Objective

> Build a business intelligence dashboard that enables decision-makers to:
- Track regional and yearly performance
- Identify top-performing products and cities
- Monitor profit margins and discount effectiveness
- Perform drillthrough analysis and explore KPI targets interactively

---

## 🧰 Tools & Technologies

- **Power BI Desktop**
- **DAX** (Data Analysis Expressions)
- Excel for data cleaning

---

## 📈 Key Features

### 🔍 Visualizations
- **KPI Cards**: Total Sales, Profit, Profit Margin %, Discount, Quantity
- **Bar Charts**: Sales by Region, Profit by City, Top Products
- **Line Chart**: Sales Trend by Region and Year
- **Donut Chart**: Profit Margin by Region
- **Gauge Chart**: Sales vs Goal Target
- **Treemap**: Category and Sub-Category Breakdown

### 📊 Interactivity
- **Slicers**: Filter by Year, Category, Segment
- **Drillthrough**: Region → City-level breakdown
- **Dynamic Tooltips** (optional)
- **Bookmarks and Page Navigation**

---

## 💡 DAX Measures Used

```dax
Total Sales = SUM('Orders'[Sales])
Total Profit = SUM('Orders'[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
Sales YOY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Orders'[Order Date]))
Sum of Discount = SUM('Orders'[Discount])
Sum of Quantity = SUM('Orders'[Quantity])

📌 Business Insights
📍 West and East regions dominate in sales and profit.

🪑 Office chairs and executive furniture drive top revenue.

📉 Some cities operate at a loss—candidates for strategic review.

📅 Sales show consistent growth over time, especially in 2016.

🧪 Future Improvements
Add anomaly detection with Power BI AI visuals

Embed the report in a business portal or SharePoint

Schedule refresh with Power BI Service

📄 Author
👩‍💼 Dilrabo Khidirova
Data Scientist | AI Enthusiast | Power BI Developer

![image](https://github.com/user-attachments/assets/2ee47e9d-4fa9-4f6a-bcac-752375293959)


![image](https://github.com/user-attachments/assets/8d1214bc-1ae7-4567-80c4-49f754bc26d7)

![image.png](attachment:5e72704e-5c27-4de6-b468-32ea94a42ec2:image.png)
