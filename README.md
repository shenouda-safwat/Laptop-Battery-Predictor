# 🔋 Project Name: **Battery Guardian: Laptop Battery Health Predictor**


## 📖 Dataset Source:

[Laptop Battery Health & Usage Dataset - Kaggle](https://www.kaggle.com/datasets/prince7489/laptop-battery-health-and-usage-dataset/data)

---

## 🧩 Project Overview

**Battery Guardian** is a Machine Learning project designed to analyze laptop battery health and predict battery degradation based on real-world usage patterns. The model captures factors like daily usage, charging cycles, battery age, overheating, and charge limits to provide actionable insights for users and IT managers.

This project demonstrates data preprocessing, feature analysis, regression modeling, classification, and visualization techniques using Python, Pandas, Seaborn, and scikit-learn.

---

## 🔍 Features & Insights

The dataset contains multiple features, including:

* `charging_cycles`: Number of times the battery has been charged.
* `battery_age_months`: Age of the battery in months.
* `avg_charge_limit_percent`: Typical charge limit set by the user.
* `daily_usage_hours`: Average daily laptop usage hours.
* `overheating_issues`: Binary indicator if overheating occurred.
* `performance_rating` (removed during modeling to prevent leakage)
* `model_year` (removed to avoid shortcut correlation)

**Key Insights:**

* Charging cycles and battery age are the most dominant factors affecting battery health.
* High charge limits and heavy daily usage accelerate battery degradation.
* Removing features that leak the target (performance_rating) improves model generalization.

---

## 🛠️ Project Workflow

1. **Data Loading & Cleaning**

   * Load dataset from Kaggle CSV.
   * Check missing values and handle categorical features (e.g., `Yes`/`No` to 1/0).

2. **Exploratory Data Analysis (EDA)**

   * Visualize battery health distribution.
   * Analyze correlation between features and battery health.
   * Identify top features impacting battery degradation.

3. **Feature Selection**

   * Selected features: `charging_cycles`, `battery_age_months`, `avg_charge_limit_percent`, `daily_usage_hours`.

4. **Train-Test Split & Scaling**

   * Split dataset (80% train, 20% test).
   * Standardize features using `StandardScaler`.

5. **Regression Modeling**

   * Linear Regression to predict `battery_health_percent`.
   * Evaluate with MSE, R², and scatter plot with ideal line.

6. **Optional Classification**

   * Categorize battery as Healthy (≥80%) or Degraded (<80%).
   * Logistic Regression to classify battery status.
   * Evaluate with accuracy, precision, recall, F1-score.

7. **Visualization**

   * Scatter plots, boxplots, heatmaps.
   * Feature importance for top 5 contributors.

---

## 📈 Model Performance

**Regression:**

* MSE: ~1.63
* R²: ~0.934
* Residuals and actual vs predicted plots show strong predictive ability with most variance explained.

**Classification (optional):**

* Accuracy: 100% on small test sample (note: requires larger validation for real-world generalization)
* Precision / Recall / F1: 1.00

> Note: Performance ratings and model_year features were removed to avoid data leakage and maintain realistic predictions.

---

## 🔧 Tools & Libraries Used

* Python 3.11
* Pandas & NumPy
* Matplotlib & Seaborn
* scikit-learn (LinearRegression, LogisticRegression, StandardScaler, train_test_split)
* Jupyter Notebook for interactive development

---

## 💡 Usage

1. Clone the repository:

```bash
git clone <your-repo-link>
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the Jupyter Notebook to explore EDA, train models, and visualize results.

4. Modify the input features to test battery health predictions for different usage scenarios.

---

## 🚀 Future Enhancements

* Implement ensemble models (RandomForest, XGBoost) for higher predictive accuracy.
* Create a Streamlit dashboard for interactive battery health prediction.
* Incorporate time-series data for battery health over lifespan.
* Build alerts/recommendations system for optimal battery usage.

---

## 📝 Conclusion

**Battery Guardian** provides a practical, interpretable model for predicting laptop battery health. The project emphasizes **data-driven insights**, responsible feature selection, and effective visualization, making it ideal for educational purposes, portfolio showcases, or preliminary deployment in IT management systems.


## [Shenouda Safwat](https://www.linkedin.com/in/shenouda-safwat/)
