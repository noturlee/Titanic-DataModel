<img src="Images/banner.gif">

# Titanic Survival Prediction Model

## Table of Contents

- [Objective](#objective)
- [Dataset Description](#dataset-description)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
  - [Logistic Regression](#logistic-regression)
  - [Random Forest](#random-forest)
- [Data Visualisations](#data-visualisations)
- [Best Model - Random Forest Model (with Hyperparameter Tuning)](#best-model---random-forest-model-with-hyperparameter-tuning)
- [Conclusion](#model-conclusion)
- [Final Thoughts](#final-thoughts)


  
##  Objective
The objective of this project was to build a predictive model using the Titanic dataset to determine whether a passenger on the Titanic survived or not. This dataset is a common starting point for data science and machine learning projects due to its simplicity and the availability of relevant features.

## Dataset Description
<br>
The Titanic dataset contains information about individual passengers, including the following features:
- **Pclass**: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings or spouses aboard the Titanic
- **Parch**: Number of parents or children aboard the Titanic
- **Ticket**: Ticket number
- **Fare**: Passenger fare
- **Cabin**: Cabin number
- **Embarked**: Port of embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)
- **Survived**: Survival status (0 = No, 1 = Yes) [Target variable]
<br>

## Data Preprocessing
<br>

Before building the models, the following preprocessing steps were undertaken:
1. **Handling Missing Values**: Missing values in the `Age`, `Cabin`, and `Embarked` columns were addressed.
   - `Age` was imputed using the median age.
   - `Cabin` information was dropped due to a large number of missing values.
   - Missing values in `Embarked` were filled with the most common port (`S`).

2. **Feature Encoding**: Categorical variables (`Sex`, `Embarked`) were converted into numerical values using one-hot encoding.

3. **Feature Scaling**: Continuous variables (`Age`, `Fare`) were standardized to have a mean of 0 and a standard deviation of 1.
<br>

## Model Building
<br>

Two machine learning models were trained and evaluated: Logistic Regression and Random Forest. Additionally, Randomized Search Cross-Validation was used to tune the hyperparameters of the Random Forest model.

<br>

### Logistic Regression
<br>

- **Accuracy**: 0.80
- **Precision, Recall, and F1-Score**:
  
<img width="1192" alt="Screenshot 2024-06-14 at 13 44 23" src="https://github.com/noturlee/TitanicModel-CODSOFT/assets/100778149/b1d6fc55-96bf-4192-b23f-54afeca86f89">

<br>

### Random Forest
<br>

- **Accuracy**: 0.82
- **Precision, Recall, and F1-Score**:

<img width="1192" alt="RandomForestOutput" src="https://github.com/noturlee/TitanicModel-CODSOFT/assets/100778149/7e3619ec-476c-4279-8c75-81334a850d19">

<br>
## Data Visualisations
<br>

<p float="left">
<img width="400" alt="Screenshot 2024-06-14 at 13 45 37" src="https://github.com/noturlee/TitanicModel-CODSOFT/assets/100778149/4682463d-3dd6-4a76-9eb3-c1bace73bdb7">
<img width="400" alt="Screenshot 2024-06-14 at 13 45 49" src="https://github.com/noturlee/TitanicModel-CODSOFT/assets/100778149/a7f3229c-f6bb-41a5-b6ae-0e5337aabfa3">
</p>
<p float="left">
<img width="400" alt="Screenshot 2024-06-14 at 13 45 59" src="https://github.com/noturlee/TitanicModel-CODSOFT/assets/100778149/6432372c-f1a1-470e-b6b3-72cc4477bf0e">
<img width="400" alt="Screenshot 2024-06-14 at 13 46 15" src="https://github.com/noturlee/TitanicModel-CODSOFT/assets/100778149/0c190d54-285e-4e52-9f57-2ce8c638ffce">
</p>

<br>
### Best Model - Random Forest Model (with Hyperparameter Tuning)
<br>

- **Accuracy**: 0.82
- **Precision, Recall, and F1-Score**:


<br>
## Model Conclusion
<br>
The Random Forest model with hyperparameter tuning performed slightly better than the Logistic Regression model, achieving an accuracy of 82%. The precision, recall, and F1-score indicate that the model is reasonably good at predicting survival on the Titanic, with a higher precision for predicting non-survival (class 0) and a balanced performance for survival (class 1).
<br>

## Final Thoughts
<br>
The predictive models built using the Titanic dataset offer valuable insights into the factors that influenced survival on the Titanic. Analysis of the dataset revealed the following key points about survival:

1. **Gender**: Women had a significantly higher survival rate compared to men. This is reflected in the model's feature importance, where gender (Sex) was one of the most influential factors.
   
2. **Passenger Class**: Passengers in first class (Pclass = 1) had a higher survival rate compared to those in second and third classes. This indicates that socio-economic status played a crucial role in survival chances.

3. **Age**: Younger passengers had a better chance of survival compared to older passengers. Children, in particular, had higher survival rates.

4. **Family Size**: Passengers with fewer family members aboard (SibSp and Parch) tended to survive more often than those with larger families.

5. **Embarkation Point**: Passengers who embarked from Cherbourg (Embarked = C) had a slightly higher survival rate compared to those who boarded at Queenstown or Southampton.
<br>

In conclusion, the model successfully identifies the key determinants of survival, emphasizing the importance of gender, socio-economic status, age, and family size. These findings align with historical accounts and provide a comprehensive understanding of the factors that influenced survival during the Titanic disaster. The models developed in this project serve as an effective tool for predicting survival and demonstrate the potential of machine learning in analyzing historical datasets.








