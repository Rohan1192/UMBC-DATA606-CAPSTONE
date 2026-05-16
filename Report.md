# 🌍 Air Quality & Pollution Prediction in European Cities
### A Multi-Output Machine Learning Approach
**UMBC DATA606 – Data Science Capstone**

**Author:** RAMIREDDY ROHAN REDDY 
**Instructor:** Dr. Chaojie (Jay) Wang  
**University:** University of Maryland, Baltimore County  

---

## 📌 Project Overview

Air pollution is one of the major environmental challenges affecting both public health and environmental sustainability. Pollutants such as **PM2.5, PM10, NO₂, and O₃** significantly affect air quality and are associated with respiratory diseases and environmental degradation.

This project develops a machine learning framework for predicting pollutant concentrations across European cities using historical air quality and meteorological data. Multiple machine learning algorithms are implemented and compared under a **multi-output regression framework**.

The project workflow includes:

✔ Data preprocessing  
✔ Feature engineering  
✔ Exploratory Data Analysis (EDA)  
✔ Machine learning modeling  
✔ Performance evaluation  
✔ Interactive prediction application  

---

## 🎯 Objectives

- Predict **PM2.5, PM10, NO₂, and O₃** simultaneously
- Identify important weather factors affecting pollution
- Analyze seasonal pollution patterns
- Compare machine learning algorithms
- Develop an air quality forecasting framework

---

## 🔍 Research Questions

1. Can pollutant concentrations be accurately predicted using weather and historical pollution data?

2. Which environmental variables significantly influence pollution levels?

3. How does pollution vary across different cities?

4. Do seasonal patterns affect pollutant concentrations?

---

## 📊 Dataset Information

### Dataset Source

European Environment Agency (EEA)

https://discomap.eea.europa.eu/App/AQViewer/index.html?fqn=Airquality_Dissem.b2g.Measurements

### Dataset Summary

| Metric | Value |
|----------|--------|
| Records | 1,048,576 |
| Columns | 24 |
| Date Range | 2000–2010 |
| Dataset Size | ~400 MB |
| Observation Type | Daily Measurements |

---

## 📘 Features Used

### Target Variables

- PM2.5
- PM10
- NO₂
- O₃

### Input Features

- Temperature
- Relative Humidity
- Wind Speed
- Pressure
- CO
- SO₂
- Year
- Month
- Day
- Day of Week
- Weekend Indicator

---

## ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

- Missing value handling
- Duplicate removal
- Date conversion
- Feature engineering
- Feature scaling
- Outlier treatment

### Missing Values

| Variable | Missing Values |
|-----------|----------------|
| CO_AQI | 524,224 |
| SO2_AQI | 524,487 |

Duplicate rows removed:

**2,407**

---

## ⚙️ Feature Engineering

The datetime field was transformed into:

- Year
- Month
- Day
- Day of Week
- Weekend Indicator
- Season

Season categories:

| Months | Season |
|----------|---------|
| Dec–Feb | Winter |
| Mar–May | Spring |
| Jun–Aug | Summer |
| Sep–Nov | Autumn |

---

## 📊 Exploratory Data Analysis

EDA was performed to understand data patterns and variable relationships.

### Correlation Heatmap

The heatmap shows relationships among pollutants and environmental variables.

<img width="1018" height="791" alt="image" src="https://github.com/user-attachments/assets/422e63fc-098e-4894-999c-2dfa67b1accb" />


**Observations:**

- PM10 and PM2.5 exhibit strong positive correlation
- Temperature and Dewpoint Temperature show high correlation
- Relative Humidity demonstrates negative correlation with temperature
- Weather variables influence pollutant behavior

---

## 🤖 Machine Learning Models

The following models were implemented:

### Linear Regression

Purpose:

- Baseline prediction model

Advantages:

- Fast computation
- Easy interpretation

---

### Random Forest Regressor

Purpose:

- Capture nonlinear relationships

Advantages:

- Better prediction accuracy
- Handles large datasets

---

### XGBoost

Purpose:

- Improve prediction performance

Advantages:

- Strong predictive capability
- Reduces overfitting

---

## 📈 Model Performance Comparison

Performance metrics:

- R² Score
- MAE
- RMSE

<img width="1189" height="590" alt="image" src="https://github.com/user-attachments/assets/027fb840-7f8e-42b4-962f-3f83a36405ee" />


### Results

| Model | R² Score | MAE | RMSE |
|---------|-----------|------|-------|
| Linear Regression | ~0.10 | 8.4 | 10.5 |
| Random Forest | ~0.50 | 5.6 | 7.9 |
| XGBoost | ~0.52 | 5.8 | 7.7 |

### Key Findings

✔ Linear Regression showed weak prediction capability

✔ Random Forest improved performance significantly

✔ XGBoost achieved the best prediction performance

---

## 🌐 Air Quality Prediction Application

An interactive web application was developed for real-time predictions.

### Application Interface

<img width="1919" height="885" alt="image" src="https://github.com/user-attachments/assets/31e32f40-667f-4103-80d2-f855a4fae9c5" />


### Features

Users can provide:

- Temperature
- Relative Humidity
- Year
- Month
- Day
- Day of Week
- Weekend Indicator

The application dynamically displays:

- Input summary
- Weather information
- Predicted pollution values

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Matplotlib
- Seaborn
- Streamlit
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
├── images/
│   ├── correlation_heatmap.png
│   ├── model_comparison.png
│   ├── air_quality_app.png
│
├── models/
│   ├── air_quality_model.pkl
│
├── README.md
│
└── requirements.txt
```

---

## 🚀 Future Improvements

Future enhancements include:

- Real-time API integration
- LSTM-based prediction
- Streamlit cloud deployment
- Geospatial visualization
- Mobile application development

---

## ⭐ Conclusion

This project demonstrates how machine learning techniques can be used to predict air quality levels using historical environmental data. Results show that weather and environmental variables strongly affect pollution concentrations.

Among the evaluated models, **XGBoost achieved the best overall prediction performance**, making it suitable for future real-time air quality forecasting systems.
