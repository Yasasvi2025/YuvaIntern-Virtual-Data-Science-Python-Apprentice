# Week 3: Statistical Analysis and Hypothesis Testing in Python

**Author:** Nune Venkata Yasasvi  
**Role:** Data Science Intern  
**Dataset:** Titanic Survival Dataset (891 records)  
**Environment:** Google Colab / Python 3  

---

## 📌 Project Overview
This repository contains the complete codebase and technical report for **Week 3: Statistical Analysis and Hypothesis Testing in Python**. The primary objective of this project is to apply formal inferential statistical methods to validate or refute empirical hypotheses regarding demographic prioritization, socio-economic factors, and passenger survival outcomes.

The analysis evaluates three distinct statistical hypotheses covering parametric continuous comparisons, non-parametric categorical independence, and multi-group variance evaluations.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3
* **Data Handling:** `pandas`, `numpy`
* **Statistical Computing:** `scipy.stats`, `statsmodels`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Automated Document Generation:** `python-docx`, `libreoffice`

---

## 📁 Repository Deliverables
```text
├── Week3_Statistical_Analysis.ipynb          # Executable Google Colab Notebook
├── Week3_Statistical_Analysis_Report.docx     # Complete Word Document Report
├── Week3_Statistical_Analysis_Report.pdf      # Converted PDF Report Deliverable
└── README.md                                 # Repository Documentation

```

---

## 🧪 Statistical Hypotheses & Summary Results

| Hypothesis ID | Target Variables | Statistical Test | Test Statistic | p-value | Significance ($\alpha=0.05$) | Decision |
| --- | --- | --- | --- | --- | --- | --- |
| **H1: Fare vs. Survival** | Continuous (`Fare`) vs. Binary (`Survived`) | **Welch's Two-Sample t-Test** | $t = 6.8390$ | $p = 1.07 \times 10^{-11}$ | $p < 0.05$ | **Reject $H_0$** |
| **H2: Class vs. Survival** | Categorical (`Pclass`) vs. Categorical (`Survived`) | **Chi-Square ($\chi^2$) Test of Independence** | $\chi^2 = 102.8887$ | $p = 4.55 \times 10^{-23}$ | $p < 0.05$ | **Reject $H_0$** |
| **H3: Age vs. Embarkation** | Continuous (`Age`) vs. Multi-Group (`Embarked`) | **One-Way ANOVA** | $F = 4.7405$ | $p = 0.0089$ | $p < 0.05$ | **Reject $H_0$** |

---

## 📊 Detailed Test Breakdown & Key Insights

### 1. Hypothesis 1: Mean Fare Differential (Welch's t-Test)

* **Null Hypothesis ($H_0$):** $\mu_{\text{survived}} = \mu_{\text{non-survived}}$ (No mean fare difference).
* **Alternative Hypothesis ($H_1$):** $\mu_{\text{survived}} > \mu_{\text{non-survived}}$ (Survivors paid a higher mean fare).
* **Key Finding:** Survivors paid a significantly higher mean fare ($\$48.40$) compared to non-survivors ($\$22.12$).

### 2. Hypothesis 2: Class & Survival Dependency (Chi-Square & Cramér's V)

* **Null Hypothesis ($H_0$):** Ticket class and survival status are independent.
* **Alternative Hypothesis ($H_1$):** Ticket class and survival status are dependent.
* **Key Finding:** A statistically significant association exists ($\text{Cramér's V} \approx 0.34$), confirming that First-Class passengers had substantially higher survival rates ($62.9\%$) than Third-Class passengers ($24.2\%$).

### 3. Hypothesis 3: Passenger Age Across Embarkation Ports (One-Way ANOVA)

* **Null Hypothesis ($H_0$):** $\mu_{\text{Cherbourg}} = \mu_{\text{Queenstown}} = \mu_{\text{Southampton}}$
* **Alternative Hypothesis ($H_1$):** At least one embarkation port has a different mean passenger age.
* **Key Finding:** Passengers embarking from Cherbourg recorded a higher mean age ($\approx 30.8$ years) compared to Queenstown ($\approx 28.0$ years) and Southampton ($\approx 29.4$ years).

---

## 📈 Real-World Implications

1. **Financial Privilege & Safety Allocation:** Ticket fare serves as a strong continuous predictor of crisis survival probability.
2. **Structural Prioritization:** Access to premium accommodation directly influenced emergency evacuation access.
3. **Demographic Stratification:** Geographic port origin correlates with distinct passenger demographic profiles.

---

## 🚀 How to Run the Notebook

1. Open **Google Colab** ([colab.research.google.com](https://colab.research.google.com)).
2. Upload `Week-3: Statistical Analysis and Hypothesis Testing in Python.ipynb`.
3. Select **Runtime ➔ Run all**.
4. The notebook will execute the calculations, display all figures in-line, and download `Week3_Statistical_Analysis_Report.docx` and `Week3_Statistical_Analysis_Report.pdf`.
