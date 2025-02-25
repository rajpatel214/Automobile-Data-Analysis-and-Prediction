# Automobile Data Analysis and Prediction

## Project Overview
This project focuses on analyzing an automobile dataset to explore various features of cars, identify trends, detect outliers, and predict car prices using machine learning models. The dataset contains information about different attributes such as engine type, fuel system, body style, horsepower, and more.

## Dataset
- The dataset used: `autoss.csv`
- Contains various attributes related to automobile specifications and prices.
- Includes categorical and numerical features.

## Exploratory Data Analysis (EDA)
### 1. Data Loading and Cleaning
- Read the dataset using `pandas`
- Handle missing values and incorrect values (e.g., replacing `?` with median or mean values)
- Display dataset information such as column names, data types, and missing values

### 2. Data Visualization
- **Count Plots**: Display distribution of categorical variables like `symboling`, `drive-wheels`, `engine-type`, and `num-of-cylinders` using `seaborn`.
- **Distribution Plots**: Visualize numerical features like `normalized-losses`, `bore`, `stroke`, `compression-ratio`, `engine-size`, `horsepower`, etc.
- **Bar Charts**: Show the frequency of `make`, `body-style`, and `fuel-system`.
- **Pie Charts**: Represent `fuel-type`, `aspiration`, and `num-of-doors` proportions.
- **Histograms**: Analyze the distribution of features like `wheel-base`, `width`, and `height`.
- **Box Plots**: Identify outliers in features like `normalized-losses`, `symboling`, `length`, `curb-weight`, etc.

## Machine Learning Models
### 1. Data Preprocessing
- One-Hot Encoding categorical features.
- Splitting data into training (`80%`) and testing (`20%`) sets.
- Standardizing numerical features using `StandardScaler`.

### 2. Regression Models for Price Prediction
- **Linear Regression**: Baseline model (`score = 0.74`)
- **Ridge Regression**: Improved model with regularization (`score = 0.748`)
- **Lasso Regression**: Regularized model (`score = 0.750`)
- **Decision Tree Regressor**: Non-linear model (`score = 0.82`)
- **Bagging Regressor**: Ensemble learning method (`score = 0.805`)
- **Hyperparameter Tuning**: Used `RandomizedSearchCV` to optimize model parameters.

## Results and Insights
- The decision tree model performed best with a score of `0.82`, followed by bagging regression.
- Feature importance analysis showed that `engine-size`, `horsepower`, and `curb-weight` significantly influence car prices.
- Cars with turbo aspiration and higher compression ratios tend to have higher prices.

