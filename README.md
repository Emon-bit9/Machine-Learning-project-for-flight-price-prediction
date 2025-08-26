# Flight ticket Price Prediction

Machine learning project to predict flight ticket prices based on various features.

## Overview

This project analyzes flight data to build a predictive model that estimates ticket prices based on features like airline, date, route, duration, and stops.

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

- Enhanced regularization parameters
- Feature selection to reduce dimensionality
- Ensemble methods with different model types
- More sophisticated encoding for categorical variables
- External data integration (holidays, weather, etc.)
- Advanced cross-validation techniques
