# 📈 Sales Forecasting using SARIMA

## 📌 Project Overview

This project focuses on forecasting future sales using historical retail sales data.

The project performs Exploratory Data Analysis (EDA), identifies sales trends and seasonal patterns, and applies a **SARIMA (Seasonal ARIMA)** time-series forecasting model to predict future monthly sales.

This project was developed as part of an industrial internship project at **Codec Technologies**.

---

## 🎯 Objectives

- Analyze historical sales trends
- Identify monthly sales patterns
- Study seasonality in sales
- Aggregate transaction-level data into monthly sales
- Build a time-series forecasting model
- Forecast future sales
- Compare actual sales with forecasted sales
- Evaluate model performance using MAE and RMSE

---

## 📊 Dataset

The project uses the **Superstore retail sales dataset**.

The dataset contains:

- **9,994 records**
- **21 columns**

Important features include:

| Feature | Description |
|---|---|
| Order Date | Date when the order was placed |
| Ship Date | Date when the order was shipped |
| Ship Mode | Shipping method |
| Customer ID | Unique customer identifier |
| Customer Name | Customer name |
| Segment | Customer segment |
| Region | Sales region |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Product name |
| Sales | Sales amount |
| Quantity | Quantity ordered |
| Discount | Discount applied |
| Profit | Profit generated |

The dataset is included in the `data/` directory.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Scikit-learn
- Google Colab
- GitHub

---

## 🔍 Project Workflow

1. Data Loading
2. Data Cleaning
3. Date Conversion
4. Exploratory Data Analysis
5. Monthly Sales Aggregation
6. Yearly Sales Analysis
7. Seasonality Analysis
8. Train-Test Split
9. SARIMA Model Development
10. Sales Forecasting
11. Model Evaluation
12. Actual vs Forecast Visualization

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

- Loaded the Superstore dataset
- Handled dataset encoding
- Converted `Order Date` into datetime format
- Checked for missing dates
- Removed invalid date records where required
- Converted `Sales` into numeric format
- Aggregated sales by month
- Prepared the data for time-series forecasting

### Date Range

The dataset covers sales from:

**January 2014 to December 2017**

After preprocessing:

- Missing dates: **0**
- Monthly sales data was created for forecasting

---

## 📈 Exploratory Data Analysis

### Yearly Sales Analysis

Yearly sales were analyzed to understand the overall sales trend.

The analysis showed that sales generally increased from **2014 to 2017**, although some yearly variations were observed.

### Monthly Sales Analysis

Monthly sales were aggregated from the transaction-level data to study changes in sales over time.

The monthly sales analysis showed noticeable fluctuations and an overall increasing trend.

### Seasonality Analysis

Monthly sales patterns were analyzed to identify recurring seasonal behavior.

The analysis showed relatively stronger sales activity around **September and November**, while **February** showed comparatively lower sales.

---

## ⏳ Train-Test Split

The monthly sales data was divided chronologically into training and testing datasets.

Approximately:

- **80% → Training Data**
- **20% → Testing Data**

A chronological split was used to ensure that future observations were not used during model training.

---

## 🤖 Forecasting Model

### SARIMA

A **SARIMA (Seasonal Autoregressive Integrated Moving Average)** model was used for sales forecasting.

SARIMA is suitable for time-series data containing trend and seasonal patterns.

### Model Parameters

```text
Order: (1, 1, 1)

Seasonal Order: (1, 1, 1, 12)

Seasonal Period: 12 months
