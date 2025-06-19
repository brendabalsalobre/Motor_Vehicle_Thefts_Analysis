# Motor Vehicle Thefts Analysis (New Zealand)

## 🔎 Project Overview
This project investigates the when, what, and where of vehicle thefts in New Zealand, using a SQL database and Excel for visual storytelling. The insights gathered from this project can help law enforcement and local governments better understand crime trends by day, region, and vehicle type.

## 🔧 Tools Used
* **MySQL (SQL)**: SQL queries for data transformation and analysis
* **Excel**: Data visualizations (bar chart, heatmap, map, and scatter plot)

## 🎯 Objectives and Analysis
The queries below were developed to answer specific questions about vehicle thefts in New Zealand: 
1. **When are vehicles most commonly stolen?**

'''sql 
SELECT 
  CASE DAYOFWEEK(date_stolen)
    WHEN 1 THEN 'Sunday'
    WHEN 2 THEN 'Monday'
    WHEN 3 THEN 'Tuesday'
    WHEN 4 THEN 'Wednesday'
    WHEN 5 THEN 'Thursday'
    WHEN 6 THEN 'Friday'
    ELSE 'Saturday'
  END AS day_of_week,
  COUNT(vehicle_id) AS num_vehicles
FROM stolen_vehicles
GROUP BY day_of_week;

** 📄 Data Info
* **Source**: Maven Analytics
* **Formats**:
   * SQL (.sql) – Relational database for queries
   * CSV (.csv) – Exported data for visualizations in Excel
