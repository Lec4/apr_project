---
title: Methodology
layout: default
--- 
# Methodology

## 1. Data Preprocessing

Before performing any statistical analysis, the data needed to be cleaned and preprocessed. The following steps were taken to prepare the dataset for analysis:

- **Handling Missing Values**: 
  - The `Age` variable had several missing values. We imputed these using the median age by passenger class.
  - The `Cabin` variable was mostly missing, so it was excluded from the analysis.
  - The `Embarked` variable had two missing values, which were filled with the most common port of embarkation.
  
- **Encoding Categorical Variables**:
  - The categorical variables `Sex` and `Embarked` were converted into binary and one-hot encoded features, respectively.
  - `Pclass` (Passenger Class) was treated as a categorical variable, even though it is numeric (1, 2, 3).

- **Feature Engineering**:
  - Created a new variable `FamilySize` by combining the `SibSp` (siblings/spouses aboard) and `Parch` (parents/children aboard) variables.
  - Created an indicator variable for whether a passenger was traveling alone (`IsAlone`).

## 2. Exploratory Data Analysis (EDA)
