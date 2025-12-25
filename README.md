# CGM - Meal and Insulin Impact Analysis
One of the most valuable insights for users is understanding how meals and insulin timing influence postprandial (after-meal) glucose spikes. This project simulates a real analytics use case by transforming CGM data into actionable, interpretable insights.

## Problem Statement
Analyze how meal intake and insulin dosage impact postprandial glucose response and build predictive models to estimate: 
- Glucose spike magnitude
- Time-to-peak glucose after meals

## Models, Tools & Librabries
- Python Libraries - Pandas, Numpy, Matplotlib, Scikit Learn, Seaborn
- Models used -   Linear Regression, Random forest, Gradient Boosting Regressor
- Evaluation Metrics - Mean Absolute Error, Root Mean squared Error (RMSE), R-squared
  
## Data Overview
- Total CGM readings - 100,800
- Number of Patients - 25
- Monitoring duration - 14 days per patient
- Total meal events - 2972
- Data collection period - 01-01-2024 to 14-01-2024

## Exploratory Data Analysis (EDA)
- Glucose statistics (mg/dL)
  - Mean : 97.6 mg/dL
  - Median : 95.8 mg/dL
  - Std Dev : 36.4 mg/dL
  - Min : 60 mg/dL
  - Max : 300 mg/dL
  - Missing values : 4928 (4.9%)

- Meal Analysis
  - Breakfast events : 992
  - Lunch events : 982
  - Dinner events : 998
  - Average carb Intake : 58.4 g
  - Average insulin units : 8.2 units
 
  ## Graphs and Demo

  [Graphs Preview](https://github.com/sidhmen09/CGM---Meal-and-Insulin-Impact-Analysis/blob/main/eda_visualization.png)
  
