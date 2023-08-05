# Titanic Survival Analysis

## Introduction

This repository explores the infamous Titanic shipwreck that occurred in 1912. The disaster led to the tragic loss of 1502 out of 2224 passengers and crew members on board. This project analyzes the various factors that might have affected the survival rates of the passengers and crew.

## Data

The dataset used in this project includes the following features:

- `PassengerId`: Unique identifier for each passenger
- `Survived`: Denotes whether the passenger survived (1) or died (0)
- `Pclass`: Class of the passenger's ticket
- `Name`: Passenger's name
- `Sex`: Passenger's gender
- `Age`: Passenger's age
- `SibSp`: Number of the passenger's siblings/spouses on board
- `Parch`: Number of the passenger's parents/children on board
- `Ticket`: Ticket number
- `Fare`: Cost of the ticket
- `Cabin`: Cabin category
- `Embarked`: Port where the passenger embarked (C= Cherbourg, Q = Queenstown, S= Southampton)

The dataset is divided into a training and a testing set.

## Workflow

The workflow of this notebook can be broadly divided into the following steps:

1. **Loading and Checking the Data:** The Titanic dataset is loaded into the environment. The structure of the data is explored using methods like `head()`, `describe()`, and `info()`.

2. **Variable Description and Exploration:** Each feature in the dataset is analyzed to get a better understanding of the data. For categorical features, bar plots are used to visualize the frequency of each category. For numerical features, histograms are used to understand the distribution of the data.

3. **Basic Data Analysis:** The relationship between various features (`Pclass`, `Sex`, `SibSp`, `Parch`) and the target variable `Survived` is analyzed by grouping the data based on these features and calculating the mean survival rate.

4. **Outlier Detection:** Outliers in the dataset are identified using Turkey's method (1.5 * Inter-Quartile Range). The identified outliers are then removed from the dataset to improve the accuracy of the analysis.

5. **Missing Value Treatment:** Missing values in the dataset are identified and imputed with suitable values. For example, the missing values in the `Embarked` feature are filled using 'C' based on the distribution of fare among different embarkment points, and the missing values in the `Fare` feature are filled using the mean fare of passengers in `Pclass` 3.

## Conclusion and Final Steps

At the end of the exploratory data analysis, we have a dataset that is ready for machine learning modeling. We have analyzed the correlation between various features and the target variable `Survived`, which provides us with useful insights into the data. The outliers in the dataset were identified and removed, ensuring a higher quality of data for training our model. Missing values were also treated using appropriate methods to avoid inaccuracies in prediction.

In the final steps, the preprocessed data could be used to train a machine learning model. This model can predict whether a passenger on the Titanic would have survived or not, based on the features in the dataset. The model's performance can be evaluated using appropriate metrics such as accuracy, precision, recall, F1-score, and AUC-ROC.

The primary goal of this project is to understand the importance of data preprocessing and exploratory data analysis in any machine learning workflow. It demonstrated the different steps involved in data preprocessing, including data cleaning, outlier detection, and missing value imputation.

Further work in this project could involve tuning the model's hyperparameters to enhance its performance, applying different machine learning algorithms, and conducting a more in-depth analysis of the features to gain additional insights.
## How to Run

Ensure that you have the necessary packages (Numpy, Pandas, Matplotlib, Seaborn) installed. You can run the notebook using a Jupyter server. You can access the dataset by clicking [here](https://www.kaggle.com/competitions/titanic) and the notebook on Kaggle by clicking [here](https://www.kaggle.com/code/okanarslan/okan-arslan-titanic-eda/notebook).
