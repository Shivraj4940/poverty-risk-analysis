# Out-of-Pocket Healthcare Costs and Poverty Risk Analysis

This repository contains an end-to-end data science and statistical computing project investigating how out-of-pocket healthcare expenses (OOPE) drive households into financial vulnerability across Kolhapur City. 

The project spans primary data engineering, advanced inferential modeling, machine learning optimization, and production deployment.

## 📁 Repository Structure

* **`1_Data_Prep_and_Cleaning/`**
    * `Hospital_Row_Data.csv`: Raw bilingual survey questionnaire dataset (300 samples).
    * `Data Cleaning.ipynb`: Programmatic Python pipeline for data filtering, bilingual string normalization, and midpoint conversions.
    * `Healthcare_Data_Cleaning_Process_Report.pdf`: Formal documentation detailing engineering steps and imputation strategies.
* **`2_Analysis_and_Modeling/`**
    * `Hospital num data.xlsx - Sheet1.csv`: Standardized, fully engineered analytical matrix.
    * `Hospital Analysis.ipynb`: Inferential code running Ridge Regression, Factorial ANOVA/MANOVA, and Chi-Square tests.
    * `Healthcare_Expenditure_and_Poverty_Analysis_Report.pdf`: Academic-grade paper evaluating socio-economic stratification and health-burden indices.
* **`3_Machine_Learning_and_Deployment/`**
    * `ML Model.ipynb`: Script training, validating, and testing multiple classifiers while diagnosing overfitting boundaries.
    * `app.py`: Production code for the interactive user-facing web dashboard.
    * `poverty_model.pkl` & `scaler.pkl`: Serialized model weights and scaling parameters exported via `joblib`.
    * `requirements.txt`: Package dependency matrix for remote cloud hosting environment replication.

## 🚀 Key Technical Highlights
* **Overfitting Safeguards:** Evaluated 5 baseline models; identified and isolated an over-fitted Decision Tree (13.33% variance gap) to narrow down choices to the top three models.
* **Ensemble Optimization:** Built a robust **Soft-Voting Ensemble Classifier** (combining Random Forest, SVC, and Logistic Regression) achieving **96.67% holdout test accuracy** with minimal variance ($0.42\%$).
* **Production Deployment:** Serialized model artifacts to launch a reactive cloud-hosted **Streamlit Web Application** for real-time household poverty risk evaluation.
