# Power_Consumption_Prediction
A machine learning project to predict power consumption using environmental and meteorological features.

# ⚡ Optimize Zone 1 Power Consumption – Wellington, New Zealand

## 📌 Project Overview

The purpose of this project is to develop and demonstrate a machine learning model that accurately **predicts power consumption in Zone 1 in Wellington** based on a range of environmental and meteorological factors. By analyzing historical data—including temperature, humidity, wind speed, solar flows, air quality, and cloudiness—the project aims to provide insights for more efficient energy planning and usage in the region.

## 🎯 Objective

- **Collect and preprocess** key meteorological and environmental data affecting power usage.
- **Analyze** relationships between weather features and electricity consumption using Exploratory Data Analysis (EDA).
- **Identify and address** multicollinearity among predictors to ensure robust modeling.
- **Build and validate** predictive models (e.g., regression or machine learning algorithms) to forecast power consumption.
- **Demonstrate model performance** using relevant metrics and visualizations.
- **Provide actionable insights** that help utilities or organizations anticipate and optimize energy demand based on changing environmental conditions.

## 📊 Dataset Summary

- **Region:** Zone 1 – Wellington, New Zealand
- **Target Variable:** Power consumption in Zone A
- **Independent Variables:**  
  - Wind Speed
  - Temperature
  - Humidity
  - General Diffuse Flows  
  - Diffuse Flows  
  - Air Quality Index (PM)  
  - Cloudiness
  - The dataset includes:

- **Observation Count:** 52,584 rows  
- **Tools Used:** Python, Pandas, Matplotlib, Seaborn, Scikit-learn, XGBoost

---

## 🧪 Workflow

### ✅ Step 1: Importing Required Libraries  
Standard ML libraries and visualization tools (NumPy, pandas, matplotlib, seaborn, sklearn, xgboost)

### ✅ Step 2: Data Loading  
Loaded environmental and power consumption data from CSV files.

### ✅ Step 3: Exploratory Data Analysis (EDA)  
- Wind Speed: Right-skewed distribution with outliers  
- Diffuse Flows & General Diffuse Flows: High skewness and outliers  
- Air Quality Index (PM): Nearly constant  
- Cloudiness: Binary variable (mostly zero)  
- Target (Power Consumption): Widely spread with values from ~8000 to ~52000  

### ✅ Step 4: Feature Engineering  
- Treated missing values  
- Detected and capped outliers using IQR  
- Scaled features using StandardScaler  
  
### ✅ Step 5: Model Building  
Trained multiple regression models:
- Linear Regression  
- Random Forest Regressor  
- XGBoost Regressor  

### ✅ Step 6: Hyperparameter Tuning  
Used `GridSearchCV` to optimize model parameters for better performance.

### ✅ Step 7: Model Evaluation  
Used metrics like:
- R² Score  
- Root Mean Squared Error (RMSE)  
- Mean Absolute Error (MAE)  


## 📈 Model Performance Summary

| Model                 | R² Score | RMSE     | MAE      |
|-----------------------|----------|----------|----------|
| Linear Regression      | 0.327   | 6591.93  | 5310.38  |
| Random Forest Regressor| 0.629   | 4894.99  | 3430.92  |
| Decision Tree          |0.259    | 6917.31  |4235.11   |
| Gradient Boosting      | 0.434   | 6044.13  | 4744.71  |


## 📌 Business Insights

1. **Temperature and Humidity Impact:**
   - Higher temperatures lead to increased usage of cooling systems → higher energy consumption.
   - Power usage patterns vary significantly with humidity levels due to HVAC system loads.

2. **Solar Radiation Flows (Diffuse and General):**
   - Lower solar radiation (cloudy days) may result in increased artificial lighting or heating → more power usage.
   - A drop in diffuse flows is a strong indicator of increased grid demand.

3. **Air Quality and Cloudiness:**
   - Poor air quality correlates with increased indoor activity → potentially more daytime electricity usage.
   - Cloudiness indirectly impacts lighting and heating needs.



## ▶️ How to Run This Project

### Clone the Repository:
```bash
git clone https://github.com/YOUR_USERNAME/Power_Consumption_Prediction.git
cd Power_Consumption_Prediction


  
