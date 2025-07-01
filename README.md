# Survival_Analysis
"""
# Survival Analysis on Pan-Cancer Dataset

**Author:** Ashutosh Anand  
**Email:** [ashutoshanand3007@gmail.com](mailto:ashutoshanand3007@gmail.com)  
**Date:** August 4, 2022  

---

## 📘 Project Description

This project conducts **Survival Analysis** on a Pan-Cancer dataset using Python's `lifelines` library. The objective is to understand patient survival behavior based on variables such as **age**, **gender**, **race**, **tumor stage**, **treatment outcomes**, and **cancer type**. Kaplan-Meier estimators are used to compute survival probabilities and stratified insights.

---

## 🔬 What is Survival Analysis?

Survival Analysis is a statistical method for analyzing the expected duration of time until an event of interest occurs (e.g., death, relapse). It handles **censored data** — cases where the final event status is unknown.

- **Right-Censoring:** Individual survived longer than the study duration.
- **Left-Censoring:** Event occurred before the start of the observation window.

---

## 📊 Dataset Description

The dataset contains 10 variables:

| Column              | Description                                                 |
|---------------------|-------------------------------------------------------------|
| `bcr_patient_barcode` | Unique patient identifier                                 |
| `type`               | Type of cancer (e.g., MESO, PRAD)                          |
| `age`                | Age of patient in years                                    |
| `gender`             | Gender (Male/Female)                                       |
| `race`               | Race category (e.g., Asian, White, Black)                  |
| `tumor_stage`        | Tumor stage (e.g., Stage I, II, III, IV, X, IS)            |
| `vital_status`       | Alive or Dead                                              |
| `treatment_outcome`  | Treatment result (e.g., Complete Remission, Stable Disease)|
| `event`              | Event status (1 = event occurred, 0 = censored)            |
| `delay`              | Survival time in days                                      |

---

## 📈 Key Analyses & Findings

### 🧪 1. Overall Survival Curve
- Kaplan-Meier estimator shows the **median survival time is 2240 days**.
- Confidence Interval: **[2097, 2417] days**.

### 🚻 2. Gender-wise Survival
- **Females** have a higher survival probability than males.
- Mean event rate (death probability) is higher in males.

### 📅 3. Age-wise Survival
- Patients **aged < 25** have the highest survival probability.
- Survival drops gradually with increasing age brackets (25–50, 50–75, 75–100).

### 🌍 4. Race-wise Survival
- **Asian** patients show better survival than other racial groups.
- Confidence interval overlap suggests some group differences may not be statistically significant.

### 🩸 5. Tumor Stage Impact
- Patients at **Stage X** are at the highest risk.
- Lower stages (IS, I, II) have better outcomes.

### 🧬 6. Cancer Type
- **MESO** (Mesothelioma) shows higher mortality.
- **PRAD** (Prostate Adenocarcinoma) appears benign with lower mortality.

### 🔗 7. Correlation Analysis
- `treatment_outcome` and `event` have a **strong positive correlation**.
- `age` and `delay` are **negatively correlated**, suggesting older patients tend to have shorter survival times.

---

## 🛠 Tools & Libraries Used

- Python 3.x
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `lifelines` (for Kaplan-Meier survival analysis)
- Jupyter Notebook

---
