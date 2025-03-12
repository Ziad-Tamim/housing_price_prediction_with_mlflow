# Median House Price Prediction with Scikit-Learn

![california_housing_prices_plot](https://github.com/user-attachments/assets/78d8739b-f4ba-4491-a365-e03a326242f1)

This project demonstrates an end-to-end Machine Learning pipeline to predict median house prices in California using census data. The goal is to provide a reliable, scalable solution for real-estate pricing that outperforms manual estimates.


## Overview
- **Data Collection & Cleaning**: Used California census data (1990) and handled missing values.
- **Exploratory Analysis & Visualization**: Identified correlations and feature distributions.
- **Feature Engineering**: Created new features (ratios, cluster similarities) and performed transformations (log scaling, standardization).
- **Model Training & Selection**: Evaluated Linear Regression, Decision Trees, and Random Forests using cross-validation.
- **Hyperparameter Tuning**: Optimized parameters via GridSearchCV and RandomizedSearchCV.
- **Deployment & Monitoring**: Saved final model with joblib; emphasized continuous monitoring and retraining.

## Results

| Model             | Method                    | RMSE (Cross-Validation) |
| ----------------- | ------------------------- | ----------------------- |
| Linear Regression | Basic Training            | ~68,687                 |
| Decision Tree     | Cross-validation          | ~66,868                 |
| Random Forest     | Cross-validation & Tuning | ~41,000 - 43,000        |

Random Forest emerged as the best model, significantly reducing errors compared to simpler models.

## Metrics
- **RMSE**: Prioritizes avoiding large errors.
- **MAE**: Provides average magnitude of errors, less sensitive to outliers.

## Project Structure
- **Data Acquisition**: Census data CSV.
- **Preprocessing Pipeline**: Scikit-Learn (Pipelines, Imputation, Encoding).
- **Modeling & Tuning**: GridSearchCV, RandomizedSearchCV.
- **Deployment**: Model serialization with joblib.

## Features
- longitude (float)
- latitude (float)
- housing_median_age (float)
- total_rooms (float)
- total_bedrooms (float)
- population (float)
- households (float)
- median_income (float)
- ocean_proximity (categorical; e.g., "INLAND", "NEAR BAY", etc.)

## Target
- median_house_value (float)

## Skills & Tools Used
- **Python Programming & Data Handling**: Proficiency with Python and libraries like NumPy, Pandas, Matplotlib (or similar) is key for data loading, manipulation, and visualization.
- **Machine Learning Fundamentals**: Understanding supervised learning (especially regression), model evaluation (train/test splits, cross-validation), and performance metrics (RMSE, MAE) is critical.
- **Data Preprocessing & Wrangling**: Skills in dealing with missing values, outliers, data transformations (log-scaling heavy-tailed distributions, feature scaling, encoding categorical variables, etc.).
- **Feature Engineering**: Ability to create meaningful new features (e.g., ratios like rooms_per_house, or engineered similarity features like cluster centers) to improve model performance.
- **Scikit-Learn Workflows**: Familiarity with Scikit-Learn’s pipelines, transformers (e.g., SimpleImputer, StandardScaler, OneHotEncoder), and model selection tools (GridSearchCV, RandomizedSearchCV).
- **Model Deployment & Maintenance**: Basic knowledge of how to save a model (using joblib) for production, monitor its performance over time, and implement an automated pipeline for retraining if needed.
- **MLflow**: Model tracking and versioning
- **DVC**: Data tracking and version control
