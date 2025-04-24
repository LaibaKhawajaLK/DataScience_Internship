🧠 Internship Data Science Project Guide

✅ Task 5: Predicting Employee Attrition
Objective: Predict if an employee is likely to leave the company.
Dataset: IBM HR Analytics Dataset (Kaggle)

🔸 Step-by-Step Workflow:
🔹 Step 1: Environment Setup
Install necessary libraries:
pip install pandas numpy matplotlib seaborn scikit-learn shap lime xgboost
🔹 Step 2: Load Dataset
import pandas as pd
df = pd.read_csv('WA_Fn-UseC_-HR-Employee-Attrition.csv')
df.head()
🔹 Step 3: EDA (Exploratory Data Analysis)
Check nulls, datatypes, summary

Visualize Attrition rates:

import seaborn as sns
import matplotlib.pyplot as plt

sns.countplot(data=df, x='Attrition')
plt.title('Attrition Distribution')
plt.show()
Explore relationships using:
sns.boxplot(data=df, x='Attrition', y='Age')
sns.boxplot(data=df, x='Attrition', y='MonthlyIncome')
🔹 Step 4: Preprocessing
Convert categorical variables

Encode target variable:
df['Attrition'] = df['Attrition'].map({'Yes': 1, 'No': 0})
df = pd.get_dummies(df, drop_first=True)
🔹 Step 5: Train-Test Split
from sklearn.model_selection import train_test_split

X = df.drop('Attrition', axis=1)
y = df['Attrition']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
🔹 Step 6: Train Classifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report

model = RandomForestClassifier()
model.fit(X_train, y_train)
y_pred = model.predict(X_test)

print(classification_report(y_test, y_pred))
🔹 Step 7: Explain Predictions (SHAP)
import shap
explainer = shap.TreeExplainer(model)
shap_values = explainer.shap_values(X_test)
shap.summary_plot(shap_values[1], X_test)
🔹 Step 8: Insights & Report
List top features affecting attrition

Suggest strategies (e.g., improve job satisfaction, reduce overtime)

🧾 Outcome:
Classification model to predict attrition

SHAP explanation plots

