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

