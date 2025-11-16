# ☕ Brewed Insights: Coffee Sales Analysis

## 📊 Project Overview

A full-year sales analysis for a coffee shop, uncovering revenue drivers, operational bottlenecks, and demand patterns. The project blends SQL, exploratory analysis, and predictive modeling to generate practical, real-world business insights.

## 🔗 Dataset


Source: [Kaggle](https://www.kaggle.com/datasets/kainatjamil12/coffe-sale/data).

- **Total transactions** 3,547  

- **Included features:**
  - `hour_of_day` – hour of sale (0–23)  
  - `cash_type` – payment method (cash or card)  
  - `money` – revenue from the transaction  
  - `coffee_name` – type of coffee sold  
  - `Time_of_Day` – Morning, Afternoon, Night  
  - `Weekday` – day of the week  
  - `Month_name` – month of the sale  
  - `Weekdaysort` / `Monthsort` – numeric order for sorting  
  - `Date` – transaction date  
  - `Time`- transaction time

## 🎯 Business Objectives

- Identify the products and time windows that drive revenue

- Optimize staffing and scheduling

- Detect and profile high-value purchases

- Build predictive models to support forecasting and inventory planning

# Executive Summary / Key Findings

## 📌 Key Metrics

| Metric | Value |
|--------|-------|
| Total Transactions | 3,547 |G
| Total Revenue | $112,245.58 |
| Average Transaction | $31.64 |
| High-Value Transactions (Top 25%) | 1,415 (46% of revenue) |
| Operating Hours | 6 AM - 10 PM |

## 📊 Revenue Drivers

- **Top product:** Latte — $26,875 (757 units)

- **Peak hour:** 10 AM — $10,198

- **Best weekday:** Tuesday — $18,168

- **High-value transactions:** Top 25% → 46% of revenue

## ⏰ Time-Based Insights

- **Morning (9–11 AM)** — peak staffing needed

- **Afternoon slump (1–3 PM)** — good for promotions

- **Evening** — preference for premium drinks

- **Weekend revenue** ~20–25% lower than weekdays

## 💰 Outliers

- Top 25% transactions generated $51,511 (46% revenue)

- Latte & Cappuccino dominate high-value sales

## 🔮 Predictive Analysis

- **Hourly forecast:** $30.16 (6 AM) → $33.22 (10 PM)

- **Monthly projection:** ≈$11,076 over 3 months

## 💡 Recommendations

- **Staffing:** Strengthen 9–11 AM and late-afternoon mini-peaks

- **Product strategy:** Prioritize Lattes & Americanos with Milk during peak

- **Promotions:** Slow hours for combos/discounts

- **Inventory:** Ensure top sellers are stocked during weekdays

- **Weekend strategy:** Targeted offers to boost traffic

## 📈 Analysis Methodology

1. **Data Loading & Preparation**: CSV data imported into asSQLite database
2. **Exploratory Data Analysis**: 
   - Product performance analysis
   - Temporal pattern identification (hourly, daily, monthly)
   - Customer transaction segmentation
3. **Statistical Analysis**:
   - Sales growth rate calculations
   - High-value transaction profiling (75th percentile threshold)
   - Average transaction value by time period
4. **Predictive Modeling**:
    - Polynomial regression (degree 2) to capture non-linear hourly sales patterns   
    - Monthly revenue projection using historical trends

## 🛠️ Technologies Used

- **Python**: Data manipulation and analysis
- **Pandas**: Data processing and aggregation
- **SQLite**: Database management and complex queries
- **scikit-learn**: Predictive modeling (Polynomial Regression)
- **NumPy**: Numerical computations

## 📁 Project Structure

```
coffee-sales-analysis/
├── data/
│   └── coffee_sales.csv
├── notebooks/
│   └── coffee_sales_analysis.ipynb
|   └── coffee.db (generated)
└── README.md
```

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy scikit-learn sqlite3
```

### Running the Analysis
```python
# Navigate to notebooks directory
cd notebooks/

# Launch Jupyter Notebook
jupyter notebook coffee_sales_analysis.ipynb
```

## 📊 Sample Queries

```sql
-- Top 5 best-selling products
SELECT coffee_name, COUNT(*) AS total_sales, 
       ROUND(SUM(money), 2) AS total_revenue
FROM coffee_sales
GROUP BY coffee_name
ORDER BY total_sales DESC
LIMIT 5;

-- Peak sales hours
SELECT hour_of_day, SUM(money) AS total
FROM coffee_sales
GROUP BY hour_of_day
ORDER BY hour_of_day;
```


## 👤 Graziella Morais

**Data Analyst | Business Intelligence**

*Passionate about transforming raw data into strategic business insights*

## 📝 License

This project is available for educational and portfolio purposes.