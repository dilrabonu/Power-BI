
# 📊 Power BI Sales Dashboard with Advanced DAX Time Intelligence & Cleaning

This Power BI project demonstrates a complete end-to-end sales analysis using **advanced DAX time intelligence functions** and **Power Query-based data cleaning**. It showcases best practices for modeling, transforming, and visualizing sales data professionally.

---

## 🚀 Project Overview

The goal of this project is to analyze shopping trends and sales performance using real-world customer shopping data. It covers everything from data import and cleaning to implementing DAX measures with **time-based filtering**, **text transformation**, and **conditional logic**.

---

## 📂 Key Components

### 📥 Data Import & Cleaning
- Imported raw dataset: `customer_shopping_data`
- Cleaned column names, removed nulls, and corrected data types
- Standardized date format for `invoice_date`
- Created a **custom Date Table** using DAX to enable advanced time intelligence

### 📅 Date Table (Calendar Dimension)
```dax
DateTable = 
ADDCOLUMNS (
    CALENDAR (
        MIN (customer_shopping_data[invoice_date]),
        MAX (customer_shopping_data[invoice_date])
    ),
    "Year", YEAR([Date]),
    "Month", FORMAT([Date], "MMMM"),
    "MonthNumber", MONTH([Date]),
    "Quarter", "Q" & FORMAT([Date], "Q")
)
 Advanced DAX Themes & Functions Used
🔁 Time Intelligence
Function	Purpose
DATESBETWEEN	Filter sales between two fixed dates
DATESINPERIOD	Analyze last N days/months/years relative to max date
NEXTDAY, NEXTMONTH, NEXTYEAR	Shift date range forward
PREVIOUSMONTH, PREVIOUSYEAR	Compare with previous periods
LASTDATE, FIRSTDATE	Retrieve boundary dates for filters or calculations

➗ Percentage & Division

Sales Percentage = 
DIVIDE([Sales Amount], [Total Sales])
🔤 Text Transformation
Function	Example
UPPER, LOWER	Standardize case
REPLACE, CONCATENATE	Clean & combine strings


CustomerInfo = CONCATENATE(customer_shopping_data[gender], "-", customer_shopping_data[payment_method])
🔎 Filtering & Context
Function	Use Case
ALL, ALLEXCEPT	Remove filters for % of total calculations


Sales % of Total = 
DIVIDE(
    SUM(customer_shopping_data[price]),
    CALCULATE(SUM(customer_shopping_data[price]), ALL(DateTable))
)
🧠 Conditional Logic
Function	Example
IF, SWITCH	Create dynamic categories or decisions


Category Type = 
SWITCH(TRUE(),
    customer_shopping_data[category] = "Clothing", "Apparel",
    customer_shopping_data[category] = "Technology", "Electronics",
    "Other"
)
📊 Measures Created
Total Sales Last 30 Days

Total Sales Last 3 Months

Sales % of Total

Category-Level Totals

Year-Over-Year Comparisons

Dynamic Time Navigation Using DATESINPERIOD and NEXTMONTH

📈 Visuals and Interactions
Bar charts by Month and Quarter

KPI cards for 30-day and 3-month metrics

Time-series slicers and tooltips

Filterable by gender, category, and payment method

🧠 Business Insights Enabled
Identify monthly trends and spikes

Compare seasonal performance

Spot shifts in category or gender-based sales

Show customer behavior insights with filters

🧠 Key Learning Outcomes
Mastery of DAX time functions (DATESINPERIOD, NEXTDAY, etc.)

Cleaned and modeled data for efficient reporting

Used ALL, ALLEXCEPT to control filter context

Combined string operations and conditional logic

Delivered a dashboard-ready Power BI report


![image](https://github.com/user-attachments/assets/4340b56b-eadd-41af-9c16-1e5b3b630b02)


![image](https://github.com/user-attachments/assets/1424e4e6-3736-4595-9c8b-91b3cce3e4f8)
