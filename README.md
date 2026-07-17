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

---

# Project Workflow

The project follows a structured Machine Learning workflow from raw data to business insights.

```text
                Raw Dataset
                     │
                     ▼
            Data Understanding
                     │
                     ▼
              Data Cleaning
                     │
                     ▼
        Exploratory Data Analysis
                     │
                     ▼
          Feature Engineering
                     │
                     ▼
          Data Preprocessing
                     │
                     ▼
          Train-Test Split
                     │
                     ▼
        Regression Model Training
                     │
                     ▼
       Hyperparameter Tuning
                     │
                     ▼
         Model Evaluation
                     │
                     ▼
        SHAP Explainability
                     │
                     ▼
      Interactive Plotly Dashboard
                     │
                     ▼
         Business Recommendations
```

---

# Data Preprocessing

The following preprocessing steps were performed before training the machine learning models:

- Removed duplicate records (if present)
- Checked for missing values
- Identified numerical and categorical features
- Applied One-Hot Encoding to categorical features
- Standardized numerical features where appropriate
- Created a preprocessing pipeline using `ColumnTransformer`
- Combined preprocessing and model training using Scikit-learn `Pipeline`

---

# Exploratory Data Analysis (EDA)

EDA was performed to better understand the dataset and identify relationships between variables.

The following visualizations were created:

- Dataset overview
- Missing value analysis
- Distribution of CO₂ emissions
- Vehicle class distribution
- Fuel type distribution
- Correlation heatmap
- Feature relationships
- Engine size vs CO₂ emissions
- Fuel consumption vs CO₂ emissions

Key findings from EDA:

- Fuel Consumption (Combined) has the strongest relationship with CO₂ emissions.
- Larger engine sizes generally produce higher CO₂ emissions.
- Vehicles with more cylinders tend to emit more CO₂.
- Fuel consumption is the primary driver of vehicle emissions.

---

# Feature Engineering

The following features were used for model development:

### Numerical Features

- Engine Size (L)
- Cylinders
- Fuel Consumption City (L/100 km)
- Fuel Consumption Highway (L/100 km)
- Fuel Consumption Combined (L/100 km)
- Fuel Consumption Combined (MPG)

### Categorical Features

- Make
- Model
- Vehicle Class
- Transmission
- Fuel Type

### Target Variable

- CO₂ Emissions (g/km)

---

# Machine Learning Models Evaluated

The following regression algorithms were evaluated during model selection:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regressor
- Random Forest Regressor
- Extra Trees Regressor
- Gradient Boosting Regressor
- AdaBoost Regressor
- XGBoost Regressor
- CatBoost Regressor

Hyperparameter tuning was performed on the best-performing models using GridSearchCV to identify the optimal configuration.
