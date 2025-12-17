# S-and-P-500-stock-analysis.
S&amp;P 500 Stock Analysis (2014) – Tableau dashboard and SQL analysis of closing prices and trading volumes.
# 📊 S&P 500 Stock Analysis Mini Project (2014)

## Overview
This project explores historical S&P 500 stock trends for 2014. Using SQL for data aggregation and Tableau for visualization, it highlights patterns in **closing prices** and **trading volumes** across multiple companies. The dashboard and charts demonstrate the ability to transform raw financial data into actionable insights.

## Tools Used
- Tableau – for interactive dashboards and visualizations  
- SQL – for data querying and aggregation  
- GitHub – for version control and portfolio presentation  

## Dashboard Screenshots

## Dashboard Screenshots

### Dashboard Overview
![Dashboard Overview](dashboard/dashboard_overview.png)

### Closing Prices
![Closing Prices Chart](dashboard/closing_prices_chart.png)

### Trading Volume
![Trading Volume Chart](dashboard/trading_volume_chart.png)


## Representative SQL Analysis

```sql
-- Average closing price by stock
SELECT stock_symbol, AVG(closing_price) AS avg_price
FROM closing_prices
GROUP BY stock_symbol
ORDER BY avg_price DESC;

