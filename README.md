# Vehicle CO₂ Emission Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Plotly](https://img.shields.io/badge/Plotly-Dashboard-blueviolet)
![SHAP](https://img.shields.io/badge/SHAP-Explainable%20AI-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Project Overview

This project develops an end-to-end Machine Learning solution to predict vehicle CO₂ emissions using vehicle specifications and fuel consumption data. The workflow includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, hyperparameter tuning, model evaluation, explainable AI using SHAP, and an interactive Plotly dashboard.

The final model enables accurate estimation of vehicle CO₂ emissions and demonstrates a complete regression-based machine learning pipeline suitable for portfolio projects and educational purposes.

---

# Business Problem

Vehicle manufacturers and environmental agencies need reliable methods to estimate CO₂ emissions before vehicles enter production. Manual estimation is time-consuming and expensive.

This project builds a predictive machine learning model that estimates vehicle CO₂ emissions based on vehicle specifications, enabling faster decision-making and supporting environmental compliance.

---

# Project Objectives

- Predict vehicle CO₂ emissions using supervised machine learning.
- Compare multiple regression algorithms.
- Identify the best-performing regression model.
- Perform feature engineering and preprocessing.
- Explain model predictions using SHAP.
- Visualize results through an interactive Plotly dashboard.
- Provide business insights and recommendations.

---

# Dataset Information

**Dataset Name**

Canadian Vehicle CO₂ Emissions Dataset

**Source**

Kaggle

**Records**

- 6,282 Vehicles

**Target Variable**

- CO₂ Emissions (g/km)

**Features**

- Make
- Model
- Vehicle Class
- Engine Size
- Cylinders
- Transmission
- Fuel Type
- Fuel Consumption (City)
- Fuel Consumption (Highway)
- Fuel Consumption (Combined)
- Fuel Consumption (MPG)

---

# Technologies Used

| Category | Technology |
|----------|------------|
| Language | Python |
| Notebook | Google Colab |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Plotly |
| Machine Learning | Scikit-Learn |
| Explainable AI | SHAP |
| Hyperparameter Tuning | GridSearchCV |
