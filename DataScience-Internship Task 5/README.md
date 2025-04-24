🎯 Task 5 - Predicting Employee Attrition using Random Forest & SHAP Explainability
This project aims to predict whether an employee will leave the organization using machine learning, and to interpret model predictions using SHAP (SHapley Additive exPlanations).

📌 Objectives
Preprocess HR dataset for binary classification

Train a Random Forest model to predict employee attrition

Evaluate model performance using classification metrics

Visualize and explain feature importance using SHAP values

📂 Dataset
A structured HR dataset with various features like:

Age, JobSatisfaction, MonthlyIncome, DistanceFromHome, etc.

Attrition (target): Yes / No

⚙️ Technologies Used
Python

Pandas, NumPy

Scikit-learn

SHAP

Matplotlib / Seaborn (optional for visualization)

🧠 Model Summary
Model Used: RandomForestClassifier

Target Variable: Attrition (converted to binary: Yes → 1, No → 0)

Accuracy: ~87%

Class Imbalance Notice: Precision/Recall for class "1" (attrition) is low due to fewer positive samples.

📊 Classification Report
markdown
Copy
Edit
              precision    recall  f1-score   support

           0       0.88      1.00      0.93       255
           1       0.75      0.08      0.14        39

    accuracy                           0.87       294
   macro avg       0.81      0.54      0.54       294
weighted avg       0.86      0.87      0.83       294
🔍 SHAP Explainability
Used TreeExplainer to calculate SHAP values for the Random Forest model.

Generated a bar summary plot to show the most influential features driving predictions.

🔝 Top Influential Features:
OverTime

MonthlyIncome

Age

DistanceFromHome

JobSatisfaction

These features had the highest impact on attrition predictions.

📁 Files Included
employee_attrition_model.ipynb: Main Jupyter notebook with complete pipeline

Visualizations.

README.md: Project documentation

(Optional) requirements.txt: For replicating the environment

✅ Future Improvements
Handle class imbalance using SMOTE or class weights

Try other classifiers like XGBoost or Logistic Regression

Use SHAP dependency plots for deeper insights

Deploy as a Streamlit or Flask app for real-time predictions

