# 🌍 Air Quality & Pollution Prediction in European Cities
### A Multi-Output Machine Learning Approach
**UMBC DATA606 – Data Science Capstone**

**Author:**   RAMIREDDY ROHAN REDDY  
**Instructor:** Dr. Chaojie (Jay) Wang  
**University:** University of Maryland, Baltimore County  

---

## 📌 Project Overview

Air pollution is one of the most critical environmental and public health challenges worldwide. Pollutants such as **PM2.5, PM10, NO₂, and O₃** significantly impact air quality and are associated with respiratory diseases, cardiovascular problems, and environmental degradation.

This project develops a machine learning framework for predicting pollutant concentrations across European cities using historical air quality and meteorological data. A **multi-output regression approach** is used to predict multiple pollutants simultaneously.

The project includes:

- Data preprocessing
- Feature engineering
- Exploratory Data Analysis (EDA)
- Machine Learning modeling
- Model evaluation
- Air quality forecasting

---

## 🎯 Objectives

The primary objectives of this project are:

✔ Predict PM2.5, PM10, NO₂, and O₃ levels simultaneously  

✔ Identify important weather factors affecting pollution  

✔ Analyze seasonal and city-wise pollution trends  

✔ Compare multiple machine learning models  

✔ Build an air quality forecasting framework  

---

## 🔍 Research Questions

This project aims to answer the following questions:

1. Can pollutant levels be accurately predicted using historical weather and air quality data?

2. Which environmental variables most influence pollution levels?

3. How does air pollution vary across cities?

4. Do seasonal changes significantly impact pollutant concentrations?

---

## 📊 Dataset Information

### Dataset Source

European Environment Agency (EEA)

Dataset Link:

https://discomap.eea.europa.eu/App/AQViewer/index.html?fqn=Airquality_Dissem.b2g.Measurements

---

### Dataset Summary

| Metric | Value |
|----------|--------|
| Total Records | 1,048,576 |
| Total Columns | 24 |
| Date Range | 2000–2010 |
| Data Size | ~400 MB |
| Observation Type | Daily measurements |

---

## 📘 Data Dictionary

### 🎯 Target Variables

- PM2.5 → Fine particulate matter
- PM10 → Coarse particulate matter
- NO₂ → Nitrogen dioxide
- O₃ → Ozone

### 📌 Feature Variables

- City
- Datetime
- Temperature
- Humidity
- Wind Speed
- Pressure
- CO
- SO₂

---

## ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

### Missing Value Handling

Missing values identified:

| Column | Missing Values |
|----------|----------------|
| CO_AQI | 524,224 |
| SO2_AQI | 524,487 |
| Other Numeric Features | ≤1 |

Techniques used:

- Median imputation
- Mode imputation
- Null value removal where necessary

---

### Data Cleaning

Data cleaning operations:

- Removed unnecessary columns
- Standardized column names
- Converted dates into datetime format
- Removed duplicate records

Duplicate rows removed:

**2,407**

---

## ⚙️ Feature Engineering

Features extracted from datetime:

- Year
- Month
- Day
- Day of Week
- Weekend Indicator
- Season

### Season Categories

| Months | Season |
|----------|----------|
| Dec–Feb | Winter |
| Mar–May | Spring |
| Jun–Aug | Summer |
| Sep–Nov | Autumn |

---

## 📊 Exploratory Data Analysis (EDA)

EDA techniques performed:

### Distribution Analysis

Visualizations:

- Histograms
- Boxplots
- Density plots

Purpose:

- Understand data distribution
- Detect skewness
- Identify outliers

---

### Correlation Analysis

Top correlations with O₃ AQI:

| Variable | Correlation |
|------------|-------------|
| O3_Mean | 0.77 |
| SO2_AQI | 0.08 |
| NO2_AQI | 0.06 |
| SO2_Mean | 0.03 |
| CO_AQI | -0.13 |

Observations:

- O3_Mean had the strongest relationship with O3_AQI
- CO_AQI showed slight negative correlation

---

### Outlier Detection

| Variable | Outliers |
|------------|-----------|
| SO2_Mean | 69,125 |
| O3_AQI | 67,264 |
| CO_Mean | 56,414 |
| SO2_AQI | 45,461 |
| CO_AQI | 27,753 |
| NO2_Mean | 27,190 |
| NO2_AQI | 16,250 |
| O3_Mean | 4,584 |

---

## 📈 Key Findings

Key observations obtained from analysis:

- Dataset contains over **1 million records**
- Missing values are concentrated in **CO_AQI and SO2_AQI**
- Ozone levels show strong seasonal patterns
- Pollution variables exhibit right-skewed distributions
- Southwestern cities displayed elevated ozone values

Highest average O₃ cities:

- Capitan
- Boulder City
- Ponca City

---

## 🤖 Machine Learning Models

Models implemented:

### Linear Regression

Purpose:

- Baseline prediction model

Advantages:

- Simple
- Fast training
- Easy interpretation

---

### Random Forest Regressor

Purpose:

- Capture nonlinear relationships

Advantages:

- Robust performance
- Handles large datasets
- Provides feature importance

---

### Multi-Output Regression

Predicted pollutants:

- PM2.5
- PM10
- NO₂
- O₃

---

## 📈 Model Evaluation Metrics

Performance metrics used:

### Mean Absolute Error (MAE)

Measures average prediction error.

### Root Mean Square Error (RMSE)

Measures prediction deviation.

### R² Score

Measures model fit:

- 0 → Poor fit
- 1 → Perfect fit

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- Jupyter Notebook

---

## 📂 Project Structure

```bash
Air-Quality-Prediction/
│
├── data/
│   ├── raw_data.csv
│   ├── processed_data.csv
│
├── notebooks/
│   ├── Final.ipynb
│
├── models/
│   ├── air_quality_model.pkl
│
├── images/
│   ├── heatmap.png
│   ├── pollution_trends.png
│
├── README.md
│
└── requirements.txt
```

---

## 🚀 Future Improvements

Future enhancements include:

- Real-time API integration
- LSTM-based forecasting
- Streamlit dashboard
- Interactive geospatial visualization
- Real-time pollution prediction system

---

## 📚 References

European Environment Agency Dataset

https://discomap.eea.europa.eu/App/AQViewer/index.html?fqn=Airquality_Dissem.b2g.Measurements

Python Libraries:

- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- XGBoost

---

## ⭐ Project Outcome

This project demonstrates how machine learning can be used to analyze environmental data and predict pollution levels effectively. The framework provides valuable insights that can help policymakers, researchers, and environmental agencies improve air quality monitoring and public health initiatives.
