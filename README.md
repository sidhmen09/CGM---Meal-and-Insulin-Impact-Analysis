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
  - Average insulin units : 8.2 unit

![Graphs Preview](https://github.com/sidhmen09/CGM---Meal-and-Insulin-Impact-Analysis/blob/main/eda_visualization.png)

## Model Performance & Feature Importance

-  Model Performance
  
    - Spike Magnitude (R²) : 0.664
    - Spike Magnitude (MAE) : 33.97 mg/dL
    - Time to Peak (R²) : 0.105
    - Time to Peak (MAE) : 8.42 minutes

-  Top 5 Predictive Features:
  
    - time_since_last_insulin : 0.425
    - baseline_glucose : 0.208
    - insulin_to_carb_ratio : 0.139
    - carbs : 0.136
    - activity_adjusted_carbs : 0.041

![Graphs Preview](https://github.com/sidhmen09/CGM---Meal-and-Insulin-Impact-Analysis/blob/main/model_performance.png)

## Prediction Analysis

![Graphs Preview](https://github.com/sidhmen09/CGM---Meal-and-Insulin-Impact-Analysis/blob/main/predictions_analysis.png)

## Key Insights

-  High-carb meals with low activity produce 125.7 mg/dL spikes vs. 113.8 mg/dL with high activity (11.9 mg/dL reduction).
-  Pre-meal insulin (within 30 min) reduces spikes by 111.8 mg/dL compared to insulin given >60 minutes before meals.
-  Dinner meals show highest spike magnitude (96.2 mg/dL) and longest time-to-peak (9.8 min).
-  Optimal insulin-to-carb ratio: 0.167 units/gram (Current average: 0.144 units/gram).
-  Higher baseline glucose (>120 mg/dL) associated with -124.1 mg/dL larger postprandial spikes.
