
# Diabetes Prediction Project

## Introduction

The goal of this project is to analyze the diabetes prediction dataset and build a predictive model to determine if a patient has diabetes based on their HbA1c level. The dataset contains 100,000 rows and 9 columns, with information about patients' age, gender, hypertension status, heart disease status, smoking history, BMI (Body Mass Index), HbA1c level (a measure of blood sugar control), blood glucose level, and whether they have diabetes.

## Data Preprocessing

### Data Cleaning

1. Checked for missing values: There were no missing values in the dataset.
2. Checked for duplicate rows: Found 3,854 duplicate rows which were removed from the dataset.

### Exploratory Data Analysis (EDA)

1. Visualized the distribution of age, BMI, HbA1c level, and blood glucose level using histograms and box plots.
2. Examined the frequencies or proportions of categorical variables such as gender, hypertension status, heart disease status, and smoking history.
3. Created a correlation matrix to identify relationships between variables. Notably, HbA1c level had a moderate positive correlation (0.41) with diabetes.

### Statistical Analysis

1. Performed a t-test to compare the mean HbA1c levels between patients with and without diabetes.
   - Result: There was a significant difference between the two groups (p-value < 0.05).

## Modeling

Two models were trained on the dataset using only HbA1c_level as a predictor variable for diabetes:

### Logistic Regression Model

- Split the data into training (80%) and testing (20%) sets.
- Trained a logistic regression model on the training set.
- Made predictions on the testing set.
- Evaluated model performance:
  - Accuracy: 0.9378
  - Confusion Matrix: [[17509, 0], [1197, 524]]

### Random Forest Model

- Split the data into training (80%) and testing (20%) sets.
- Trained a random forest model on the training set.
- Made predictions on the testing set.
- Evaluated model performance:
  - Accuracy: 0.9517
  - Confusion Matrix: [[17509, 0], [929, 792]]

## Results and Conclusion

From the analysis and modeling, we can conclude that there is a significant difference in HbA1c levels between patients with and without diabetes. Using HbA1c level as a predictor variable can help predict diabetes with reasonable accuracy. The Random Forest model performed slightly better than the Logistic Regression model in terms of accuracy.
