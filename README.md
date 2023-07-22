# Real Estate Price Prediction

This project aims to predict real estate prices based on various features such as location, total square feet area, number of bathrooms, and number of bedrooms (BHK). The dataset used for this project is from the `house.csv` file.

## Table of Contents
- [Introduction](#introduction)
- [Data Cleaning](#data-cleaning)
- [Outlier Detection/Removal](#outlier-detectionremoval)
- [Feature Engineering](#feature-engineering)
- [Model Building](#model-building)
- [K-Fold Cross Validation](#k-fold-cross-validation)
- [Grid Search](#grid-search)
- [Usage](#usage)

## Introduction

In this project, we use Python with libraries like Pandas, NumPy, and scikit-learn for data manipulation, cleaning, and building a Linear Regression model to predict real estate prices. The dataset consists of various features like area type, availability, location, size, society, total square feet area, number of bathrooms, number of balconies, and price.

## Data Cleaning

We start by importing the required libraries and loading the dataset from the `house.csv` file. We perform data cleaning by dropping irrelevant columns like area type, society, balcony, and availability. We also handle missing values and convert the 'size' column to a new 'bhk' column for the number of bedrooms.

## Outlier Detection/Removal

Next, we detect and remove outliers from the 'bhk' and 'price_per_sqft' columns. Outliers are data points that deviate significantly from the average and can affect the model's performance.

## Feature Engineering

We perform feature engineering to convert the 'total_sqft' values, which sometimes represent a range, into a single numerical value for better analysis. Additionally, we handle categorical data like location by creating dummy variables.

## Model Building

After data preprocessing, we split the dataset into training and testing sets and build a Linear Regression model to predict real estate prices based on the features.

## K-Fold Cross Validation

We use K-Fold Cross Validation to evaluate the model's performance on different subsets of the data.

## Grid Search

To find the best hyperparameters for our model, we implement Grid Search, which exhaustively searches through specified parameter values to achieve optimal performance.

## Usage

To predict real estate prices, you can use the `predict_price` function and provide the location, total square feet area, number of bathrooms, and number of bedrooms (BHK).

Example usage:
```python
predicted_price = predict_price('1st Phase JP Nagar', 1000, 2, 2)
print(predicted_price)
