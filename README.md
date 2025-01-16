# Diabetes Prediction Model

### Overview

This project aims to build a predictive model to diagnose whether a patient has diabetes based on specific medical measurements. The dataset used is the Pima Indians Diabetes Dataset, sourced from the National Institute of Diabetes and Digestive and Kidney Diseases.

The predictive model leverages various machine learning techniques, including logistic regression with hyperparameter tuning, to achieve optimal performance. The implementation includes robust data preprocessing, feature selection, handling imbalanced datasets, and model evaluation.

### Problem Statement

Diabetes is a chronic condition that can lead to serious health complications if not managed properly. Early detection is crucial for effective treatment and management of the disease. The problem this project aims to solve is to accurately predict whether an individual has diabetes based on diagnostic measurements such as glucose levels, blood pressure, and BMI. This predictive model could be used as a supplementary tool in clinical settings to aid in the early diagnosis of diabetes.

### Data Description and Source

The dataset used in this project is sourced from the National Institute of Diabetes and Digestive and Kidney Diseases. It is publicly available and contains medical records of female patients who are at least 21 years old and of Pima Indian heritage. The dataset includes the following attributes:

- Pregnancies: Number of times the patient has been pregnant.
- Glucose: Glucose concentration in the blood (mg/dL).
- BloodPressure: Diastolic blood pressure (mm Hg).
- SkinThickness: Triceps skin fold thickness (mm).
- Insulin: 2-Hour serum insulin (mu U/mL).
- BMI: Body mass index (weight in kg/(height in m)^2).
- DiabetesPedigreeFunction: A function that represents diabetes genetic risk.
- Age: Age of the patient (years).
- Outcome: The target variable indicating whether the patient has diabetes (1) or not (0).

This dataset was curated with specific constraints: all patients are females of Pima Indian heritage, a population known to have a higher incidence of diabetes. The dataset will be used to build and evaluate different machine learning models to predict diabetes, with the aim of selecting the most effective model for this task.

### Solution Approach

1. Data Preprocessing
- Handling Missing Values: Replaced zero values in Glucose, BloodPressure, SkinThickness, Insulin, and BMI with the median value of each column.
- Feature Scaling: Standardized the features using StandardScaler to normalize data for better model performance.

2. Handling Imbalanced Data
- SMOTE (Synthetic Minority Oversampling Technique): Used SMOTE to balance the classes in the dataset by oversampling the minority class.

3. Feature Selection
- Selected features based on their correlation with the target variable (Outcome) using a correlation threshold of 0.1.

4. Model Building and Hyperparameter Tuning

Logistic Regression:
- Tuned hyperparameters using GridSearchCV to find the best combination of regularization (C) and solver.

Evaluation Metrics:
- Accuracy
- Precision, Recall, and F1 Score
- ROC AUC Score

5. Model Evaluation

- Evaluated the model's performance on a test set using a confusion matrix and classification report.

6. Saving the Model

- Saved the best logistic regression model using the pickle library for future use.

7. Prediction Demonstration

- Provided a demonstration of predicting diabetes risk for a new patient using the trained model.

1. Data Preprocessing

Handling Missing Values: Replaced zero values in Glucose, BloodPressure, SkinThickness, Insulin, and BMI with the median value of each column.

Feature Scaling: Standardized the features using StandardScaler to normalize data for better model performance.

2. Handling Imbalanced Data

SMOTE (Synthetic Minority Oversampling Technique): Used SMOTE to balance the classes in the dataset by oversampling the minority class.

3. Feature Selection

Selected features based on their correlation with the target variable (Outcome) using a correlation threshold of 0.1.

4. Model Building and Hyperparameter Tuning

Logistic Regression:

Tuned hyperparameters using GridSearchCV to find the best combination of regularization (C) and solver.

Evaluation Metrics:

Accuracy

Precision, Recall, and F1 Score

ROC AUC Score

5. Model Evaluation

Evaluated the model's performance on a test set using a confusion matrix and classification report.

6. Saving the Model

Saved the best logistic regression model using the pickle library for future use.

7. Prediction Demonstration

Provided a demonstration of predicting diabetes risk for a new patient using the trained model.

Installation

To run this project, ensure you have the following libraries installed:

pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn xgboost

How to Run the Project

Clone the Repository

git clone <repository_url>
cd <repository_name>

Place Dataset
Ensure the dataset file diabetes.csv is located in the root directory of the project.

Run the Script

python diabetes_prediction.py

Evaluate Results
View the output metrics (accuracy, precision, recall, F1 score, ROC AUC) and the confusion matrix.

Make Predictions
Use the provided new_data example or input your own data to make predictions.

### Results

Best Model: Logistic Regression with tuned hyperparameters.

Performance Metrics:
- Accuracy: ~69%
- ROC AUC Score: ~81%

### Source:

The dataset is publicly available and is widely used for educational and research purposes. It is often referred to as the "Pima Indians Diabetes Database" and can be found on platforms like Kaggle or the UCI Machine Learning Repository.

https://www.kaggle.com/datasets/mathchi/diabetes-data-set
