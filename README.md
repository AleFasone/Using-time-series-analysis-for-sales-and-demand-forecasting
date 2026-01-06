# Using Time Series Analysis for Sales and Demand Forecasting

## 📖 Project Overview
Accurate demand forecasting is a critical challenge for independent publishers, as poor forecasts can lead to inefficient print runs, excess inventory, and missed sales opportunities.  
This project applies **time series analysis, machine learning, and deep learning models** to forecast book sales and demand, combining interpretability with predictive accuracy.

Using historical sales data from **Nielsen BookScan**, the analysis compares classical statistical models with modern ML and neural network approaches across **weekly and monthly horizons**, providing actionable insights for both tactical and strategic decision-making.

## 🎯 Objectives
- Forecast sales and demand using time series data  
- Compare classical, machine learning, and deep learning models  
- Capture both short-term volatility and long-term seasonal patterns  
- Support data-driven decisions for inventory, reprinting, and investment planning  

## 🗂 Project Structure
├── Using_time_series_analysis_for_sales_and_demand_forecasting.ipynb

├── Using time series analysis for sales and demand forecasting.pdf

└── README.md

- **Notebook**: Full forecasting pipeline including exploratory analysis, modeling, tuning, and evaluation  
- **PDF report**: Structured explanation of methods, results, and business recommendations  

## 🧪 Methodology

### 1. Classical Time Series Analysis
- Seasonal decomposition of weekly sales
- Stationarity testing
- **Auto-ARIMA / SARIMA** models to capture trend and seasonality
- Baseline interpretability for long-term demand patterns

### 2. Machine Learning Forecasting
- **XGBoost regression models** trained on lag-based features
- Hyperparameter tuning via time-series cross-validation
- Designed to capture nonlinear drivers and short-term demand fluctuations

### 3. Deep Learning Models
- **LSTM neural networks** trained on weekly sales data
- Architectures optimized using **KerasTuner**
- Capable of learning complex sequential and long-term temporal dependencies

### 4. Hybrid Forecasting Approaches
Two hybrid strategies were implemented:
- **Sequential SARIMA + LSTM**: LSTM trained on SARIMA residuals
- **Parallel Hybrid (Weighted)**: weighted combination of classical and neural forecasts

All models were extended to **monthly forecasting** to compare tactical vs strategic performance.

## 📊 Results Summary

### Weekly Forecasting
- **XGBoost** delivered the best overall weekly accuracy for *The Alchemist*, capturing short-term volatility and promotional effects
- **Hybrid SARIMA + LSTM** performed best for *The Very Hungry Caterpillar*, effectively modeling recurring demand and seasonality
- Classical ARIMA models captured seasonality well but struggled with sudden demand changes

### Monthly Forecasting
- Aggregation to monthly frequency reduced noise and improved interpretability
- **SARIMA** models outperformed others at the monthly level, highlighting dominant seasonal and cyclical patterns
- Monthly forecasts proved more suitable for long-term planning, budgeting, and print volume decisions

Performance was evaluated using **MAE** and **MAPE**, balancing accuracy and business interpretability.

## 🏆 Key Takeaways
- No single model dominates across all horizons and products
- Machine learning and hybrid models excel at **short-term forecasting**
- Classical SARIMA models provide **long-term stability and interpretability**
- A multi-horizon approach yields the best operational outcomes

## 💡 Business Impact
- Enables data-driven inventory and reprinting decisions  
- Reduces excess stock and missed sales opportunities  
- Aligns production and marketing strategies with real demand patterns  
- Supports both tactical (weekly) and strategic (monthly) planning  

## 🛠 Technologies Used
- Python  
- pandas, numpy  
- statsmodels  
- scikit-learn  
- XGBoost  
- TensorFlow / Keras  
- KerasTuner  
- matplotlib, seaborn  

## 🚀 Future Improvements
- Integration of exogenous variables (pricing, promotions, events)  
- Probabilistic forecasting and confidence intervals  
- Automated model selection by product category  
- Real-time demand forecasting pipelines  

## 👤 Author
**Alessandro Fasone**  
