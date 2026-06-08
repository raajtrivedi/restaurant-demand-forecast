# 🍽️ AI Demand Forecasting & Inventory Optimization System

Hi! This is my Project 3 for the **Data Science & Machine Learning Internship Program** at Infotact Solutions.

This project focuses on building an AI-powered demand forecasting system using real-world Restaurant POS sales data. By predicting future daily sales, restaurants can order the right inventory, prepare staff schedules, and reduce food waste.

---

# 📌 Project Objective

Restaurant inventory management often suffers from:
- Over-ordering leading to food waste and spoilage
- Under-ordering resulting in stockouts and lost revenue
- Reliance on gut feeling instead of data-driven decisions

This project aims to solve these challenges using:
- 🤖 Machine Learning (Random Forest)
- 📈 Time-Series Forecasting
- 🔧 Advanced Feature Engineering (Lags & Rolling Windows)
- ⚡ Automated FastAPI Predictions

---

# 🏛️ Problem Statement & My Strategy

When I first loaded the raw dataset, it had about 1,000 individual transactions. Initially, I thought about predicting sales for each specific menu item. However, I realized the data was too sparse—many items had zero sales on certain days. 

**My Solution:** Instead of predicting individual menu items (which would lead to poor model accuracy), I aggregated the data to predict **Total Daily Revenue** instead. The system takes historical daily revenue data and automatically predicts future demand.

---

# 📂 Dataset

## Dataset Used
- Balaji Fast Food Sales Dataset (April 2022 - March 2023)

## Main Features Used
- `total_sales` (Target Variable)
- `lag_7`, `lag_14`, `lag_21` (Past Memory)
- `rolling_mean_7`, `rolling_mean_14` (Recent Trends)
- `day_of_week`, `is_weekend`, `is_holiday` (Chronological Context)

---

# 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Processing | Pandas, NumPy |
| Time-Series Analysis | Statsmodels (`seasonal_decompose`, `autocorrelation_plot`) |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn (Linear Regression, Random Forest Regressor) |
| Deployment & API | FastAPI, Uvicorn, Joblib |

---

# 📅 Four-Week Development Roadmap

## ✅ Week 1 — Data Collection, Cleaning & EDA
- Handled messy mixed datetime formats using `format='mixed'`.
- Grouped individual orders into total daily sales to fix data sparsity.
- Used `seasonal_decompose` to understand weekly patterns.
- Checked autocorrelation and proved 7-day patterns mathematically.

---

## ✅ Week 2 — Advanced Feature Engineering
- Created chronological features (Weekends, Holidays).
- Fixed the known ISO week rollover bug using `.clip(1, 52)`.
- Created Lag features & Rolling window statistics.
- Prevented data leakage using `.shift(1)` before calculating rolling means.
- **Strict Sequential Train/Test Split** (avoided random splitting).

---

## ✅ Week 3 — Model Training & Selection
- Baseline Model: Linear Regression
- Advanced Model: Random Forest Regressor (`n_estimators=100`, `random_state=42`)
- Serialized and saved the best model using `joblib`.

---

## ✅ Week 4 — Evaluation & Deployment
- Evaluated the model strictly using MAE (Mean Absolute Error) and RMSE.
- Extracted Feature Importance to see what truly drives sales.
- Visualized Actual vs. Predicted sales using line plots.
- Built a final FastAPI deployment endpoint.

---

# 💡 Key Learnings from this Project
As a fresher, this project taught me practical lessons beyond textbook ML:
1. **Preventing Data Leakage:** I learned to use `.shift(1)` before calculating rolling averages so the model wouldn't "cheat" by looking at current-day sales.
2. **Strict Sequential Splitting:** I manually split the last 60 days to test the model on truly unseen future data instead of using a standard `train_test_split`.
3. **Messy Real-World Dates:** I learned to use `format='mixed'` to handle inconsistent slashes and dashes in the raw CSV.

---

# 📁 Project Structure

```text
📦 restaurant-demand-forecast
 ┣ 📂 data
 ┃ ┗ 📜 Balaji Fast Food Sales.csv
 ┣ 📂 notebooks
 ┃ ┣ 📜 01_data_ingestion_eda.ipynb
 ┃ ┣ 📜 02_advanced_feature_engineering.ipynb
 ┃ ┣ 📜 03_model_training_and_selection.ipynb
 ┃ ┗ 📜 04_evaluation_and_business_reporting.ipynb
 ┣ 📂 outputs
 ┃ ┣ 📜 cleaned_daily_sales.csv
 ┃ ┣ 📜 train_data.csv
 ┃ ┣ 📜 test_data.csv
 ┃ ┗ 📜 random_forest_model.pkl
 ┣ 📜 main.py
 ┣ 📜 README.md
 ┗ 📜 requirements.txt
```

---

# 👨‍💻 Contributors
1. Raj Trivedi 
