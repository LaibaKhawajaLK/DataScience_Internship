# 📊 Loan Default Prediction - Data Science Internship Task

This project is part of the Data Science Internship (Task 8), where the goal is to predict the likelihood of a loan default using machine learning techniques. The dataset contains loan-related attributes such as annual income, term, grade, employment length, home ownership, and more.

---

## ✅ Objective

To build a predictive model that classifies whether a loan will default (`bad_loan = 1`) or be repaid (`bad_loan = 0`) based on historical loan data.

---

## 📁 Dataset

The dataset file used is: `loan_data.csv`

### Features Used:
- `grade`: Credit grade of the loan
- `annual_inc`: Annual income of the borrower
- `emp_length_num`: Numeric representation of employment length
- `home_ownership`: Type of home ownership
- `term`: Loan term
- `od_ratio`: Outstanding debt ratio

### Target Variable:
- `bad_loan`: Binary classification target (`1 = Default`, `0 = Fully Paid`)

---

## 🛠️ Steps Followed

1. **Data Cleaning & Selection**
   - Selected relevant columns from the dataset
   - Filtered and encoded the target variable

2. **Feature Encoding**
   - Used one-hot encoding for categorical variables such as `grade`, `home_ownership`, and `term`

3. **Feature Scaling**
   - Applied `StandardScaler` to normalize numerical features

4. **Model Building**
   - Split the data into training and testing sets (80/20)
   - Trained a `GradientBoostingClassifier` model

5. **Model Evaluation**
   - Evaluated using classification metrics:
     - Accuracy
     - Precision, Recall, F1-Score
     - ROC AUC Score

---

## 📈 Results

The Gradient Boosting model was evaluated using classification report metrics and ROC AUC score. The performance shows promising predictive ability in identifying potential loan defaulters.

---

## 📚 Libraries Used

- `pandas`
- `numpy`
- `scikit-learn` (`train_test_split`, `StandardScaler`, `GradientBoostingClassifier`, `classification_report`, `roc_auc_score`)

---

## 📌 How to Run

1. Clone the repository or download the script.
2. Place the `loan_data.csv` file in the same directory.
3. Run the Python notebook or script to execute the analysis.

---

## ✍️ Author

**Laiba Khawaja**  
Data Science Intern @ DevelopersHub Corporation  
April 2025  
