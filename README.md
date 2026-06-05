# 🍽️ AI Demand Forecasting & Inventory Optimization

An enterprise-grade Time Series Forecasting project developed as part of the **Data Science & Machine Learning Internship Program** at Infotact Solutions.

This project focuses on building an AI-powered demand forecasting system for a restaurant chain using synthetic POS sales data. The system predicts daily units sold per menu item, enabling proactive inventory management and reduction of food waste.

---

# 📌 Project Objective

Restaurant inventory management often suffers from:

- Over-ordering leading to food waste and spoilage
- Under-ordering resulting in stockouts and lost revenue
- Reliance on gut feeling instead of data-driven decisions
- No visibility into seasonal and weekly demand patterns

This project aims to solve these challenges using:

- 🤖 Machine Learning
- 📈 Time Series Forecasting
- 🔧 Advanced Feature Engineering
- 📊 Demand Pattern Analysis

---

# 🏪 Problem Statement

The system accepts historical POS sales data and automatically:

- Predicts future daily sales volume per menu item
- Captures weekly and seasonal demand patterns
- Enables restaurant managers to optimize purchase orders

---

# 📂 Dataset

## Dataset Used

- Synthetic Restaurant POS Sales Data (2 years)

## Main Features

- Date
- Menu Item
- Units Sold
- Revenue
- Is Holiday
- Day of Week

---

# 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Plotly |
| Machine Learning | Scikit-learn |
| Forecasting Models | Linear Regression, Random Forest, XGBoost, Prophet |
| Notebook Environment | Jupyter Notebook |
| Version Control | Git & GitHub |

---

# ✨ Key Features

- ✅ Time Series Data Cleaning & EDA
- ✅ Seasonal Decomposition
- ✅ Autocorrelation Analysis
- ✅ Lag Feature Engineering
- ✅ Rolling Window Statistics
- ✅ Cyclic Encoding (sin/cos)
- ✅ Sequential Train/Test Split (No Data Leakage)
- ✅ XGBoost with TimeSeriesSplit CV
- ✅ Prophet Forecasting
- ✅ Feature Importance Analysis
- ✅ MAE & RMSE Evaluation
- ✅ Business Reporting

---

# 📊 Exploratory Data Analysis (EDA)

The project includes:

- Overall sales trend analysis
- Weekly seasonality patterns
- Monthly heatmap visualization
- Seasonal decomposition
- Autocorrelation analysis

---

# 🤖 Machine Learning Models Used

The following ML models were trained and evaluated:

1. Linear Regression (Baseline)
2. Random Forest Regressor
3. XGBoost Regressor
4. Prophet (Time Series Model)

The best-performing model was selected using:

- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- TimeSeriesSplit Cross Validation

---

# 📈 Evaluation Metrics

Models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- R² Score
- Feature Importance Scores
- Residual Analysis

---

# 🔄 Project Workflow

```text
Data Generation
      ↓
Data Cleaning & EDA
      ↓
Seasonal Decomposition
      ↓
Feature Engineering
      ↓
Sequential Train/Test Split
      ↓
Model Training
      ↓
Hyperparameter Tuning
      ↓
Model Evaluation
      ↓
Feature Importance
      ↓
Business Reporting
```

---

# 🔧 Feature Engineering

The ML pipeline includes:

- Lag features (1, 3, 7, 14, 21, 28 days)
- Rolling window statistics (7, 14, 30 days)
- Exponentially Weighted Mean (EWM)
- Cyclic encoding for day of week and month
- Holiday and weekend flags
- Trend feature

---

# 📌 Example Output

```python
Menu Item: Chicken Biryani
XGBoost MAE: 16.1 units
Improvement over baseline: 75%
Top Feature: day_of_week (19%)
```

---

# 📅 Four-Week Internship Development Roadmap

## ✅ Week 1 — Data Ingestion & Time-Series EDA

- Dataset generation
- Datetime cleaning
- Sales trend plotting
- Seasonal decomposition
- Autocorrelation analysis

---

## ✅ Week 2 — Advanced Feature Engineering

- Lag features
- Rolling window statistics
- Cyclic encoding
- Sequential train/test split

---

## ✅ Week 3 — Model Training & Selection

- Linear Regression baseline
- Random Forest Regressor
- XGBoost with TimeSeriesSplit CV
- Prophet forecasting
- Hyperparameter tuning

---

## ✅ Week 4 — Evaluation & Business Reporting

- MAE & RMSE comparison
- Forecast vs actual plots
- Feature importance analysis
- Residual analysis
- Business summary report

---

# 📁 Project Structure

```text
📦 restaurant-demand-forecast
 ┣ 📂 data
 ┣ 📂 notebooks
 ┣ 📂 src
 ┣ 📂 outputs
 ┣ 📂 models
 ┣ 📜 README.md
 ┗ 📜 requirements.txt
```

---

# 🚀 Future Improvements

- 🔥 FastAPI deployment
- 🌐 Web dashboard integration
- 🌦️ Weather API integration
- 📱 Real-time inventory portal
- ☁️ Cloud deployment
- 📊 Live analytics dashboard

---

# 📌 GitHub Best Practices Followed

- ✅ Semantic commit messages
- ✅ Incremental weekly commits
- ✅ Clean notebook management
- ✅ Structured repository organization
- ✅ Modular ML workflow

---

# 👨‍💻 Contributors

1. Raj Trivedi
