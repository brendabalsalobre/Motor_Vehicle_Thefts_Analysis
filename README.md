# Motor Vehicle Thefts Analysis (New Zealand)

## 🔎 Project Overview
This project investigates the when, what, and where of vehicle thefts in New Zealand, using a SQL database and Excel for visual storytelling. The insights gathered from this project can help law enforcement and local governments better understand crime trends by day, region, and vehicle type.

## 🔧 Tools Used
* **MySQL (SQL)**: SQL queries for data transformation and analysis
* **Excel**: Data visualizations (bar chart, heatmap, map, and scatter plot)

## 🎯 Objectives and Analysis
The queries below were developed to answer specific questions about vehicle thefts in New Zealand: 
1. **When are vehicles most commonly stolen?**
SELECT p.product_name,
	SUM(o.quantity_ordered) as quantity_sold, 
	AVG(p.price), 
	SUM(p.price * o.quantity_ordered) as revenue
FROM products p
LEFT JOIN orders o ON p.product_id = o.product_id
GROUP BY 1
ORDER BY revenue DESC;

** 📄 Data Info
* **Source**: Maven Analytics
* **Formats**:
   * SQL (.sql) – Relational database for queries
   * CSV (.csv) – Exported data for visualizations in Excel
