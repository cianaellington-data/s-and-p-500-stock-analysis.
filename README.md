# 📊 S&P 500 Stock Analysis Mini Project (2014)

## Overview
This project analyzes historical S&P 500 stock trends for 2014. Using **SQL for data analysis** and **Tableau for visualization**, it explores patterns in **closing prices** and **trading volumes** across multiple companies.  

The goal is to transform raw financial data into actionable insights and create clear, interactive dashboards to visualize market trends.

---

## Tools Used
- **Tableau** – for interactive dashboards and visualizations  
- **SQL** – for querying, aggregating, and analyzing data  
- **GitHub** – for version control and project presentation  

---

## Dashboard Screenshots

### Dashboard Overview
![Dashboard Overview](https://raw.githubusercontent.com/cianaellington-data/s-and-p-500-stock-analysis/main/dashboard_overview.png)

### Closing Prices
![Closing Prices Chart](https://raw.githubusercontent.com/cianaellington-data/s-and-p-500-stock-analysis/main/Closing_prices_chart.png)

### Trading Volume
![Trading Volume Chart](https://raw.githubusercontent.com/cianaellington-data/s-and-p-500-stock-analysis/main/trading_volume_chart.png)

---

## Representative SQL Analysis

Example queries used to generate insights:

```sql
-- 1. Average closing price by stock
SELECT stock_symbol, AVG(closing_price) AS avg_price
FROM closing_prices
GROUP BY stock_symbol
ORDER BY avg_price DESC;

-- 2. Total trading volume by stock
SELECT stock_symbol, SUM(trading_volume) AS total_volume
FROM trading_volume
GROUP BY stock_symbol
ORDER BY total_volume DESC;

-- 3. Daily closing price and volume for each stock
SELECT c.date, c.stock_symbol, c.closing_price, v.trading_volume
FROM closing_prices c
JOIN trading_volume v
  ON c.date = v.date
  AND c.stock_symbol = v.stock_symbol
ORDER BY c.date;





