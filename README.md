# Classification

### Project Summary

The goal of this project is to build a predictive model to diagnose whether a patient has diabetes based on specific medical measurements. The outcome of this project could support healthcare professionals in making more informed decisions and early interventions for patients at risk of diabetes.

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

### Source:

The dataset is publicly available and is widely used for educational and research purposes. It is often referred to as the "Pima Indians Diabetes Database" and can be found on platforms like Kaggle or the UCI Machine Learning Repository.

### Overview of Models Selected

1. Logistic Regression

Serves as a baseline model for binary classification tasks, then optimized through hyperparameter tuning using GridSearchCV.

2. Random Forest Classifier

Random Forest Classifier generally provides high accuracy and good handling of unbalanced datasets without scaling requirements. It's good for benchmarking against Logistic Regression. Random Forest Classifier was applied directly with default settings and evaluated on the testing set.

3. Support Vector Machine (SVM)

SVM is effective for high-dimensional spaces and capable of defining complex higher-order separation planes through kernels. It is used with probability estimates enabled (probability=True) for binary classification. 
