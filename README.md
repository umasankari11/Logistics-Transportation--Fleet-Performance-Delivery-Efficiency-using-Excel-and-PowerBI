# 🚚 Logistics & Transportation – Fleet Performance & Delivery Efficiency

# 

This project evaluates logistics fleet operations to measure on-time delivery performance, fuel efficiency, and cost per kilometer using Power BI. It aims to help organizations optimize routes, reduce operational costs, and improve delivery efficiency.

* * *

## 📌 Description

# 

This analytical project focuses on enhancing fleet performance for a logistics company by studying trip-level data and vehicle attributes. The process includes data cleaning, building an optimized data model, generating key DAX measures, and developing interactive visualizations.  
The final dashboard provides actionable insights into route performance, vehicle utilization, fuel consumption patterns, and cost efficiency.

* * *

## 🚀 Getting Started

### Dependencies

# 

| Requirement | Details |
| --- | --- |
| Operating System | Windows 10 / 11 |
| Software | Power BI Desktop |
| Dataset Required | Logistics Trip Data + Vehicle Master |
| Skills | Data Modeling, DAX, Power BI Visualizations |

* * *

### Installing

# 

| Step | Instruction |
| --- | --- |
| 1 | Download the Logistics Dataset (Trips & Vehicle Master). |
| 2 | Open Power BI Desktop. |
| 3 | Import Excel/CSV files into Power BI. |
| 4 | Validate data types (Date, Text, Numeric). |
| 5 | Clean and replace missing values where required. |

  

* * *

###   

# 🎯 Project Steps & Objectives

# 

| Step | Task |
| --- | --- |
| 1. Data Cleaning & Modeling | Fix missing fuel consumption per vehicle type and relate Trips ↔ Vehicle Master |
| 2. DAX Measures | Fuel Efficiency, On-Time Delivery %, Cost per km |
| 3. Visualizations | Bar, Line, KPI, Map |

* * *

#   

###   

### Executing the Project

#### 1\. Data Cleaning & Preparation

# 

*   Handle missing fuel consumption by calculating average fuel consumption per vehicle type.
    
*   Standardize column names and data types.
    
*   Remove duplicate Trip or Vehicle entries.
    

#### 2\. Data Modeling

# 

*   Create a relationship:
    
    `Trips[Vehicle ID] → Vehicle Master[Vehicle ID]`
    
*   Ensure Vehicle Master acts as a dimension table, and Trips acts as a fact table.
    

#### 3\. DAX Measures

# 

`Fuel Efficiency =     SUM(Trips[Distance]) / SUM(Trips[Fuel Consumed])  On-Time Delivery % =     DIVIDE(         CALCULATE(COUNTROWS(Trips), Trips[Delivery Status] = "On-Time"),         COUNTROWS(Trips)     )  Cost per km =     DIVIDE(         SUM(Trips[Fuel Cost]) + SUM(VehicleMaster[Maintenance Cost]),         SUM(Trips[Distance])     )`

#### 4\. Report Visualizations

# 

| Visual Type | Insight Provided |
| --- | --- |
| Bar Chart | On-Time Delivery % by Route |
| Line Chart | Monthly Fuel Efficiency Trend |
| KPI Cards | Avg. Delivery Time • Cost per km • Total Trips |
| Map Visual | Delivery Performance by Origin → Destination |
  

  

  

# 📊 **Insights to be Focus**

# 

*   **On-Time Delivery** is below target due to route congestion and vehicle downtime. High-performing routes (>95%) can be used as benchmarks.
    
*   **Fuel Efficiency** varies by vehicle type; older and poorly maintained vehicles show the lowest efficiency.
    
*   **Cost per km** is higher on urban and high-traffic routes due to idling, congestion, and low load utilization.
    
*   **Route Insights:** Late deliveries are concentrated on routes with poor road conditions and traffic unpredictability.
    
*   **Vehicle Utilization:** 20–30% of vehicles are under-utilized or performing below efficiency norms—ideal candidates for rerouting or maintenance.
    
*   **Driver Insights:** Efficient drivers consistently show better fuel usage and higher on-time delivery rates.
    

**Overall:** Focus on route optimization, predictive maintenance, and driver performance improvements to reduce cost and boost delivery efficiency.
