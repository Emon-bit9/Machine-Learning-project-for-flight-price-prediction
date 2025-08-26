# Flight ticket Price Prediction

Machine learning project to predict flight ticket prices based on various features.

## Overview

This project analyzes flight data to build a predictive model that estimates ticket prices based on features like airline, date, route, duration and stops. The project implements data preprocessing including feature engineering, categorical encoding and derived attribute extraction from temporal data. Two main regression models were developed and evaluated: **Linear Regression** and **Random Forest Regressor**. Through hyperparameter optimization, the Random Forest model achieved superior performance with 90.36% R² score on test data. The final model can capture complex price patterns and provides accurate predictions across different flight categories, with flight duration and airline being the most influential factors in price determination.

## Dataset

- **Training data**: 10,682 records with labeled prices
- **Test data**: 2,671 records for prediction
- **Features**: Airline, Date, Source, Destination, Route, Time, Duration, Stops

## Results

- **Best Model**: Random Forest Regressor (optimized)
- **R² Score**: 0.9036 on test data
- **RMSE**: 1,441
- **MAE**: 640

## Key Findings

- Most important features:
  1. Flight duration (36.9%)
  2. Airline (20.8%)
  3. Journey day (8.4%)
  4. Duration hours (7.6%)
  5. Additional information (5.8%)
  
- Price ranges from ₹1,968 to ₹59,892 (predicted)
- Business class flights show highest prices
- Non-stop flights typically cost less than flights with stops


## Tech Stack

- Python 
- pandas, numpy (data manipulation)
- matplotlib, seaborn (visualization)
- scikit-learn (machine learning)
- Jupyter Notebook (development environment)

## Potential Improvements

The model shows signs of overfitting with high training R² (0.9816) compared to testing R² (0.9036). Future improvements could include:

- **Regularization**: Increase min_samples_leaf (5-10) and reduce max_depth in Random Forest
- **Feature Selection**: Remove low-importance features (< 1%) based on the feature importance analysis
- **Gradient Boosting**: Try XGBoost or LightGBM with early stopping to prevent overfitting
- **Cross-validation**: Implement time-based splits for temporal flight data
- **Ensemble Strategy**: Blend predictions from diverse models (RF, XGBoost, Linear models)
- **Data Augmentation**: Generate synthetic samples for underrepresented price ranges
