# 🏒 Analyzing What Makes a Great Hockey Player

## 📖 Project Overview
This project aims to analyze **National Hockey League (NHL) player and team performance** over 19 years (2000-2019) using game statistics, player details, and spatial data. Our goal is to uncover **key factors contributing to success in ice hockey**, from player attributes to team strategies.

### 🔍 **Problem Statement**
What factors contribute to **team and player success** in ice hockey?

---

## 🗂 Data Pipeline (ETL Process)
We implemented a **pay-as-you-go ETL pipeline** to extract, transform, and load (ETL) NHL data into an **Azure SQL Database** for analysis using **Power BI**.

### 📥 **Extract**
- Data source: **NHL Game Data (2000-2019)**
- **13 CSV files** containing:
  - Game results
  - Player statistics
  - Team performance metrics
  - Game event logs (goals, penalties, shots, etc.)
- Extracted via **Kaggle API**, validated using **MD5 hashing** for integrity.

### 🔄 **Transform**
- **Azure Data Factory (ADF)** used for:
  - **Data cleaning**: Deduplication, missing value imputation, datatype conversion.
  - **Normalization**: Many-to-Many (M:M) relationships optimized.
  - **Entity-Relationship Diagram (ERD)** designed with **6 structured tables**.

### 📤 **Load**
- Data stored in **Azure SQL Database**.
- Connected to **Power BI** for visualization.
- **Challenges resolved:**
  - Foreign key constraints causing insertion failures.
  - Missing `player_id` records requiring filtering.

---

## 📊 Analysis & Insights

### 🏒 **Key Findings**
- **Athlete Career Span**: Peaks at **30 years old**, with an average career length of **10 years**.
- **Home Advantage Exists**: Home teams score **higher goals (2.94 avg.)** and win **55.95% of games**.
- **Player Attributes Matter**:
  - **Star players** tend to be **bulkier (180+ cm, 80-100kg)**.
  - **Goalies** have high **save percentages** and typically range from **25-35 years old**.
- **Third Period is Key**: Most goals are scored in the **third period**.
- **Spatial Data Analysis**:
  - **Shot locations** vary widely with no fixed pattern.
  - **Star coaches** have a win/loss ratio **above 1.14**.

---

## 📌 Tech Stack
- **Cloud & Database**: Azure SQL Database, Azure Data Factory, Power BI
- **ETL & Data Processing**: Python, Pandas, SQL, Kaggle API
- **Visualization**: Power BI, ydata-profiling (Pandas Profiling)
- **Data Storage & Management**: Azure Data Lake Gen 2

---

## 🚀 Next Steps
🔹 **Integrate Machine Learning**: Predict player performance using AI models.  
🔹 **Automate Data Updates**: Implement HTTP connectors for real-time dataset retrieval.  
🔹 **Optimize ETL Pipeline**: Use flowlets and parameterization for efficiency.  
🔹 **Advanced Analytics**: Develop an **Expected Goals** model for hockey predictions.  

---


