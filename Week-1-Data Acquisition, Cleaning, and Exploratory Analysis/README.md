# Week 1: Data Acquisition, Cleaning & Exploratory Data Analysis (EDA)

**Author:** Nune Venkata Yasasvi  
**Role:** Data Science Intern  
**Dataset:** Titanic Passenger Cleaned Dataset (891 records)  
**Environment:** Google Colab / Python 3  

---

## 📌 Project Overview
This repository contains the complete workflow for **Week 1: Data Acquisition, Cleaning, and Exploratory Analysis**. The objective of this project is to simulate real-world data preparation processes essential for data science pipelines—from gathering raw data to handling missing values, conducting exploratory analysis, and generating automated reports.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Automated Document Generation:** `python-docx`, `libreoffice`

---

## 📁 Repository Deliverables
```text
├── Week1_Data_Preparation_and_EDA.ipynb  # Primary Google Colab Notebook
├── Week1_Data_Preparation_and_EDA_Report.docx  # Word Document Report
├── Week1_Data_Preparation_and_EDA_Report.pdf   # PDF Version of Final Report
└── README.md                             # Project Documentation

```

---

## ⚙️ Data Preparation & Cleaning Methodology

| Step | Action Taken | Rationale & Justification |
| --- | --- | --- |
| **1. Deduplication** | Executed `df.drop_duplicates()` | Verified zero duplicate entries across the initial 891 records. |
| **2. Age Imputation** | Imputed missing `Age` with median per `Pclass` | Preserved socio-economic distribution instead of using global median. |
| **3. Embarked Imputation** | Filled missing `Embarked` with Mode (`"S"`) | Categorical missingness filled with the most frequent port of embarkation. |
| **4. Column Dropping** | Removed `Cabin` feature | Dropped due to excessive missing values (>77%), avoiding bias. |
| **5. Feature Encoding** | Converted `Survived`, `Pclass`, `Sex` to categorical | Corrected data types for appropriate statistical modeling and visualization. |

---

## 📊 Exploratory Data Analysis & Key Insights

1. **Demographic Disparity:**
* Female passengers demonstrated a drastically higher survival rate across all passenger classes compared to male passengers.


2. **Socio-Economic Class Impact:**
* First-class passengers (`Pclass 1`) achieved significantly higher survival rates, showing clear socio-economic stratification during evacuation.


3. **Fare Correlation:**
* Ticket fare shows a positive correlation (`+0.26`) with survival outcomes, reinforcing the socio-economic trend observed in class groupings.



---

## 🚀 How to Execute the Project

1. Open **Google Colab** ([colab.research.google.com](https://colab.research.google.com)).
2. Upload the `Week1_Data_Preparation_and_EDA.ipynb` file.
3. Run all code cells sequentially (`Runtime` ➔ `Run all`).
4. The notebook will automatically clean the dataset, generate and display 3 Seaborn visualizations, build the report, and trigger downloads for both `.docx` and `.pdf` files.

