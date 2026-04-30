## Overview
This project analyzes global life expectancy using country-level data on economic, environmental, and health factors. We were 
interested in investigating “What economic, environmental, and health indicators are associated with life expectancy worldwide, and what are their relative effects?”
The goal is to understand how these variables influence outcomes using machine learning and visualization techniques. 

## Methods
Merged life expectancy and GDP datasets by country and year.
Cleaned data by removing high-missing columns and imputing values using interpolation and income-group medians.
Split data by country to prevent data leakage.
Trained a Random Forest Regressor.
Evaluated performance using R², RMSE, and Group K-Fold cross-validation.
Assessed feature importance and generated Partial Dependence Plots (PDPs) for interpretation.

## Key Findings
The model explains a large portion of variation in life expectancy (R² ≈ 0.68 test, ~0.58 CV).
Most important predictors: CO₂, Injuries (DALYs), Unemployment, GDP.
CO₂ and GDP show positive relationships with diminishing returns.
Injuries (DALYs) show a strong negative relationship with life expectancy.
Unemployment exhibits a nonlinear, complex effect.

## Files
Project-2.ipynb: coding file
Report.pdf: final report with in depth explaination of methods and findings.
life-exp.csv: life expectancy data file
gdp.csv: GDP data file
merged_data.parquet: dataframe life merged data on country exported to parquet
var_imp_plot.png: variable importance plot of features in random forest
pdp_<feature>: partial dependency plots for given feature
