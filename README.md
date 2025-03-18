Data Science Internship - Task 1

Exploratory Data Analysis (EDA) on Titanic Dataset

Project Description

This project focuses on performing Exploratory Data Analysis (EDA) on the Titanic dataset. The dataset includes details about passengers, such as age, gender, ticket class, and survival status. The goal is to analyze patterns and insights using data visualization techniques.

Dataset Used

- Titanic Dataset (Available in Seaborn library or Kaggle)
- Contains passenger details like Age, Fare, Gender, Class, and Survival status.

Tasks Performed

1. Data Loading and Inspection

- Loaded the dataset using `pandas`.
- Displayed the first few rows and checked basic information.
- Identified missing values in `Age`, `Cabin`, and `Embarked`.

2. Data Cleaning

- Imputed missing `Age` values using the mean.
- Dropped the `Cabin` column due to excessive missing values.
- Filled missing `Embarked` values with the most common category.
- Removed duplicate rows if present.

3. Outlier Detection and Handling

- Used box plots to detect outliers in numeric columns like `Fare`.
- Removed extreme outliers using the Interquartile Range (IQR) method.

4. Data Visualization

- Bar Charts: Passenger class distribution.
- Histograms: Age distribution of passengers.
- Heatmaps: Correlation between numeric features.

5. Insights and Observations

- Higher survival rates for women and children.
- First-class passengers had better survival chances.
- Passengers paying higher fares had a higher likelihood of survival.

How to Run the Notebook

1. Clone this repository:
      git clone https://github.com/LaibaKhawaja/DataScience_Internship.git
 
2. Navigate to the project folder:
      cd DataScience_Internship
   
3. Install required libraries:
      pip install pandas numpy matplotlib seaborn
  
4. Open the Jupyter Notebook:
   
   jupyter notebook "DataScience Internship task 1.ipynb"
   

Project Structure

├── DataScience Internship task 1.ipynb  # Jupyter Notebook with EDA
├── Titanic-Dataset.csv                          # Titanic Dataset 
├── README.md                            # Project Documentation


Author
LaibaKhawaja - Data Science Intern

