# Week 2: Advanced Data Visualization and Storytelling

**Author:** Nune Venkata Yasasvi  
**Role:** Data Science Intern  
**Dataset:** Expanded Titanic Survival Dataset (891 records)  
**Environment:** Google Colab / Python 3  

---

## 📌 Project Overview
This repository contains the complete codebase and report for **Week 2: Advanced Data Visualization and Storytelling with Python**. The objective of this project is to create multi-dimensional visual narratives that communicate complex data insights to both technical and non-technical stakeholders.

The project incorporates feature engineering (family sizing, fare binning) and 5 advanced Seaborn/Matplotlib visualizations to analyze demographic prioritization, socio-economic factors, and survival trends during the Titanic evacuation.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Report Generation:** `python-docx`, `libreoffice`

---

## 📁 Repository Deliverables
```text
├── Week2_Advanced_Data_Visualization.ipynb       # Executable Google Colab Notebook
├── Week2_Advanced_Data_Visualization_Report.docx  # Word Document Deliverable
├── Week2_Advanced_Data_Visualization_Report.pdf   # Standard PDF Submission Report
└── README.md                                      # Repository Documentation

```

---

## 📊 Visual Storytelling & Key Insights

| Visual | Chart Type | Core Narrative Insight |
| --- | --- | --- |
| **Visual 1** | Multi-Panel Distribution (HistPlot & KDE) | Highlights child prioritization during evacuation and shows that higher fare density strongly aligns with survival. |
| **Visual 2** | Pivot Table Heatmap | Illustrates the combined impact of gender and socio-economic status ("women and children first" + 1st Class privilege). |
| **Visual 3** | Faceted Categorical Bar Chart (`catplot`) | Reveals that Cherbourg (`C`) embarkation port passengers had higher survival rates due to a larger concentration of 1st Class tickets. |
| **Visual 4** | Stratified Boxplot Analysis | Shows that small family units (2–4 members) achieved higher survival rates compared to solo travelers or large families (>5). |
| **Visual 5** | Pairwise Correlation Heatmap | Quantifies key numerical relationships, confirming a strong negative correlation between `Pclass` and `Survived` (`-0.34`). |

---

## 📈 Key Implications & Takeaways

1. **Emergency Protocol Prioritization:** Structured evacuation rules heavily influence survival outcomes during crisis events.
2. **Socio-Economic Disparity:** Access to higher-tier resources (`Pclass 1` / High Fare) correlates directly with higher safety probabilities.
3. **Group Dynamics:** Moderate family size offers better operational efficiency during emergency evacuations compared to traveling alone or in large groups.

---

## 🚀 How to Run the Notebook

1. Open **Google Colab** ([colab.research.google.com](https://colab.research.google.com)).
2. Upload `Week-2:Advanced Data Visualization and Storytelling with Python.ipynb`.
3. Run all code cells (`Runtime` ➔ `Run all`).
4. The notebook will display all 5 graphs directly in the execution output and automatically download the compiled `.docx` and `.pdf` reports to your device.
