 Power BI Sales Dashboard – DAX Mastery & Visualization

🧠 What I Learned Today
Today’s Power BI session focused on mastering DAX functions, data modeling, and dashboard building. I worked hands-on with the Superstore dataset to explore the full lifecycle of building a functional and insightful BI dashboard.

📊 Dataset Used
Source: Kaggle Superstore Sales Dataset
File: powerbi-demo.xlsx
Key Columns:

Order Date, Ship Date

Sales, Profit, Quantity, Discount

Product Name, Category, Sub-Category

Region, City, State, Segment

✅ Key Concepts Covered
🧱 1. Data Cleaning & Preparation
Converted date columns (Order Date, Ship Date) using "Using Locale" method to fix format errors

Corrected data types:

Sales, Profit → Decimal Number

Quantity → Whole Number

Postal Code → Text

All categorical dimensions → Text

🧮 2. Basic DAX Measures
Created reusable explicit measures:

dax
Copy
Edit
Total Sales     = SUM(train[Sales])
Total Profit    = SUM(train[Profit])
Total Quantity  = SUM(train[Quantity])
Average Discount = AVERAGE(train[Discount])
Displayed using Card visuals for instant KPIs.

📆 3. Date & Time Calculated Columns
Created new columns to support dynamic time-based filtering:

dax
Copy
Edit
Order Year      = YEAR(train[Order Date])
Order Month     = FORMAT(train[Order Date], "MMMM")
Order Quarter   = "Q" & FORMAT(train[Order Date], "Q")
Order Weekday   = FORMAT(train[Order Date], "dddd")
🧠 4. Advanced DAX Techniques
🔸 CALCULATE() – Filter context manipulation
dax
Copy
Edit
Furniture Profit = CALCULATE(SUM(train[Profit]), train[Category] = "Furniture")
Sales West = CALCULATE(SUM(train[Sales]), train[Region] = "West")
🔸 FILTER() – Custom row-level filtering
dax
Copy
Edit
High Discount Sales = CALCULATE(SUM(train[Sales]), FILTER(train, train[Discount] > 0.2))
🔸 CONCATENATE() & CONCATENATEX() – Text operations
dax
Copy
Edit
Location = CONCATENATE(train[City], ", " & train[State])
Product List = CONCATENATEX(VALUES(train[Product Name]), train[Product Name], ", ")
🎨 Visualizations Built
KPI Cards: Total Sales, Profit, Quantity, Avg Discount

Bar Chart: Sales by Category

Line Chart: Monthly Sales Trend

Table: Product List per Category

Slicers: Year, Month, Region, Segment

📌 Skills Demonstrated
Data profiling and transformation in Power Query

Explicit vs Implicit measures

Reusable DAX patterns (SUM, CALCULATE, FILTER, FORMAT)

Dimension modeling for time-based analysis

Visual storytelling with KPI metrics & filters



Data Cleaning:
![image](https://github.com/user-attachments/assets/1d9997c7-8dbd-44da-a2ad-8972e7731caf)

![image](https://github.com/user-attachments/assets/47cf526e-d16d-469b-bf71-c8307155bae1)

![image](https://github.com/user-attachments/assets/1c56e8e4-d422-4367-82e3-5d2f1f292856)

![image](https://github.com/user-attachments/assets/12f4a57f-2e55-480a-8a39-2bf7168c99b4)

![image](https://github.com/user-attachments/assets/9bd5cff1-af39-4394-a8ae-282280a3070f)

