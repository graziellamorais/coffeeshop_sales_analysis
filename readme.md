# ☕ Brewed Insights: Coffee Sales Analysis

## 📊 Project Overview

A comprehensive data analysis project examining coffee shop sales patterns to identify revenue drivers, optimize operations, and forecast future performance. This analysis combines SQL querying, statistical analysis, and basic machine learning to deliver actionable business insights.

## 🔗 Dataset


The dataset used for this analysis can be found [here](https://www.kaggle.com/datasets/kainatjamil12/coffe-sale/data).

- **Number of transactions:** 3,547  
- **Features included:**
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

- Identify top-performing products and revenue patterns
- Optimize staffing based on hourly and daily demand
- Uncover high-value customer transactions
- Generate predictive models for inventory and financial planning

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

## 🔍 Key Findings

### Revenue Drivers
- **Top Product**: Latte generates $26,875 (757 units sold)
- **Peak Hour**: 10 AM produces $10,198 in revenue
- **Strongest Day**: Tuesday leads with $18,168
- **High-Value Sales**: Top 25% of transactions contribute 46% of total revenue

### Operational Insights
- Morning rush (9-11 AM) requires maximum staffing
- Afternoon slump (1-3 PM) presents promotional opportunities
- Evening sales (7-9 PM) show premium drink preferences
- Weekend revenue drops 20-25% compared to weekdays

### Predictive Analysis
- **Hourly Forecast**: Sales expected to increase from $30.16 (6 AM) to $33.22 (10 PM)
- **Monthly Projection**: Revenue forecasted to reach $11,076 within 3 months (39% growth)

## 💡 Strategic Recommendations

1. **Staffing Optimization**: Increase staff during 9-11 AM and 4-5 PM peak periods
2. **Product Focus**: Promote Latte and Americano with Milk during high-traffic hours
3. **Promotional Strategy**: Target slow hours (1-3 PM) with lunch combos and discounts
4. **Inventory Planning**: Ensure adequate stock of top sellers during weekdays
5. **Weekend Activation**: Implement weekend promotions to boost lower sales days

## 📈 Analysis Methodology

1. **Data Loading & Preparation**: CSV data imported into SQLite database
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

## 📌 Key Metrics

| Metric | Value |
|--------|-------|
| Total Transactions | 3,547 |G
| Total Revenue | $112,245.58 |
| Average Transaction | $31.64 |
| High-Value Transactions (Top 25%) | 1,415 (46% of revenue) |
| Operating Hours | 6 AM - 10 PM |

## 🔮 Future Enhancements

- Customer segmentation analysis using clustering algorithms
- Seasonal trend decomposition
- Real-time dashboard for live sales monitoring
- A/B testing framework for promotional campaigns
- Integration with POS system for automated reporting

## 👤 Graziella Morais

**Data Analyst | Business Intelligence**

*Passionate about transforming raw data into strategic business insights*

## 📝 License

This project is available for educational and portfolio purposes.