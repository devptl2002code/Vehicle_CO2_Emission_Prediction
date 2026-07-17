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

---

# Model Performance

After evaluating multiple regression algorithms, **Random Forest Regressor** achieved the best overall performance and was selected as the final model.

## Final Model Performance

| Metric | Value |
|---------|------:|
| Best Model | Random Forest Regressor |
| R² Score | **0.9957** |
| MAE | **2.17** |
| RMSE | **3.94** |
| Cross Validation R² | **0.9970** |
| Training Time | **60.42 sec** |
| Prediction Time | **0.125 sec** |

---

# Model Comparison

Multiple regression algorithms were evaluated before selecting the final model.

| Model | Status |
|--------|--------|
| Linear Regression | Evaluated |
| Ridge Regression | Evaluated |
| Lasso Regression | Evaluated |
| Decision Tree Regressor | Evaluated |
| Random Forest Regressor | **Selected** |
| Extra Trees Regressor | Evaluated |
| Gradient Boosting Regressor | Evaluated |
| AdaBoost Regressor | Evaluated |
| XGBoost Regressor | Evaluated |
| CatBoost Regressor | Evaluated |

Random Forest Regressor demonstrated the best balance between prediction accuracy and model stability.

---

# Model Validation

The final model was validated using multiple evaluation techniques.

- Train/Test Split
- 5-Fold Cross Validation
- Overfitting Analysis
- Residual Analysis
- SHAP Explainability

### Cross Validation Results

- Average R² Score: **0.9970**
- Standard Deviation: **0.0006**

### Generalization Check

| Metric | Value |
|---------|------:|
| Training R² | 0.9995 |
| Testing R² | 0.9957 |
| Difference | 0.0038 |

The small difference between training and testing performance indicates that the model generalizes well and does not exhibit significant overfitting.

---

# Dashboard

An interactive Plotly dashboard was developed to visualize model performance and predictions.

The dashboard includes:

- Model Performance Metrics
- Model Comparison
- Actual vs Predicted Values
- Residual Analysis
- Feature Importance

### Dashboard Preview

<img width="2476" height="494" alt="image" src="https://github.com/user-attachments/assets/b74ba229-888b-4a3e-a4f6-156d60109bad" />

---

# Visualizations

The project includes several visualizations for exploratory analysis and model evaluation.

| Visualization | Purpose |
|--------------|---------|
| Distribution Plots | Understand feature distributions |
| Correlation Heatmap | Identify feature relationships |
| Actual vs Predicted | Evaluate prediction accuracy |
| Residual Plot | Analyze prediction errors |
| Feature Importance | Identify influential variables |
| SHAP Summary Plot | Explain model predictions |

Example image references:

<img width="1400" height="900" alt="dashboard" src="https://github.com/user-attachments/assets/c835e058-024a-4c8c-b389-40aadd0ef5b4" />


---

# Business Insights

The analysis indicates that fuel consumption and engine characteristics are the primary factors influencing vehicle CO₂ emissions.

The developed model can support:

- Vehicle manufacturers during design optimization.
- Environmental agencies in preliminary emission assessment.
- Consumers comparing environmental impact across vehicle types.
- Sustainability initiatives through data-driven emission estimation.


---

# Project Structure

```text
Vehicle_CO2_Emission_Prediction/
│
├── Vehicle_CO2_Emission_Prediction.ipynb
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
├── co2.csv
│
├── images/
│   ├── dashboard.png
│
└── artifacts/
    └── vehicle_co2_prediction_model.pkl
```

---

# Installation

## Clone the Repository

```bash
git clone https://github.com/devptl2002code/Vehicle_CO2_Emission_Prediction.git
```

## Navigate to the Project

```bash
cd Vehicle_CO2_Emission_Prediction
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# How to Run

1. Clone or download this repository.
2. Install the required Python packages using `requirements.txt`.
3. Open the notebook in Google Colab or Jupyter Notebook.
4. Place the dataset (`co2.csv`) in the project directory (or update the file path if needed).
5. Run all notebook cells from top to bottom.
6. Review the evaluation metrics, SHAP explainability, and Plotly dashboard.

---

# Results Summary

- Best Model: **Random Forest Regressor**
- R² Score: **0.9957**
- MAE: **2.17**
- RMSE: **3.94**
- Cross Validation R²: **0.9970**
- Model demonstrated excellent generalization with minimal overfitting.
- SHAP explainability identified fuel consumption and engine characteristics as the most influential features.

---

# Limitations

- The dataset contains approximately **6,282 vehicle records**, which is smaller than the recommended 10,000+ records for this capstone guideline.
- Predictions are limited to the vehicle categories represented in the dataset.
- Driving behavior, weather conditions, road conditions, and vehicle maintenance are not considered.
- The model should be used as a decision-support tool and not as a replacement for official emissions testing.

---

# Future Improvements

- Train the model with a larger and more recent dataset.
- Include hybrid and electric vehicle data.
- Evaluate additional ensemble and deep learning models.
- Deploy the model as a web application using Streamlit or Flask.
- Expose the trained model through a REST API.
- Automate model retraining with updated datasets.

---

# Repository Contents

- End-to-end Machine Learning workflow
- Data preprocessing pipeline
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model comparison
- Hyperparameter tuning
- Model evaluation
- SHAP explainability
- Interactive Plotly dashboard
- Business insights and recommendations

---

# Author

**Dev Patel**

GitHub: https://github.com/devptl2002code

---

# License

This project is licensed under the MIT License. See the `LICENSE` file for details.
