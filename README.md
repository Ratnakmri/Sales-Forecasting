# Sales Forecasting using SARIMA

## 📌 Project Overview

This project focuses on forecasting future sales using historical retail sales data.

The project performs exploratory data analysis, identifies trends and seasonal patterns, and applies a SARIMA time-series forecasting model to predict future sales.

## 🎯 Objective

- Analyze historical sales trends
- Identify monthly sales patterns
- Study seasonality
- Build a time-series forecasting model
- Compare actual sales with forecasted sales
- Evaluate model performance

## 📊 Dataset

The project uses the Superstore retail sales dataset.

The dataset contains information about:

- Order Date
- Sales
- Quantity
- Discount
- Profit
- Category
- Sub-Category
- Region
- Customer information

The dataset is loaded locally in Google Colab.

## 🔧 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Scikit-learn
- Google Colab

## 🔍 Project Workflow

1. Data Loading
2. Data Cleaning
3. Date Conversion
4. Exploratory Data Analysis
5. Monthly Sales Aggregation
6. Trend Analysis
7. Seasonality Analysis
8. Train-Test Split
9. SARIMA Model
10. Sales Forecasting
11. Model Evaluation

## 📈 Exploratory Data Analysis

### Yearly Sales

Sales generally increased over the period from 2014 to 2017.

### Monthly Sales Pattern

The analysis showed noticeable seasonal variations in monthly sales, with stronger sales observed in some months such as September and November.

## 🤖 Model

### SARIMA

A Seasonal ARIMA model was used because the dataset contains monthly observations with seasonal patterns.

Parameters:

- Order: `(1,1,1)`
- Seasonal Order: `(1,1,1,12)`
- Seasonal Period: `12 months`

## 📊 Model Performance

| Metric | Result |
|---|---:|
| MAE | 13,141.30 |
| RMSE | 15,846.78 |

## 📉 Actual vs Forecast

The model forecasts were compared with actual sales values from the test period.

## 💡 Key Insights

- Overall sales showed an increasing trend.
- Sales varied considerably from month to month.
- Seasonal patterns were visible.
- The SARIMA model captured the overall trend and seasonal behavior.
- Forecast errors were higher during some sharp sales peaks.

## 🚀 Future Improvements

- Test different SARIMA parameters
- Compare SARIMA with Prophet
- Try machine-learning forecasting models
- Include promotional information
- Include holidays and external factors
- Perform hyperparameter tuning

