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

### Phase 6 — Interactive Power BI Dashboard

**Status: Completed**

An interactive visual analytics dashboard was developed in Microsoft Power BI using the customer data, machine learning predictions, model-performance results, risk categories, and SHAP explanation outputs created during the previous phases.

The dashboard combines:

- Customer churn predictions
- Churn probabilities
- Actual churn outcomes
- Customer risk categories
- Global SHAP explanations
- Individual SHAP explanations
- Customer-segment comparisons
- Model-performance metrics
- Classification-threshold analysis

The final Power BI report contains six interactive dashboard pages.

#### Page 1 — Executive Overview

Provides a high-level summary of the customer churn prediction system.

Main components include:

- Total customers
- Actual churn customers
- Predicted churn customers
- Average churn probability
- Selected classification threshold
- Recall
- ROC-AUC
- F1-score
- Actual churn distribution
- Predicted churn distribution
- Churn-probability distribution
- Actual versus predicted counts
- Confusion matrix
- Key analytical insights

#### Page 2 — Customer Risk Analysis

Supports interactive customer-risk exploration and retention planning.

Main components include:

- Contract slicer
- Internet Service slicer
- Payment Method slicer
- Predicted Churn slicer
- Actual Churn slicer
- Risk Category slicer
- High-risk customer count
- Medium-risk customer count
- Low-risk customer count
- Highest churn probability
- Customer closest to the selected threshold
- Top high-risk customer ranking
- Risk-category distribution
- Tenure versus churn-probability analysis
- Detailed customer-risk table
- Analyst notes

#### Page 3 — Global Model Explanation

Explains the overall behaviour of the selected machine learning model using global SHAP results.

Main components include:

- Number of original features explained
- SHAP output scale
- SHAP base value
- Most influential global feature
- Second-most influential global feature
- Global SHAP feature-importance ranking
- Average direction of feature influence
- Top-ten global feature table
- Tenure–SHAP relationship
- Monthly Charges–SHAP relationship
- Global explanation insights

The global explanation showed that **Tenure** and **Contract** were the two most influential original customer features.

#### Page 4 — Individual Customer Explanation

Provides a detailed explanation for an individually selected customer.

Main components include:

- Customer-selection slicer
- Selected customer identifier
- Predicted churn probability
- Predicted churn classification
- Actual churn classification
- Selected classification threshold
- SHAP base value
- Original customer profile
- Customer-risk gauge
- Risk margin relative to the threshold
- Factors increasing churn risk
- Factors reducing churn risk
- Dynamically generated prediction explanation

The page updates automatically whenever another customer is selected.

#### Page 5 — Customer Segment Comparison

Supports comparison of churn risk across important customer segments.

Main components include:

- Contract slicer
- Internet Service slicer
- Payment Method slicer
- Senior Citizen slicer
- Paperless Billing slicer
- Highest-risk contract probability
- Highest-risk internet-service probability
- Highest-risk payment-method probability
- Senior-citizen average churn probability
- Average churn probability by contract
- Predicted churn rate by internet service
- Actual churn rate by payment method
- Average churn probability by senior-citizen status
- Average churn probability by paperless-billing status
- Segment summary matrix
- Overall segment interpretation

Important segment-level findings included:

- Month-to-month contracts had the highest average churn probability.
- Fibre-optic customers had the highest predicted churn rate.
- Electronic-check customers had the highest actual churn rate.
- Senior citizens had a higher average churn probability than non-senior customers.
- Customers using paperless billing had a higher average churn probability than customers without paperless billing.

These findings describe model patterns and associations and do not establish causation.

#### Page 6 — Model Performance Summary

Summarizes final model quality and the effect of classification-threshold selection.

Main components include:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Brier score
- Selected threshold
- Model ranking across performance metrics
- Default versus selected-threshold comparison
- False-negative reduction waterfall
- Threshold rationale
- Selected-model summary

The selected threshold of `0.27` improved recall and reduced the number of missed churn customers.

```text
Default threshold: 0.50
Selected threshold: 0.27

Default false negatives: 185
Selected false negatives: 72
Reduction: 113 customers
Percentage reduction: approximately 61.1%
