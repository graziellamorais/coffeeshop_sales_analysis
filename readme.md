# Brewed Insights: Coffee Sales Analysis

This project analyzes a coffee shop’s transaction data to uncover patterns in sales, revenue, and customer behavior. The goal is to provide actionable insights to optimize staffing, menu offerings, promotions, and inventory management.


## Dataset

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


## Tools & Workflow

- **Python (Pandas):** data cleaning, aggregation, feature creation, exploratory analysis  
- **SQLite:** storing the dataset as a relational database and running SQL queries 
- **Tableau (planned):** interactive dashboards for stakeholders  

**Workflow Summary:**

1. Load CSV data into a Pandas DataFrame.  
2. Store data in SQLite and query with SQL for aggregation and feature creation.  
3. Generate new features: 
   - `avg_sale_per_hour`  
   - `sales_growth_rate` by month  
4. Conduct exploratory data analysis (EDA):  
   - Top-selling products  
   - Peak hours and revenue by weekday  
   - Average transaction value by hour  
   - Monthly growth trends  
   - Identify extreme sales transactions (outliers)  
5. Visualize results using plots and heatmaps.  
6. Prepare dashboard in Tableau for interactive insights.  


## Key Insights

- **Top-selling products:** Latte and Americano with Milk generate the highest revenue, while mid-level sellers like Capuccino and Cortado contribute consistently.  
- **Peak hours:** 10 AM is the busiest hour; afternoons and evenings see higher average transaction values. Early mornings (6–7 AM) have the lowest sales.  
- **Weekday trends:** Tuesday and Monday have the highest revenue; weekends are slower.  
- **Monthly sales trends:** Sales show volatility in spring, peak late-year (Sep–Oct), and dip in Nov.  
- **Extreme transactions:** 128 high-value transactions make up 4.41% of total revenue, indicating premium purchasing behavior.  

**Actionable Recommendations:**

- Align **staffing** with peak hours and busy weekdays.  
- Promote **top-selling drinks** during peak traffic to maximize revenue.  
- Introduce **promotions or combos** in slower periods (1–3 PM, weekends, early morning).  
- Track **inventory** to prevent stockouts of popular or high-margin drinks.  
- Encourage **upselling and loyalty programs** for premium transactions.  

---

## Next Steps

- Build an **interactive dashboard in Tableau** to allow stakeholders to filter by date, product, hour, and payment type.  
- Incorporate **predictive analytics** to forecast demand by hour, day, and month.