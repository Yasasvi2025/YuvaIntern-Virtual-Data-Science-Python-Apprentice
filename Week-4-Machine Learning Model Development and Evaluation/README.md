# Week 4: Machine Learning Model Development & Evaluation

This repository contains the complete codebase and technical evaluation for **Week 4: Machine Learning Model Development and Evaluation**. The project focuses on building, training, evaluating, and comparing supervised classification models using the **Titanic Passenger Dataset** to predict survival outcomes based on demographic, socio-economic, and structural features.

---

## 📌 Project Overview

The objective of this task is to apply fundamental machine learning principles to construct a robust, end-to-end binary classification pipeline in Python.

The pipeline performs data cleaning, median/mode imputation, scaling, one-hot encoding, model training across three distinct algorithmic paradigms, performance evaluation using multiple metrics, and visualization export.

### Core Objectives

* **Data Preprocessing & Leakage Prevention:** Utilize `ColumnTransformer` and Scikit-Learn `Pipeline` objects to ensure clean data transformations without train-test leakage.
* **Model Training:** Implement Linear (Logistic Regression), Tree-Based (Decision Tree), and Ensemble (Random Forest) classifiers.
* **Performance Evaluation:** Measure model behavior using Accuracy, Precision, Recall, F1-Score, and ROC-AUC.
* **Visual Diagnostics:** Generate comparative Confusion Matrices and ROC Curves.
* **Automated Reporting:** Export findings automatically into formatted `.docx` and `.pdf` reports via Python scripts.

---

## 🛠️ Tech Stack & Dependencies

* **Language:** Python 3.x
* **Environment:** Google Colab / Visual Studio Code
* **Data Processing:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Document Generation:** `python-docx`, `libreoffice` (for PDF conversion)

---

## 📁 Repository Structure

```text
├── Week-4: Machine Learning Model Development and Evaluation.ipynb
├── confusion_matrices.png
├── roc_curves.png
├── Week4_Machine_Learning_Report.docx
├── Week4_Machine_Learning_Report.pdf
└── README.md

```

---

## 📊 Preprocessing & Model Pipeline Workflow

```
Raw Data (Titanic Dataset)
       │
       ▼
Stratified Train-Test Split (80% Train / 20% Test)
       │
       ├───────────────────────────────┐
       ▼                               ▼
Numerical Features             Categorical Features
(Age, Fare, SibSp, Parch)      (Pclass, Sex, Embarked)
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

```

---

## 📈 Model Performance & Evaluation Metrics

All models were evaluated on an independent 20% holdout test dataset (179 instances) using stratified splitting to preserve class balance (~38% survival rate).

| Model Algorithm | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| --- | --- | --- | --- | --- | --- |
| **Logistic Regression** | 0.8045 | 0.7705 | 0.6812 | 0.7231 | 0.8524 |
| **Decision Tree (max_depth=5)** | 0.8101 | 0.7931 | 0.6667 | 0.7244 | 0.8415 |
| **Random Forest (n_estimators=100)** | **0.8212** | **0.7846** | **0.7391** | **0.7612** | **0.8680** |

---

## 🔍 Key Findings & Visualizations

### 1. Confusion Matrix Comparison

* **Logistic Regression & Decision Trees** exhibited higher false negative rates, missing a larger portion of actual survivors.
* **Random Forest** achieved the highest true positive rate (Recall: 0.7391), making it the most balanced model for identifying survivors.

### 2. Receiver Operating Characteristic (ROC) Curves

* **Random Forest** achieved the highest area under the curve (**ROC-AUC = 0.868**), demonstrating superior class separation capabilities across varying decision thresholds.

---

## ⚠️ Critical Discussion & Sources of Error

1. **Class Imbalance Impact:** Survival outcomes in the dataset are moderately imbalanced (~38% survived vs. ~62% died). Relying solely on accuracy can be misleading; F1-Score and ROC-AUC provided a more reliable measure of performance.
2. **Imputation Assumptions:** Missing continuous values (e.g., `Age`) were imputed using the median. While robust to outliers, this assumes missingness at random, which may introduce minor variance distortion.
3. **Overfitting Risks:** Individual decision trees with unconstrained depth tend to memorize noise. Constraining `max_depth` or using ensemble methods like Random Forest effectively controlled model variance.

---

## 🚀 How to Run the Notebook

1. **Clone the Repository:**
```bash
# Clone using standard HTTPS URL format (spaces replaced with %20)
git clone https://github.com/Yasasvi2025/Week-4-Machine%20Learning%20Model%20Development%20and%20Evaluation.git

# Navigate into the cloned directory (quoted to handle spaces)
cd "Week-4-Machine Learning Model Development and Evaluation"
```


2. **Open in Google Colab or Jupyter Notebook:**
Launch `Week-4: Machine Learning Model Development and Evaluation.ipynb`.
3. **Execute All Cells:**
The notebook will automatically:
* Install required dependencies (`python-docx`, `libreoffice`).
* Download the Titanic dataset.
* Run the data pipeline and model training scripts.
* Output inline performance charts (`confusion_matrices.png`, `roc_curves.png`).
* Generate and download the technical report files (`.docx` and `.pdf`).



---

## 👤 Author

* **Name:** Nune Venkata Yasasvi
* **Role:** Data Science / Frontend Development Intern
* **Environment:** Google Colab / Python 3
