# Master’s Thesis Repository

## Design and Evaluation of an Interactive Visual Analytics System for Explainable Artificial Intelligence

**Author:** Reeve Nilesh Gonsalves  
**Program:** M.Sc. Applied Data Science & Analytics  
**University:** SRH Hochschule Heidelberg  

**Supervisor:** Prof. Dr. Mehrdad Jalali  
**Secondary Supervisor:** Prof. Dr.-Ing. Binh Vu  

---

## Project Overview

This repository contains the documentation, notebooks, machine learning work, Explainable AI outputs, and Power BI dashboard components developed for my Master’s thesis.

The project combines machine learning, SHAP explainability, and interactive Power BI visualization to make AI predictions easier to understand.

---

## Project Pipeline

```text
Dataset
→ Exploratory Data Analysis
→ Data Preprocessing
→ Machine Learning Model
→ SHAP Explainability
→ Power BI Dashboard
→ User Evaluation
→ Final Thesis
```

---

## Dataset

The project uses the **IBM Telco Customer Churn Dataset**.

- Original records: 7,043
- Cleaned records: 7,032
- Target variable: Churn
- Prediction task: Churn or Non-Churn

---

## Project Phases

### Phase 1 — Research Foundation and Planning

**Status: Completed**

The thesis topic, research questions, project scope, system concept, and evaluation strategy were defined.

### Phase 2 — Dataset Selection and Exploratory Data Analysis

**Status: Completed**

The dataset was selected, cleaned, explored, and analyzed to understand customer churn patterns.

### Phase 3 — Data Preprocessing

**Status: Completed**

The target variable was encoded, categorical features were transformed, numerical features were standardized, and the training and testing datasets were created.

### Phase 4 — Machine Learning Model Development

**Status: Completed**

Several machine learning models were trained and compared.

The final selected model was a **Tuned Gradient Boosting Classifier**.

- Prediction threshold: 0.27
- Test churn recall: 80.75%
- Test ROC-AUC: 83.83%

### Phase 5 — Explainable AI with SHAP

**Status: Next Phase**

SHAP will be used to explain the global model behavior and individual customer churn predictions.

### Phase 6 — Interactive Power BI Dashboard

**Status: Planned**

The prediction and SHAP outputs will be visualized through an interactive Power BI dashboard.

### Phase 7 — User Evaluation

**Status: Planned**

The interactive Power BI dashboard will be compared with a static explanation system.

### Phase 8 — Final Thesis Writing and Submission

**Status: Planned**

The technical results, dashboard, evaluation findings, and final thesis chapters will be completed.

---

## Repository Structure

```text
Documentation/
├── Phase 1 Progress Documentation
├── Phase 2 Progress Documentation
├── Phase 3 Progress Documentation
└── Phase 4 Progress Documentation

notebooks/
├── 01_eda.ipynb
├── 02_preprocessing.ipynb
└── 03_model_training.ipynb

data/
└── IBM Telco Customer Churn Dataset

powerbi/
└── Power BI dashboard files

evaluation/
└── User evaluation materials
```

---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- SHAP
- Google Colab
- Microsoft Power BI
- GitHub

---

## Current Status

Phases 1, 2, 3, and 4 are completed.

The next step is **Phase 5 — Explainable Artificial Intelligence with SHAP**.
