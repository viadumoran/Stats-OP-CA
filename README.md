# Predicting Hospital Readmission in Diabetic Patients
Via Paola Dumoran - MSc Data Analytics, National College of Ireland
## Project Overview
This project analyzes hospital readmissions of diabetic patients using logistic regression modeling. The goal is to identify key clinical and demographic factors associated with increased risk of readmission and propose actionable insights to reduce future readmission rates.

## Key Findings
- Longer hospital stays and higher numbers of medications are associated with increased readmission risk.
- Poor diabetes management, especially absence of HbA1c testing, significantly increases readmission risk.
- Interaction between primary diagnosis (e.g., diabetes, respiratory diseases) and HbA1c testing results affects readmission likelihood.

## Data
- Dataset originally published by Strack et al. (2014).
- Includes ~100,000 hospital records with 47 variables (demographic, medical history, admission details, etc.).
- Preprocessing steps included:
  - Data cleaning (handling missing values, removing irrelevant columns).
  - Variable transformation (e.g., grouping HbA1c results, simplifying diagnoses).
  - Outlier removal (using IQR method).
  - Conversion of the readmission variable into a binary classification.

## Methodology
- **Exploratory Data Analysis (EDA)**:
  - Visualization of race, gender, age distribution, admission sources, and HbA1c testing patterns.
- **Feature Engineering**:
  - Created grouped variables like `A1C_Grouped` and `primary_diagnosis`.
  - Applied log transformations and polynomial terms for numeric predictors.
- **Modeling**:
  - Built logistic regression models.
  - Included interaction terms (e.g., HbA1c testing status * primary diagnosis).
  - Final model achieved improved deviance reduction and lower AIC.

## Tools Used
- R Programming Language
- Libraries: `ggplot2`, `dplyr`, `stats`, `car`, `caret`
