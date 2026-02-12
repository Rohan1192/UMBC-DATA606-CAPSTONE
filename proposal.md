# 🌍 Air Quality & Pollution Prediction in European Cities  
### A Multi-Output Machine Learning Approach  

**UMBC DATA606 – Data Science Capstone**  
**Author:** RAMIREDDY ROHAN REDDY  
**Instructor:** Dr. Chaojie (Jay) Wang  
**University:** University of Maryland, Baltimore County  

---

## 📌 Project Overview

Air pollution is a critical environmental and public health issue across Europe. Pollutants such as **PM2.5, PM10, NO₂, and O₃** significantly impact air quality and are linked to respiratory and cardiovascular diseases.

This project analyzes historical air quality and meteorological data from multiple European cities and builds machine learning models to predict pollutant levels. A multi-output regression framework is used to forecast multiple pollutants simultaneously.

---

## 🎯 Objectives

- Predict PM2.5, PM10, NO₂, and O₃ levels  
- Identify key meteorological factors influencing pollution  
- Compare multiple machine learning models  
- Analyze city-wise and seasonal pollution patterns  
- Develop a forecasting framework for air quality monitoring  

---

## 🔍 Research Questions

1. Can pollutant levels be accurately predicted using historical air quality and weather data?  
2. Which environmental factors (temperature, humidity, wind speed, pressure) most influence pollution?  
3. How does air pollution vary across European cities?  
4. Do seasonal patterns significantly impact pollutant levels?  

---

## 📊 Dataset Information

### Dataset Description
The dataset contains historical daily air quality and meteorological measurements for multiple European cities.
Link : https://discomap.eea.europa.eu/App/AQViewer/index.html?fqn=Airquality_Dissem.b2g.Measurements
## 📘 Data Dictionary

Each row represents a **daily measurement** of air quality and meteorological conditions for a specific **European city**.

| Column Name   | Data Type    | Definition | Units / Format | Example Values | Role in ML |
|--------------|--------------|------------|----------------|----------------|------------|
| city         | Categorical  | Name of the city where measurements were recorded | Text | Paris, Berlin, London | Feature |
| datetime     | Datetime     | Date/time of observation | YYYY-MM-DD (or YYYY-MM-DD HH:MM) | 2021-06-15 | Feature (after feature engineering) |
| PM2.5        | Numeric      | Fine particulate matter concentration | µg/m³ | 12.4, 35.6 | Target |
| PM10         | Numeric      | Coarse particulate matter concentration | µg/m³ | 18.2, 52.0 | Target |
| NO2          | Numeric      | Nitrogen dioxide concentration | µg/m³ | 22.1, 60.3 | Target |
| O3           | Numeric      | Ozone concentration | µg/m³ | 45.7, 90.2 | Target |
| CO           | Numeric      | Carbon monoxide concentration | mg/m³ | 0.4, 1.2 | Feature |
| SO2          | Numeric      | Sulfur dioxide concentration | µg/m³ | 3.1, 15.0 | Feature |
| temperature  | Numeric      | Air temperature | °C | 12.5, 28.0 | Feature |
| humidity     | Numeric      | Relative humidity | % | 55, 82 | Feature |
| wind_speed   | Numeric      | Wind speed | m/s | 1.5, 6.2 | Feature |
| pressure     | Numeric      | Atmospheric pressure | hPa | 1008, 1023 | Feature |

---

### ✅ Feature Engineering from `datetime` (Derived Columns)

| Derived Column | Data Type | Definition | Example | Role in ML |
|--------------|----------|------------|---------|------------|
| year         | Integer  | Year extracted from datetime | 2021 | Feature |
| month        | Integer  | Month extracted from datetime | 6 | Feature |
| day          | Integer  | Day of month extracted | 15 | Feature |
| day_of_week  | Integer  | Day index (0=Mon … 6=Sun) | 2 | Feature |
| is_weekend   | Boolean  | Weekend indicator | True/False | Feature |
| season       | Categorical | Season derived from month | Winter/Summer | Feature |

### Data Size
- ~1,048,576 records  
- 28 columns  
- ~400 MB (compressed CSV files)  

### Row Representation
Each row represents a daily air quality measurement for a specific city along with associated meteorological conditions.

---

## 🗂 Key Variables

### 🎯 Target Variables
- PM2.5 (Fine particulate matter)  
- PM10 (Coarse particulate matter)  
- NO2 (Nitrogen Dioxide)  
- O3 (Ozone)  

### 📌 Feature Variables
- city  
- datetime  
- temperature  
- humidity  
- wind_speed  
- pressure  
- CO  
- SO2  

---

## ⚙️ Data Preprocessing

- Handling missing values  
- Datetime parsing and feature extraction (year, month, day, season)  
- Encoding categorical variables (city)  
- Feature scaling  
- Optional lag feature engineering for time-based modeling  

---

## 📊 Exploratory Data Analysis

- Pollution trend visualization by city  
- Seasonal variation analysis  
- Correlation heatmaps  
- Distribution analysis of pollutants  
- Feature importance visualization  

---

## 🤖 Machine Learning Models

- Linear Regression (Baseline)  
- Random Forest Regressor  
- Gradient Boosting / XGBoost  
- Multi-Output Regression approach  

---

## 📈 Evaluation Metrics

- Mean Absolute Error (MAE)  
- Root Mean Squared Error (RMSE)  
- R² Score  

---

