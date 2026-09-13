# Master’s Thesis Repository

## Design and Evaluation of an Interactive Visual Analytics System for Explainable Artificial Intelligence

**Author:** Reeve Nilesh Gonsalves  
**Program:** M.Sc. Applied Data Science & Analytics  
**University:** SRH Hochschule Heidelberg  

**Supervisor:** Prof. Dr.-Ing. Mehrdad Jalali  
**Secondary Supervisor:** Prof. Dr.-Ing. Binh Vu  

---

## Project Overview

This repository contains the complete implementation and documentation of my Master’s thesis.

The project investigates how machine learning predictions can be made more understandable and useful for non-technical users by combining **Machine Learning, SHAP Explainable AI, Interactive Visual Analytics, Microsoft Power BI, and User Evaluation**.

Customer churn prediction is used as the application case.

The main contribution of the thesis is the complete workflow from prediction to explanation and interactive business-oriented visual analytics, followed by a user evaluation comparing interactive and static explanations.

---

## Project Pipeline

```text
Dataset
→ Exploratory Data Analysis
→ Data Preprocessing
→ Machine Learning Model Development
→ SHAP Explainability
→ Power BI Visual Analytics
→ User Evaluation
→ Final Thesis
```

---

## Dataset

The project uses the **IBM Telco Customer Churn Dataset**, accessed through Kaggle.

- Original customers: **7,043**
- Cleaned customers: **7,032**
- Training customers: **5,625**
- Testing customers: **1,407**
- Original model features: **19**
- Processed model features: **45**
- Target variable: **Churn**

---

## Project Phases

### Phase 1 — Research Foundation and Planning

**Status: Completed**

Defined the research problem, objectives, research questions, project scope, methodology, system concept, and evaluation strategy.

### Phase 2 — Dataset Selection and Exploratory Data Analysis

**Status: Completed**

Selected and explored the Telco Customer Churn dataset.

Main work included:

- Dataset structure analysis
- Missing-value analysis
- Churn distribution
- Contract and tenure analysis
- Service and payment analysis
- Monthly and total charge analysis
- Correlation analysis
- Outlier investigation

### Phase 3 — Data Preprocessing

**Status: Completed**

Prepared the dataset for machine learning.

Main outputs:

- Cleaned dataset: **7,032 customers**
- Training dataset: **5,625 customers**
- Testing dataset: **1,407 customers**
- Original model features: **19**
- Processed model features: **45**

The preprocessing included numerical standardisation, one-hot encoding, target encoding, stratified train-test splitting, and preservation of `customerID` for later explanation and dashboard analysis.

### Phase 4 — Machine Learning Model Development

**Status: Completed**

Five classification models were compared:

- Logistic Regression
- Weighted Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting

The final selected model was a **Tuned Gradient Boosting Classifier**.

Main final test results at threshold `0.27`:

- Accuracy: **73.06%**
- Precision: **49.59%**
- Recall: **80.75%**
- F1-score: **0.6144**
- ROC-AUC: **0.8383**
- PR-AUC: **0.6520**
- Correctly identified churn customers: **302 of 374**

The classification threshold was reduced from `0.50` to `0.27` to identify more actual churn customers.

```text
Missed churn customers at 0.50: 185
Missed churn customers at 0.27: 72
Reduction: 113 customers
```

### Phase 5 — Explainable Artificial Intelligence with SHAP

**Status: Completed**

SHAP TreeExplainer was used to explain the final Gradient Boosting model.

Main outputs:

- Customers explained: **1,407**
- Processed model features: **45**
- Grouped original features: **19**
- Processed SHAP records: **63,315**
- Grouped SHAP records: **26,733**

The 45 technical model features were mapped back into the 19 original customer variables to improve business interpretation.

The strongest global features included:

- Tenure
- Contract
- Internet Service
- Online Security
- Technical Support
- Payment Method
- Monthly Charges

Both **global** and **individual customer explanations** were generated.

### Phase 6 — Interactive Power BI Visual Analytics System

**Status: Completed**

The machine learning predictions, customer information, SHAP explanations, risk categories, and model-performance results were imported into Microsoft Power BI.

The final system contains six interactive pages:

1. **Executive Overview**
2. **Customer Risk Analysis**
3. **Global Model Explanation**
4. **Individual Customer Explanation**
5. **Customer Segment Comparison**
6. **Model Performance Summary**

The dashboard allows users to move from overall model behaviour to customer segments and finally to detailed explanations for individual customers.

### Phase 7 — User Evaluation

**Status: Completed**

The interactive Power BI system was compared with a static explanation baseline using **10 participants**.

Main results:

```text
Static task accuracy:       70.83%
Interactive task accuracy:  91.67%

Static overall rating:       3.53 / 5
Interactive overall rating:  4.45 / 5

Static mean completion time:       6 min 56 sec
Interactive mean completion time:  6 min 48 sec
```

**8 out of 10 participants preferred the interactive system.**

The evaluation showed higher task accuracy and stronger ratings for understanding, factor identification, decision support, trust, ease of use, and perceived usefulness with the interactive dashboard.

### Phase 8 — Final Thesis

**Status: Completed**

The final thesis documents the complete research process, technical implementation, results, discussion, limitations, research contribution, and user evaluation.

The final report is available in the `Documentation` folder.

---

## Main Research Contribution

The thesis does not claim a new machine learning algorithm or a new SHAP algorithm.

The main contribution is the integration of:

```text
Machine Learning
+ SHAP Explainability
+ Business-Level Feature Transformation
+ Interactive Power BI Analytics
+ User Evaluation
```

The project transforms technical machine learning and SHAP outputs into an interactive visual analytics system for non-technical users.

The system supports explanation at:

- Global model level
- Customer-segment level
- Individual customer level
- Model-performance level

The interactive system was then evaluated against a static explanation baseline.

---

## Repository Structure

```text
Documentation/
├── Phase 1 Research Foundation and Planning
├── Phase 2 Dataset Selection and Exploratory Data Analysis
├── Phase 3 Data Preprocessing
├── Phase 4 Machine Learning Model Development
├── Phase 5 Explainable Artificial Intelligence with SHAP
├── Phase 6 Interactive Visual Analytics Dashboard
├── Phase 7 User Evaluation Documentation
└── Reeve_Thesis_Report.pdf

data/
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── cleaned_telco_churn.csv
└── Phase_6_PowerBI_Import.zip

notebooks/
├── 01_eda.ipynb
├── 02_preprocessing.ipynb
├── 03_model_training.ipynb
└── 04_shap_analysis.ipynb

powerbi/
├── Executive Overview.png
├── Customer Risk Analysis.png
├── Global Model Explanation.png
├── Individual Customer Explanation.png
├── Customer Segment Comparison.png
├── Model Performance Summary.png
└── Power BI project file

src/
├── Phase_3_Preprocessing_Outputs.zip
├── Phase_4_Model_Development_Outputs.zip
├── Phase_5_SHAP_Outputs.zip
└── Phase_6_PowerBI_Import.zip
```

---

## Main Notebooks

### `01_eda.ipynb`

Exploratory Data Analysis of the Telco Customer Churn dataset.

### `02_preprocessing.ipynb`

Data cleaning, feature transformation, encoding, scaling, and train-test preparation.

### `03_model_training.ipynb`

Model comparison, tuning, threshold selection, and final model evaluation.

### `04_shap_analysis.ipynb`

Global and individual SHAP explanation generation and preparation of Power BI-ready outputs.

---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- SHAP
- Matplotlib
- Seaborn
- Joblib
- Google Colab
- Microsoft Power BI
- GitHub

---

## Final Status

**All thesis phases are completed.**

The repository contains the complete workflow from the original dataset through exploratory analysis, preprocessing, machine learning, SHAP explainability, Power BI visual analytics, user evaluation, and the final Master’s thesis report.
