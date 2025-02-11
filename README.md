# Car Price Prediction Model 🚗💰

## Overview
This project is a **car price prediction model** built using **Linear Regression and Random Forest**. The goal was to predict the price of a car based on features such as mileage, engine size, car age, and other categorical attributes like brand, fuel type, and transmission.

## Dataset 📊
The dataset used for this project is publicly available on Kaggle:
[Car Price Dataset](https://www.kaggle.com/datasets/asinow/car-price-dataset)

### Features:
- **Price** (Target variable)
- **Year** (Converted to Car Age)
- **Mileage**
- **Engine Size**
- **Transmission** (One-hot encoded)
- **Fuel Type** (One-hot encoded)
- **Brand** (One-hot encoded)
- **Derived Features** (Luxury Car, High Mileage, Price per Liter, etc.)

## Steps & Approach 🛠️
1. **Data Cleaning:**
   - Checked for null values (None found ✅)
   - Converted `Year` into `Car Age`
   - Removed duplicates (None found ✅)

2. **Exploratory Data Analysis (EDA):**
   - Price distribution was **slightly left-skewed**
   - **Negative correlation** between mileage and price
   - **Positive correlation** between car age and price (older cars are cheaper)

3. **Feature Engineering:**
   - Created new features such as **Luxury Car, High Mileage, Price per Liter**
   - One-hot encoded categorical variables
   - Removed features causing multicollinearity

4. **Model Training & Evaluation:**
   - **Linear Regression** (Initial Model):
     - R²: **0.88**
     - MSE: **1,137,718.10**
   - **Random Forest (Final Model):**
     - R²: **0.99**
     - RMSE: **318.84**

## Results 🚀
- The **Random Forest model performed best** with an R² of **0.99** and RMSE of **318.84**.
- Linear Regression overfitted after feature engineering, so we removed redundant features.

## Lessons Learned 📌
- **Check feature correlations carefully** to avoid data leakage.
- **An R² of 1.00 usually means you did something wrong.**
- **Feature engineering can improve results, but overdoing it can cause overfitting.**

## Future Improvements 🏗️
- Try **time-series forecasting** for price trends
- Use **XGBoost** for better performance
- Deploy the model with a **Flask or FastAPI web app**

## Contributing 🤝
If you have suggestions or improvements, feel free to fork this repo and submit a pull request!
