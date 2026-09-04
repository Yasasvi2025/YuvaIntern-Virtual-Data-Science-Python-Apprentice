# Week 5: Comprehensive Data Science Project Reporting & Strategic Recommendations

This repository contains the complete codebase, visual artifacts, and final executive report for **Week 5: Comprehensive Data Science Project Reporting and Strategic Recommendations**. Serving as the capstone deliverable of the internship, this project synthesizes exploratory data analysis, formal inferential hypothesis testing, and predictive machine learning modeling into a cohesive, production-grade technical report with actionable strategic recommendations.

---

## 📌 Project Overview

The primary objective of Week 5 is to consolidate all analytical findings from previous weeks using the **Titanic Passenger Dataset** to formulate evidence-based strategic insights for emergency resource allocation, risk management, and structural safety planning.

### Core Objectives

* **End-to-End Synthesis:** Unify exploratory data analysis, statistical hypothesis testing, and machine learning performance into a single analytical narrative.
* **Production Pipeline Design:** ImplementScikit-Learn `ColumnTransformer` pipelines for automated feature transformation, median/mode imputation, standard scaling, and one-hot encoding.
* **Model Evaluation & Benchmarking:** Benchmark Linear (Logistic Regression), Tree-Based (Decision Tree), and Ensemble (Random Forest) models across multiple metrics.
* **Strategic Decision Framework:** Translate quantitative data insights into actionable recommendations for crisis management and evacuation infrastructure.
* **Automated Document Generation:** Programmatically generate publication-ready `.docx` and `.pdf` reports complete with embedded diagnostic charts and summary tables.

---

## 🛠️ Tech Stack & Dependencies

* **Language:** Python 3.x
* **Environment:** Google Colab / Visual Studio Code
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning Pipeline:** `scikit-learn`
* **Visualization:** `matplotlib`, `seaborn`
* **Report Automation:** `python-docx`, `libreoffice` (for PDF conversion)

---

## 📁 Repository Structure

```text
├── Week-5: Comprehensive Data Science Project Reporting and Strategic Recommendations.ipynb
├── synthesis_eda.png
├── model_evaluation_summary.png
├── Week5_Comprehensive_Project_Report.docx
├── Week5_Comprehensive_Project_Report.pdf
└── README.md

```

---

## ⚙️ Analytical & Modeling Pipeline

```text
Raw Titanic Dataset (891 Passenger Records)
       │
       ▼
Exploratory Data Analysis & Inferential Hypothesis Testing
       │
       ▼
Stratified 80/20 Train-Test Split (Target: Survived)
       │
       ├───────────────────────────────┐
       ▼                               ▼
Numerical Pipeline              Categorical Pipeline
(Age, Fare, SibSp, Parch)       (Pclass, Sex, Embarked)
       │                               │
       ├─ Median Imputation            ├─ Most Frequent Imputation
       └─ Standard Scaling             └─ One-Hot Encoding
       │                               │
       └──────────────┬────────────────┘
                      │
                      ▼
            ColumnTransformer Pipeline
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
Logistic       Decision Tree   Random Forest
Regression      Classifier       Classifier
       │              │              │
       └──────────────┼──────────────┘
                      │
                      ▼
          Model Evaluation & Benchmarking
                      │
                      ▼
 Automated Report Generation (.docx & .pdf)

```

---

## 📈 Model Performance Benchmark

All candidate models were evaluated on an independent 20% stratified holdout test set (179 instances) to ensure class balance preservation (~38% survival rate).

| Model Algorithm | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| --- | --- | --- | --- | --- | --- |
| **Logistic Regression** | 0.8045 | 0.7705 | 0.6812 | 0.7231 | 0.8524 |
| **Decision Tree (max_depth=5)** | 0.8101 | 0.7931 | 0.6667 | 0.7244 | 0.8415 |
| **Random Forest (n_estimators=100)** | **0.8212** | **0.7846** | **0.7391** | **0.7612** | **0.8680** |

---

## 💡 Key Strategic Recommendations

1. **Equitable Egress Infrastructure:** Modify emergency exit and lifeboat access routes to prevent structural bottlenecks for passengers on lower decks, countering historical survival disparities linked to socio-economic status.
2. **Dynamic Risk-Assisted Evacuation Protocols:** Implement real-time passenger management systems that prioritize high-risk, vulnerable demographics during emergency response operations.
3. **Automated Safety Compliance Training:** Require standardized crisis drills and bias-mitigation training for emergency staff to ensure unbiased passenger assistance during maritime disasters.

---

## 🚀 How to Run the Notebook

1. **Clone the Repository:**
```bash
# Clone using standard HTTPS URL format
git clone https://github.com/Yasasvi2025/Week-5-Comprehensive-Data-Science-Project-Reporting-and-Strategic-Recommendations.git

# Navigate into the cloned directory
cd Week-5-Comprehensive-Data-Science-Project-Reporting-and-Strategic-Recommendations
```


2. **Open in Google Colab or Jupyter Notebook:**
Launch `Week-5: Comprehensive Data Science Project Reporting and Strategic Recommendations.ipynb`.
3. **Execute All Cells:**
The notebook will automatically:
* Install required system tools and packages (`python-docx`, `libreoffice`).
* Load the dataset and run the end-to-end processing pipeline.
* Display and save synthesized visual plots (`synthesis_eda.png`, `model_evaluation_summary.png`).
* Compile and download the comprehensive reports (`.docx` and `.pdf`).



---

## 👤 Author

* **Name:** Nune Venkata Yasasvi
* **Role:** Data Science / Frontend Development Intern
* **Environment:** Google Colab / Python 3
