# Walmart Sales Forecasting Project

This project analyzes Walmart weekly sales data and applies both regression analysis and time series forecasting methods to understand sales patterns and predict future performance.

## Project Overview

The goal of this project is to explore the factors that may influence Walmart's weekly sales and to compare different analytical approaches for forecasting sales performance.

The project is divided into four main parts:

1. Data preprocessing and exploratory data analysis (EDA)
2. Regression model analysis
3. Time series analysis using ARIMA
4. Model evaluation and conclusion

## Dataset

- **Source:** Kaggle - Walmart Dataset
- **Link:** https://www.kaggle.com/datasets/yasserh/walmart-dataset

### Main Variables

- `Store`: Store ID
- `Date`: Week of sales
- `Weekly_Sales`: Weekly sales amount
- `Holiday_Flag`: Whether the week includes a holiday
- `Temperature`: Average temperature
- `Fuel_Price`: Fuel price
- `CPI`: Consumer Price Index
- `Unemployment`: Unemployment rate

## Project Content

### 1. Data Preprocessing
- Loaded the Walmart dataset
- Converted the `Date` column into datetime format
- Checked dataset structure and descriptive statistics
- Confirmed there were no missing values

### 2. Feature Engineering
To improve model performance, additional time-related features were extracted from the `Date` column, including:
- Year
- Month
- Week number

### 3. Exploratory Data Analysis (EDA)
- Correlation heatmap
- Sales trend visualization over time
- Interpretation of relationships between sales and other variables

### 4. Regression Analysis
A linear regression model was built to examine how different variables affect weekly sales.

#### Regression Model Evaluation
- **RMSE:** 521,583.50
- **R²:** 0.1555

#### Feature Coefficient Highlights
Based on the regression coefficients:
- `Month` had a positive influence on weekly sales
- `Fuel_Price` and `Holiday_Flag` also showed positive effects
- `Store`, `Week`, `CPI`, and `Unemployment` had negative coefficients

### 5. Time Series Analysis
A time series model was built using ARIMA to forecast total Walmart sales.

Steps included:
- Aggregating total weekly sales by date
- Performing an ADF test for stationarity
- Plotting ACF and PACF
- Building an ARIMA(1, 0, 1) model
- Forecasting future sales

#### Time Series Model Evaluation
- **RMSE:** 1,367,365.28
- **MAPE:** 2.68%

## Tools and Libraries

- Python
- Google Colab
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels
- opendatasets
