# Cardiovascular Disease Risk Analysis – Research Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-XGBoost-orange.svg)
![Data Analysis](https://img.shields.io/badge/Analysis-EDA-green.svg)
![XAI](https://img.shields.io/badge/XAI-SHAP-yellow.svg)

## Project Overview
This project was developed as part of an **Engineering Thesis**. It focuses on building a robust classification model to predict the risk of cardiovascular diseases based on clinical data and lifestyle factors.

The project goes beyond simple prediction by implementing **Explainable AI (XAI)** techniques. This ensures that the model's decisions are transparent and can be interpreted in a clinical context, identifying which specific health parameters contribute most to a patient's risk.

---

## Tech Stack
* **Language:** Python
* **Data Manipulation:** `Pandas`, `NumPy`
* **Statistical Analysis:** `SciPy`, `Statsmodels` (Chi-square tests, Pearson correlation)
* **Visualization:** `Seaborn`, `Matplotlib`
* **Machine Learning:** `XGBoost`, `Scikit-learn`
* **Interpretability:** `SHAP` (Shapley Additive Explanations)

---

## Analysis Workflow

### 1. Data Cleaning & Preprocessing
* **Feature Engineering:** Converted age from days to years and engineered the **BMI (Body Mass Index)** feature.
* **Integrity Checks:** Removed records with medical inconsistencies (e.g., cases where diastolic pressure exceeded systolic pressure).
* **Outlier Removal:** Applied statistical filtering to handle anomalous values in height, weight, and blood pressure.

### 2. Exploratory Data Analysis (EDA)
* Analyzed feature distributions and identified patterns related to cardiovascular risk.
* Performed **Chi-square tests** to validate the statistical significance of categorical features.
* Conducted correlation analysis to understand the relationships between lifestyle choices and health outcomes.

### 3. Modeling & Interpretability (XAI)
The primary model used is an **XGBoost Classifier**. To ensure clinical reliability, I utilized **SHAP values** to:
* **Identify Global Importance:** Found that **Systolic Blood Pressure (ap_hi)**, **Age**, and **Glucose levels** are the most significant predictors.
* **Validate with Medical Knowledge:** Confirmed that the model's behavior aligns with established cardiovascular risk factors.

---

## Key Results
* **Primary Drivers:** High systolic blood pressure and advanced age were the strongest indicators of risk.
* **Lifestyle Impact:** Factors like smoking, alcohol consumption, and physical activity levels were analyzed for their relative impact on heart health.
* **Diagnostic Support:** The model serves as a proof-of-concept for automated screening tools in early cardiovascular diagnostics.

---

## Repository Structure
* `inzynierka (2).ipynb` – Full Jupyter Notebook with data processing, EDA, and model training.
* `cardio_train.csv` – The dataset used for training (Source: Kaggle).
* `processed_data.csv` – The refined dataset used for final analysis.

---
