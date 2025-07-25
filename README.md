
# ☕ Coffee Sales Data Analysis and Prediction

This project performs an **end-to-end data analysis** and builds a simple **sales prediction model** using a coffee shop's transactional dataset. It includes data cleaning, feature engineering, visualization, and machine learning modeling, all performed in Python using popular data science libraries.

---

## 📁 Dataset Summary

- **Rows:** 1133 transactions
- **Columns:** 6 main columns:
  - `date`, `datetime` — Transaction timestamps
  - `cash_type`, `card` — Payment info
  - `money` — Amount spent
  - `coffee_name` — Coffee product purchased

---

## 🔧 Key Steps Performed

### 1. 📊 Data Preprocessing
- Converted `date` and `datetime` to proper datetime objects
- Handled missing values (`card` column had 89 missing)
- Checked for and removed any outliers in `money` using Z-score (threshold = 3)
- Added new time-based features:
  - `month`, `day` (weekday), and `hour`

### 2. 📈 Exploratory Data Analysis
- **Revenue by Coffee Type**: Bar plot showing which coffee contributes the most
- **Monthly Sales Trends**: Line plot for coffee type performance by month
- **Weekly and Hourly Trends**: Bar charts analyzing:
  - Best days of the week for sales
  - Peak hours of the day
- **Hourly Coffee Trends**: Subplots for each coffee type's hourly performance

### 3. 🧠 Feature Engineering for ML
Created a daily sales dataset with features:
- `day_of_week`, `day_of_month`, `month`, `week_of_year`
- Used for predicting `total_sales`

### 4. 🤖 Machine Learning Model
- **Model Used**: Linear Regression (`scikit-learn`)
- **Features**: Time-based variables
- **Target**: Daily `total_sales`
- **Metrics**:
  - Mean Squared Error (MSE): `9942.10`
  - R² Score: `-0.10` (model underperformed — could be improved with better features or models)

---

## 📊 Visual Output Highlights

| Plot Type                        | Purpose                                 |
|----------------------------------|-----------------------------------------|
| Revenue by Coffee Type (bar)     | Understand which coffee earns the most  |
| Monthly Sales (line)             | Track seasonal patterns                 |
| Day-of-Week Sales (bar)          | Identify best performing weekdays       |
| Hourly Sales (bar)               | Find peak hours for business            |
| Hourly by Coffee Type (subplot)  | Analyze each drink’s sales by hour      |

---

## 🧠 Libraries Used

```python
pandas, numpy, matplotlib, seaborn, datetime, scipy, sklearn
