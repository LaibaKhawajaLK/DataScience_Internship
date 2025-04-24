Diabetes Prediction using Gradient Boosting Classifier
Overview
This project involves building a machine learning model to predict the presence of diabetes based on various health parameters. The model uses the Gradient Boosting Classifier to perform classification and predict whether a patient has diabetes or not, using a dataset of health metrics.

Dataset
The dataset used in this project is the Pima Indians Diabetes Database, which contains medical data for female patients of Pima Indian heritage. The dataset contains the following features:

Pregnancies: Number of times pregnant

Glucose: Plasma glucose concentration after 2 hours in an oral glucose tolerance test

Blood Pressure: Diastolic blood pressure (mm Hg)

Skin Thickness: Triceps skinfold thickness (mm)

Insulin: 2-Hour serum insulin (mu U/ml)

BMI: Body mass index (weight in kg/(height in m)^2)

Diabetes Pedigree Function: A function which scores the likelihood of diabetes based on family history

Age: Age (years)

Outcome: Whether the patient has diabetes (1) or not (0) [Target Variable]

The task is to predict the Outcome (1: diabetic, 0: not diabetic) based on the other features.

Project Steps
1. Dataset Loading and Preprocessing
The dataset is loaded into a pandas DataFrame from a CSV file. The features are separated from the target variable (Outcome), and the features are then scaled using StandardScaler to normalize the values for better model performance.


import pandas as pd
from sklearn.preprocessing import StandardScaler

df = pd.read_csv('diabetes.csv')
scaler = StandardScaler()
X_scaled = scaler.fit_transform(df.drop('Outcome', axis=1))  # Features
2. Train-Test Split
The dataset is split into training and testing sets using train_test_split from sklearn.model_selection.


from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X_scaled, df['Outcome'], test_size=0.2, random_state=42)
3. Model Training
The Gradient Boosting Classifier is used to train the model on the training dataset.


from sklearn.ensemble import GradientBoostingClassifier

model = GradientBoostingClassifier()
model.fit(X_train, y_train)
4. Model Prediction
The trained model is used to make predictions on the test dataset.


y_pred = model.predict(X_test)
5. Model Evaluation
The model is evaluated using the classification report and the ROC AUC score to measure its performance.


from sklearn.metrics import classification_report, roc_auc_score

print(classification_report(y_test, y_pred))
print(f"ROC AUC Score: {roc_auc_score(y_test, y_pred):.4f}")
6. Results
Classification Report: Displays precision, recall, and F1-score for each class.

ROC AUC Score: A metric that evaluates the ability of the model to distinguish between the two classes (diabetes vs. no diabetes).

Requirements
To run this project, you need to install the following libraries:

pandas

scikit-learn

You can install the required libraries using pip:

pip install pandas scikit-learn
How to Run
Clone the repository or download the diabetes.csv dataset.

Install the required dependencies as mentioned above.

Run the Python script to load, train, and evaluate the model.

python diabetes_prediction.py
Conclusion
This project demonstrates the implementation of a Gradient Boosting Classifier to predict diabetes. The model achieves good performance based on the evaluation metrics, and it can be used to predict diabetes risk in patients based on health metrics.
