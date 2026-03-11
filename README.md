## Prediction of Product Sales
---
## Project Description
This project analyzes retail sales data to understand factors influencing product sales and build predictive models. The dataset contains information about items (weight, fat content, visibility, MRP) and outlet characteristics (size, location type, establishment year) to predict item outlet sales. The analysis includes comprehensive data cleaning, exploratory data analysis, and visualization of key patterns in the data.

## Key Insights from Visualizations
1. Correlation Heatmap of Numerical Features
The heatmap highlights relationships between numerical variables, specifically showing a notable positive correlation between Item MRP (price) and Item Outlet Sales, suggesting higher prices generally drive higher revenue.

2. Frequency of Categorical Features
The frequency plots reveal that "Low Fat" products and items sold in Tier 3 locations are the most dominant segments in this specific retailer's portfolio compared to their counterparts.

## Dataset Information
Source: Sales predictions dataset 2023
Records: 8,523 entries
Features: 12 columns (7 categorical, 5 numerical)
Features
# Numerical Features:
Item_Weight: Weight of the item
Item_Visibility: Visibility of the item in the store
Item_MRP: Maximum Retail Price
Outlet_Establishment_Year: Year when outlet was established
Item_Outlet_Sales: Sales of the item (Target Variable)

## Categorical Features:
Item_Identifier: Unique ID for items
Item_Fat_Content: Fat content category (Low Fat/Regular)
Item_Type: Type of item
Outlet_Identifier: Unique ID for outlets
Outlet_Size: Size of the outlet
Outlet_Location_Type: Tier type of location
Outlet_Type: Type of outlet

## Methodology
Data Loading and Inspection
Data Cleaning (handling missing values, fixing inconsistencies)
Exploratory Data Analysis
Data Visualization
Feature Engineering
Model Building (to be completed)
Requirements
Python 3.x
pandas
numpy
matplotlib
seaborn
missingno
scikit-learn
