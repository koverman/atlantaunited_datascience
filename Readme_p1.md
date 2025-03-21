# Project 1: Exploratory Data Analysis and Feature Engineering

## Overview

This notebook reads a little like stream of consciousness. Within the notebook, the provided matchlog and schedule datasets undergo exploratory data analysis, feature engineering, and feature selection using a catboost model to prepare the data for a final catboost model. The goal is to predict the upcoming weekend's non-penalty xGoal + xAssist (referred to as xTotal) for individual players based on the selected features.

## Requirements

This notebook is run on Python version 3.9.6. The following Python libraries are required to run this notebook:

- pandas
- numpy
- matplotlib
- catboost
- scikit-learn

## Data Sources

The notebook loads the following, provided datasets:

- `atlutd_datascientist_project1_matchlog.csv`: Contains match logs with relevant player statistics.
- `atlutd_datascientist_project1_schedule.csv`: Provides match schedule information.

## Steps Included

1. **Exploratory Data Analysis (EDA)**
   - Checking for missing values
   - Plotting different attributes to understand distributions and relationships

2. **Feature Engineering & Selection**
   - Scaling numerical features
   - Splitting data into training and test sets
   - Selecting features for modeling using catboost's built-in feature importance and setting a threshold

3. **Prediction of Players' xTotal for the Upcoming Weekend**
   - Using the selected features, a catboost model is trained to predict each player's xTotal
   - Given the necessary data, the model outputs the predicted xTotal for individual players. That output is sorted and filtered to show the top 10 players with the highest xTotal values

## How to Use

1. Ensure all dependencies are installed.
2. Place the required datasets in the appropriate directory.
3. Run the notebook sequentially to perform EDA, feature engineering and selection, and predict players' xG.

## Output

The processed dataset and selected features will be used for further modeling and predictions. There's a table displaying top 10 predicted xTotal and the corresponding players' names.
