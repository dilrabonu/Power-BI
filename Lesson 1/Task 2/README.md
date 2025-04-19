# 🌲 Alberta Field Validation Dataset – Power BI Dashboard

## 🔍 Project Overview

This project demonstrates the end-to-end process of **data cleaning, transformation, and visualization** using the **Alberta Field Validation Dataset** related to peatland land cover and wildfire ecosystem assessments in Alberta, Canada.

The original dataset contains multiple observational parameters including geolocation, ecosystem type, moisture levels, peat depth, plant species, and more. The final result is a fully interactive **Power BI dashboard** providing insights into land conditions, observer contributions, and environmental indicators.

---

## 📁 Dataset Information

- **Source**: NASA / NACP Peatland Wildfire Severity Study
- **Format**: `.csv` (58 columns × 351 rows)
- **Fields include**:
  - Site Name, Date, Latitude, Longitude
  - Peat Depth, Soil pH, Moisture, Ecosystem
  - Observer Names
  - Species and Growth Stage indicators

---

## 🛠️ Data Cleaning Tasks

Performed inside **Power BI Power Query Editor**:

- ✅ Removed unnecessary metadata rows
- ✅ Renamed columns for clarity (e.g., `Column2` → `Date`, `Column3` → `Latitude`)
- ✅ Replaced missing values:
  - `"not recorded"` → `"unknown"`
  - `-9999` → `null` or column mean
- ✅ Transformed data types (e.g., text → decimal, date)
- ✅ Removed duplicates and blank rows
- ✅ Replaced categorical placeholders with meaningful values

---

## 📊 Visualizations Created

The following visuals were built using the cleaned dataset:

| Visualization Type | Description |
|--------------------|-------------|
| 🗺️ Map              | Plots geolocation of sample sites using Latitude & Longitude |
| 📊 Bar Chart        | Distribution of land ecosystem types (`Ecosystem`) |
| 🥧 Pie Chart        | Moisture level categories across sites |
| 📈 Line Chart       | Peat Depth trend over observation dates |
| 🔘 Scatter Plot     | Relationship between Soil pH and Peat Depth |
| 🌳 Treemap          | Species name grouped by growth stage |

---

## 📌 Key Learnings

- Hands-on practice with Power BI’s **Power Query Editor** for data preprocessing
- Applied **data imputation techniques** (mean/mode) to fix missing values
- Built dynamic and interactive **dashboard visuals**
- Learned to categorize and restructure raw scientific data for analytics

---

## 📂 Files Included

- `Alberta_field_validation_data_variables.csv` – Cleaned dataset
- `PowerBI_Alberta_Wildfire.pbix` – Power BI project file
- `README.md` – Project summary

---

## 🚀 Next Steps

- Add time-based filtering and forecasting visuals
- Integrate weather datasets for enriched analytics
- Publish dashboard on Power BI Service (web)

---

## 🙋‍♀️ Author

**Dilrabo Khidirova**  
Data Scientist & AI Enthusiast  
 

---

## 📢 License

This project is for educational and demonstration purposes. Dataset is publicly available via NASA/ORNL open data.



  # TASK 2

  # Power BI + SQL Server Integration 🚀

This repository documents **Task 2** from my Power BI practical project focused on integrating and transforming data from a local SQL Server source.

## ✅ What I Did

1. **Connected to Local SQL Server**
   - Created dynamic parameters for `ServerName` and `DatabaseName`
   - Connected to the `ForestFire` database using these parameters in Power BI

2. **Imported Data Using Power BI**
   - Loaded data from SQL Server with both:
     - `Import` mode
     - `DirectQuery` mode
   - Observed performance and refresh behavior differences

3. **Transformed Data in Power Query**
   - Merged `month` and `day` columns to create a new `date` column
   - Cleaned and previewed the dataset for further visualization

## 🔍 Key Learnings

- How to parameterize SQL Server connections for reusable reports
- Differences between **Import** vs **DirectQuery**:
  - **Import** = faster visuals, offline capable
  - **DirectQuery** = real-time updates, server-side queries
- Power Query is powerful for merging/splitting and preparing data for dashboards

## 🛠 Tools Used

- Microsoft SQL Server (LocalDB)
- SQL Server Management Studio (SSMS)
- Power BI Desktop
- Power Query Editor

---


![image](https://github.com/user-attachments/assets/6ae85419-8bec-4e99-85c0-3d7498e874ba)

![image](https://github.com/user-attachments/assets/7caf40c3-67e3-483d-b8f7-3d68f34fc909)

![image](https://github.com/user-attachments/assets/9a6c74fb-181b-4768-bdda-7028033e75c7)


