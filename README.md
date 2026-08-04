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

The final processed datasets contained:

- Training records: 5,625
- Testing records: 1,407
- Processed features: 45

### Phase 4 — Machine Learning Model Development

**Status: Completed**

Several machine learning models were trained, evaluated, tuned, and compared.

The final selected model was a **Tuned Gradient Boosting Classifier**.

- Prediction threshold: 0.27
- Test churn recall: 80.75%
- Test F1-score: 61.44%
- Test ROC-AUC: 83.83%
- Test Precision-Recall AUC: 65.20%
- Correctly identified churn customers: 302 out of 374

### Phase 5 — Explainable Artificial Intelligence with SHAP

**Status: Completed**

SHAP TreeExplainer was used to explain the customer churn predictions produced by the selected Gradient Boosting model.

The explanations were calculated directly on the churn-probability scale for all customers in the independent test dataset.

The main Phase 5 results were:

- Customers explained: 1,407
- Processed model features explained: 45
- Grouped original features: 19
- Processed long-format rows: 63,315
- Grouped long-format rows: 26,733
- SHAP output scale: Probability
- SHAP additivity passed for all 1,407 customers
- Final validation failures: 0

The strongest globally important original features were:

- Tenure
- Contract
- Internet Service
- Online Security
- Technical Support
- Payment Method
- Monthly Charges

The Phase 5 outputs include:

- Global SHAP feature importance
- Customer-level SHAP contributions
- Top positive churn factors
- Top negative churn factors
- Original customer feature values
- Actual and predicted churn status
- Churn probabilities
- Contribution direction and ranking
- SHAP additivity validation
- Global and local SHAP visualizations
- Power BI-ready long-format files

### Phase 6 — Interactive Power BI Dashboard

**Status: Next Phase**

The customer predictions and SHAP explanation outputs will be imported into Power BI.

The planned dashboard will include:

- Executive Overview
- Customer Risk Analysis
- Global Model Explanation
- Individual Customer Explanation
- Customer Segment Comparison
- Model Performance Summary

### Phase 7 — User Evaluation

**Status: Planned**

The interactive Power BI dashboard will be compared with a static explanation system.

The evaluation will examine:

- Interpretation accuracy
- Task-completion time
- User confidence
- Trust
- Decision quality

### Phase 8 — Final Thesis Writing and Submission

**Status: Planned**

The technical results, dashboard, evaluation findings, final thesis chapters, and presentation will be completed.

---

## GitHub Repository Structure

```text
Documentation/
├── Phase 1 Research Foundation and Planning.pdf
├── Phase 2 Dataset Selection and Exploratory Data Analysis.pdf
├── Phase 3 Data Preprocessing.pdf
├── Phase 4 Machine Learning Model Development.pdf
└── Phase 5 Explainable Artificial Intelligence with SHAP.pdf

notebooks/
├── 01_eda.ipynb
├── 02_preprocessing.ipynb
├── 03_model_training.ipynb
└── 04_shap_analysis.ipynb

outputs/
├── Phase_3_Preprocessing_Outputs.zip
├── Phase_4_Model_Development_Outputs.zip
└── Phase_5_SHAP_Outputs.zip

data/
└── IBM Telco Customer Churn Dataset

powerbi/
└── Power BI dashboard files

evaluation/
└── User evaluation materials
```

---

## Phase 5 Output Archive

The file `Phase_5_SHAP_Outputs.zip` contains the complete Explainable Artificial Intelligence outputs created during Phase 5.

The ZIP archive contains 28 files, including:

- Global processed-feature SHAP importance
- Global grouped-feature SHAP importance
- Processed-feature SHAP values
- Grouped original-feature SHAP values
- Power BI-ready long-format files
- Wide-format SHAP files
- Customer-level explanation summaries
- Top positive customer factors
- Top negative customer factors
- Combined customer-factor outputs
- SHAP feature mapping
- SHAP additivity validation
- Final Phase 5 validation results
- SHAP metadata
- Global SHAP bar plots
- SHAP beeswarm visualization
- Numerical feature relationship plots
- Local customer waterfall explanations

All final Phase 5 validation checks passed successfully.

---

## Main Phase 5 Output Files

### `shap_values_grouped_long.csv`

The main Power BI-ready explanation table containing one row for each customer and each original feature.

### `customer_prediction_explanations.csv`

Combines original customer information, churn predictions, churn probabilities, and the strongest SHAP explanations.

### `customer_top_factors_combined.csv`

Contains the strongest positive and negative churn factors for each customer.

### `global_shap_importance_grouped.csv`

Contains the global importance ranking of the 19 original customer features.

### `shap_additivity_validation.csv`

Confirms that the SHAP base value and feature contributions reconstruct the model output.

### `phase5_validation_summary.csv`

Records the final Phase 5 validation checks and confirms that all checks passed.

### `shap_metadata.json`

Stores the SHAP configuration, explainer type, probability scale, dataset sizes, feature counts, validation results, and output information.

---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- SHAP
- Matplotlib
- Joblib
- Google Colab
- Microsoft Power BI
- GitHub

---

## Current Status

Phases 1, 2, 3, 4, and 5 are completed.

The machine learning prediction model and SHAP explainability outputs are complete and validated.

The next step is **Phase 6 — Interactive Power BI Dashboard Development**.
