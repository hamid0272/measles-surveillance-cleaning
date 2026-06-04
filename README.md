# measles-surveillance-cleaning
Machine learning models and data cleaning scripts for my thesis on measles surveillance.
Predictive Modeling of Measles Patient Mortality in Ethiopia
Overview
This repository contains the source code, data preprocessing pipelines, and machine learning models developed for my MSc thesis in Public Health Data Science. The project addresses the critical challenge of identifying high-risk measles patients in Ethiopia by integrating national surveillance data with health facility readiness indicators.

Problem Statement
Despite a robust national surveillance system, Ethiopia experienced a fivefold increase in confirmed measles cases between 2021 and 2023. Current clinical assessment methods struggle to predict mortality due to the complex interplay between patient-level characteristics and systemic health facility limitations.

Key Technical Approach
To address the extreme rarity of mortality events (0.59% prevalence), this study implemented:

Advanced Resampling: Applied Synthetic Minority Over-sampling Technique (SMOTE) to mitigate severe class imbalance.

Model Optimization: Trained and compared six supervised learning algorithms:

Ensemble Models: Random Forest (RF), XGBoost (XGB), Easy Ensemble (EE).

Deep Learning: Multi-Layer Perceptron (MLP) and 1D-Convolutional Neural Networks (CNN).

Interpretability: Used SHAP (SHapley Additive exPlanations) values to identify key predictors of patient mortality.

Evaluation: Utilized Bayesian optimization for hyperparameter tuning and assessed performance using PR-AUC and F1-score to account for the minority class.

Tech Stack
Language: Python

Data Analysis: Pandas, NumPy, Scikit-learn

Machine Learning: Imbalanced-learn (SMOTE), XGBoost, Keras/TensorFlow (for CNN/MLP)

Visualization: Matplotlib, Seaborn

Explainability: SHAP

Key Findings
Ensemble-based models, particularly Random Forest and XGBoost, achieved the highest discriminatory power in identifying high-risk mortality outcomes. Key predictors included case classification status, care-seeking intervals, and zonal-level health service coverage.

Project Structure
Plaintext
├── data/               # Preprocessed surveillance and SPA datasets
├── notebooks/          # Exploratory Data Analysis and Model Development
├── src/                # Modular scripts for feature engineering and training
├── models/             # Saved optimized model weights
