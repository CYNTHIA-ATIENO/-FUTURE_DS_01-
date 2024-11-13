# FUTURE_DS_01-  Titanic Dataset: EXPLORATORY DATA ANALYSIS
## Table of Contents
- [Introduction](#introduction)
- [Dataset Overview](#dataset-overview)
- [Data Features](#data-features)
  - [Passenger Information](#passenger-information)
  - [Ticket Information](#ticket-information)
  - [Survival Information](#survival-information)
- [Data Preprocessing](#data-preprocessing)
- [EDA](#EDA)
  - [Basic Statistics](#Basic Statistics)
 [Visualizations](#visualizations)
  - [Distribution of Numerical Features](#distribution-of-numerical-features)
  - [Univariate Analysis of Numerical Variables](#univariate-analysis-of-numerical-variables)
  - [Univariate Analysis of Categorical Variables](#univariate-analysis-of-categorical-variables)
  - [Bivariate Analysis](#bivariate-analysis)
  - [Multivariate Analysis](#multivariate-analysis)
- [Conclusions](#Conclusions)
- [Recommendation](#Recommendation)


## Introduction
The Titanic dataset contains information about the passengers aboard the ill-fated Titanic ship, which sank in 1912. The goal of this project is to predict whether a passenger survived or not based on the features available in the dataset.
   
![Stöwer_Titanic](https://github.com/user-attachments/assets/418b2dbf-413d-4240-9e04-4f13d0e9a0ef)
![download](https://github.com/user-attachments/assets/cc44d1c0-a637-481d-86ee-f4c060831f28)
![download](https://github.com/user-attachments/assets/9105683b-0146-4877-a43d-3947477edd5c)



## Dataset Overview
The Titanic dataset contains details of **891 passengers** from the Titanic disaster. The key objective is to predict whether a passenger survived or not, using several features about the passengers.

### Data Features
The dataset includes several features, some of which are:
- **Pclass**: Passenger class (1, 2, 3)
- **Name**: Passenger's name
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings or spouses aboard
- **Parch**: Number of parents or children aboard
- **Fare**: Fare paid for the ticket
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

### Passenger Information
- **Pclass**: The class of the passenger's ticket (1st, 2nd, or 3rd class)
- **Name**: Full name of the passenger, which can be used to derive titles (e.g., Mr, Mrs, Dr, etc.)
- **Sex**: Gender of the passenger (Male or Female)
- **Age**: Age of the passenger, which can be used to create new features (e.g., Is Child, Is Senior)

### Ticket Information
- **Ticket**: The ticket number assigned to the passenger.
- **Fare**: The amount paid for the ticket, which could indicate socioeconomic status.
### Survival Information
- **Survived**: The target variable (1 if the passenger survived, 0 if they did not).

## Data Preprocessing
Data preprocessing is a critical step in building machine learning models. We will perform:
- **Handling Missing Data**: Many columns, especially `Age`, have missing values. We will impute missing values using the median for `Age` and the mode for `Embarked`.
- **Feature Encoding**: Convert categorical features like `Sex` and `Embarked` into numerical formats using one-hot encoding or label encoding.
- **Feature Scaling**: Normalize continuous features like `Fare` and `Age`.
## Visualizations

### Distribution of Numerical Features
We'll start by looking at the **distribution** of some key numerical features like `Age` and `Fare`.

### Distribution of Age
![Age Distribution](images/age_distribution.png)

This histogram shows the distribution of passengers' ages.

### Distribution of Fare
![Fare Distribution](images/fare_distribution.png)

### Explanation of Each Section:

#### 1. **Distribution of Numerical Features**:
   - Histograms show the distribution of `Age` and `Fare`. These are helpful for understanding the overall spread of numerical data.
   
#### 2. **Univariate Analysis of Numerical Variables**:
   - **Boxplot**: Visualizes the spread and central tendency of `Age` with respect to `Survived`. This is especially useful for spotting outliers and understanding the distribution of the data.

#### 3. **Univariate Analysis of Categorical Variables**:
   - **Countplot**: Visualizes the frequency distribution of categorical variables like `Sex`, `Pclass`, and `Embarked`. This is useful for understanding how many instances each category has and how they relate to survival.

#### 4. **Bivariate Analysis**:
   - A **scatterplot** is used to explore the relationship between two variables, such as `Age` and `Fare`. Coloring the points by `Survived` gives insights into how the combination of these variables may affect survival.

#### 5. **Multivariate Analysis**:
   - **Heatmap**: Shows the correlation between various numerical features. This is helpful in identifying which features are strongly correlated, guiding feature selection and engineering for model building.

- [Conclusions](#conclusions)

Based on the EDA, we will conclude the factors that contributed to the survival of the passenger or not.

  - [Did children have a higher chance of survival?](#did-children-have-a-higher-chance-of-survival)
  - [Were women and children prioritized in lifeboat boarding?](#were-women-and-children-prioritized-in-lifeboat-boarding)
  - [Did passengers from higher classes have a higher chance of survival?](#did-passengers-from-higher-classes-have-a-higher-chance-of-survival)
  - [How did age, sex, and embarkation point influence survival chances?](#how-did-age-sex-and-embarkation-point-influence-survival-chances)
  - [Safety Measures and Emergency Preparedness](#safety-measures-and-emergency-preparedness)
    
 [Recommendations](#recommendations)
  - [Prioritize Vulnerable Populations](#prioritize-vulnerable-populations)
  - [Gender-Neutral Evacuation Policies](#gender-neutral-evacuation-policies)
  - [Ensure Equal Access to Lifeboats and Safety Equipment](#ensure-equal-access-to-lifeboats-and-safety-equipment)
  - [Improve Emergency Training and Preparedness for All Passengers](#improve-emergency-training-and-preparedness-for-all-passengers)
