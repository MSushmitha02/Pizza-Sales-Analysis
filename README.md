# Pizza Sales Analysis (SQL & Tableau)

Pizza sales analysis using SQL and Tableau to evaluate sales performance and customer ordering patterns.

## Tools Used
- SQL
- Tableau

## Key Analysis
- Calculated KPIs such as total revenue, total orders, average order value, and average pizzas per order
- Analyzed hourly and weekly sales trends
- Identified top and bottom performing pizzas using SQL
- Visualized insights using an interactive Tableau dashboard

## Dashboard Features
- KPI cards for quick overview
- Hourly and weekly trend analysis
- Sales contribution by pizza category and size
- Filters for date range and pizza category

## Key Insights
- Peak pizza orders occur around lunchtime and in the evening.
- Classic and Chicken pizzas contribute most revenue.
- XX-Large pizzas are rarely ordered.

## Sample SQL Queries

-- Total Revenue:
SELECT SUM(total_price) AS total_revenue
FROM pizza_sales;

-- Weekly Orders Trend: 
SELECT 
  DATEPART(iso_week, order_date) AS week_num,
  COUNT(DISTINCT order_id) AS total_orders
FROM pizza_sales
GROUP BY DATEPART(iso_week, order_date)
ORDER BY week_num;




