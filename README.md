# Car Price Prediction Pipeline (Databricks + PySpark)

## Project Overview

This project presents an end-to-end data processing and machine learning pipeline built using **PySpark in Databricks**.
The goal was to analyze car sales data and develop a model to predict car selling prices based on key features.

---

## Objectives

* Perform exploratory data analysis (EDA) to understand relationships between variables
* Build a scalable data pipeline using PySpark
* Engineer meaningful features for modeling
* Train and evaluate machine learning models
* Compare model performance and draw insights

---

## Technologies Used

* PySpark
* Databricks
* Python

---

## Dataset Description

The dataset contains information about used cars, including:

* `Car_Name` – model of the car
* `Year` – manufacturing year
* `Selling_Price` – target variable (price to predict)
* `Present_Price` – current market price of the car
* `Kms_Driven` – mileage
* `Fuel_Type` – petrol/diesel
* `Seller_Type` – dealer or individual
* `Transmission` – manual/automatic
* `Owner` – number of previous owners

---

## Exploratory Data Analysis (EDA)

Initial analysis showed:

* Strong positive correlation between **Present Price** and **Selling Price**
* Negative relationship between **car age** and selling price
* Differences in price distribution across fuel types

These insights guided feature selection for the model.

---

## Data Pipeline

The pipeline includes:

1. **Data Loading** – reading data from Databricks tables
2. **Data Cleaning** – removing missing values
3. **Feature Engineering**:

   * Created `car_age` from manufacturing year
4. **Feature Transformation**:

   * Encoding categorical variables using StringIndexer
   * Combining features using VectorAssembler

---

## Machine Learning Models

### 🔹 Linear Regression

* Achieved **R² ≈ 0.81**
* Demonstrated strong performance due to linear relationships in data

### 🔹 Random Forest

* Lower performance compared to linear regression
* Highlighted importance of model selection based on data characteristics

---

## Model Evaluation

Models were evaluated using:

* **R² (coefficient of determination)**
* **RMSE (Root Mean Squared Error)**

The final model showed good predictive performance and generalization.

---

## Key Insights

* **Present Price** is the most important predictor of selling price
* Car value decreases with age
* Simpler models (Linear Regression) can outperform complex ones when relationships are linear
* Feature selection has a significant impact on model performance

---

## Project Structure

```
├── car_price_prediction.ipynb
├── README.md
```

---

## Future Improvements

* Add more advanced feature engineering
* Tune hyperparameters for better model performance
* Deploy model as an API
* Integrate with cloud services (e.g., Azure Databricks)

---

## Author

Project created as part of hands-on learning in data engineering and machine learning using PySpark and Databricks.

