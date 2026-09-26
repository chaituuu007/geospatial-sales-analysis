# 🌍 Geospatial Sales Analysis

> A data analytics project that analyzes regional sales, customer demand, revenue, and service capacity to identify high-potential underserved markets.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![Folium](https://img.shields.io/badge/Folium-Interactive%20Maps-green)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 📌 Project Overview

This project performs **geospatial sales analysis** to understand how sales performance and customer demand vary across different cities and regions.

The analysis combines:

- Customer/user volume
- Revenue
- Orders
- Geographic location
- Demand Index
- Service Capacity Index

The goal is to identify regions where **customer demand and market activity indicate potential opportunities that may not be fully supported by current service capacity**.

> **Note:** The dataset used in this project is synthetic and is intended for analytics/project demonstration purposes.

---

## 🎯 Business Objective

Businesses need to understand **where demand is high and whether existing service capacity is sufficient**.

This project answers questions such as:

- Which regions generate the highest revenue?
- Where is customer/user activity concentrated?
- Which cities have high demand?
- Where does demand exceed service capacity?
- Which regions show potential for expansion?

---

## 🗂️ Dataset

The dataset contains monthly regional sales records with the following fields:

| Column | Description |
|---|---|
| `Month` | Monthly observation |
| `State` | State/region |
| `City` | City |
| `PostalCode` | Postal code |
| `Latitude` | Geographic latitude |
| `Longitude` | Geographic longitude |
| `Users` | Number of users |
| `Orders` | Number of orders |
| `Revenue` | Revenue generated |
| `DemandIndex` | Relative customer demand |
| `ServiceCapacityIndex` | Relative service capacity |

---

## 🧹 Data Cleaning

The following preprocessing steps were performed:

- Cleaned State and City names
- Standardized Postal Codes
- Converted numeric fields to appropriate numeric types
- Validated latitude and longitude values
- Removed records missing essential geographic or analytical fields
- Aggregated monthly records at the city level
- Calculated average demand and service capacity

---

## 📊 Analysis Methodology

### 1. Regional Aggregation

Data was aggregated by:

- State
- City
- Postal Code
- Latitude
- Longitude

The following metrics were calculated:

- Total Users
- Total Revenue
- Total Orders
- Average Demand Index
- Average Service Capacity Index
- Average Monthly Users

### 2. Demand-Capacity Gap

A positive difference between demand and service capacity was used to identify areas where demand may not be fully supported by current capacity.

### 3. Opportunity Score

An analytical opportunity score was created using:

- Average Demand
- Positive Demand-Capacity Gap
- User Density

The score is used to prioritize regions for further investigation.

---

## 🗺️ Interactive Geospatial Visualization

The project includes an interactive **Folium map** containing geographic markers for the analyzed cities.

Each marker provides:

- City
- State
- Postal Code
- Users
- Revenue
- Average Demand
- Average Capacity
- Demand Gap
- Opportunity Score

### 🔴 High-Potential Regions

The three highest-scoring regions identified by the analysis are:

| Rank | Region | State |
|---|---|---|
| 1 | Visakhapatnam | Andhra Pradesh |
| 2 | Mysuru | Karnataka |
| 3 | Gurugram | Haryana |

These results represent the output of the project's scoring methodology and should not be interpreted as real-world forecasts because the dataset is synthetic.

---

## 💡 Key Insights

### Visakhapatnam
- 2,538 cumulative users
- ₹2.31M cumulative revenue
- Average demand: **1.15**
- Average service capacity: **1.10**

### Mysuru
- 2,205 cumulative users
- ₹1.98M cumulative revenue
- Average demand: **1.10**
- Average service capacity: **1.03**

### Gurugram
- 2,169 cumulative users
- ₹2.01M cumulative revenue
- Average demand: **1.13**
- Average service capacity: **1.06**

These locations show a combination of significant user activity and demand relative to service capacity under the project's analytical framework.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **Folium**
- **HTML**
- **Geospatial Analysis**
- **Data Cleaning**
- **Data Aggregation**
- **Exploratory Data Analysis**

---

## 📁 Project Structure

```text
geospatial-sales-analysis/
│
├── README.md
├── Spatial_Analysis_Report.pdf
├── geospatial_city_summary.csv
└── india_geospatial_sales_analysis.html
