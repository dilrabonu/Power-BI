# 🔥 Power BI Data Cleaning & Analysis — Lesson 1 Part 3

This repository contains the solution for **Lesson 1 - Part 3** of the Power BI practical tasks.  
The goal was to connect Power BI to a local SQL Server source and perform a full data cleaning workflow using **Power Query**.

---

## ✅ Task Overview

> ✔️ Connect to SQL Server  
> ✔️ Import data into Power BI  
> ✔️ Clean and transform data in Power Query  
> ✔️ Visualize insights in Power BI dashboard

---

## 📊 Steps Completed

### 1. Connected to SQL Server
- Created parameterized connection using `ServerName` and `DatabaseName`.
- Loaded `forestfires` table into Power BI.

### 2. Removed Unwanted Data
- Deleted unnecessary columns (e.g., indexes or empty columns).
- Disabled unwanted tables in the query panel.

### 3. Cleaned the Dataset
- ✅ **Removed duplicates** across relevant columns  
- ✅ **Filtered** rows to include only records for **August** and **September**  
- ✅ **Replaced values** to standardize abbreviations (e.g., `aug` → `August`)  
- ✅ **Changed column data types**:
  - Text → for categorical values (month, day)
  - Decimal → for continuous values (temp, wind, FFMC)
  - Whole Number → for counts (rain, area)

### 4. Applied All Changes
- Clicked `Close & Apply` to load cleaned data into the Power BI model.

---

## 📈 Dashboard Highlights

- ✅ **Stacked Column Chart**: Sum of area burned by weekday and wind level  
- ✅ **Line Chart**: Fire intensity (wind + area) across time  
- ✅ **Bubble Chart**: Multivariate view using X, Y, wind, and area  
- ✅ **Scatter Plot**: Relationship between temperature and area, color-coded by RH  
- ✅ **Rainfall Bar Chart**: Total rain by Merged Date

---

## 🎯 Outcome

> This project demonstrates how to build a full **ETL + Visualization workflow** in Power BI using Power Query.

You now have:
- A **clean and structured dataset**
- Insightful **data visualizations**
- A solid foundation for further **exploratory analysis**

---

## 🛠 Tools Used
- Microsoft Power BI Desktop
- Power Query
- SQL Server Express (Local)

---

## 📌 Author
**Dilrabo Khidirova**  
https://www.linkedin.com/in/dilrabo-khidirova-3144b8244/

---



![image](https://github.com/user-attachments/assets/8783845b-b26f-400d-b2e9-620ba7ddb759)


