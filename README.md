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

## Features
# Numerical Features:
1- Item_Weight: Weight of the item

2- Item_Visibility: Visibility of the item in the store

3- Item_MRP: Maximum Retail Price

4- Outlet_Establishment_Year: Year when outlet was established

5- Item_Outlet_Sales: Sales of the item (Target Variable)

## Categorical Features:

1- Item_Identifier: Unique ID for items

2- Item_Fat_Content: Fat content category (Low Fat/Regular)

3- Item_Type: Type of item

4- Outlet_Identifier: Unique ID for outlets

5- Outlet_Size: Size of the outlet

6- Outlet_Location_Type: Tier type of location

7- Outlet_Type: Type of outlet

## Methodology
- Data Loading and Inspection
- Data Cleaning (handling missing values, fixing inconsistencies)
- Exploratory Data Analysis
- Data Visualization
- Feature Engineering

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- missingno
scikit-learn


##  Models Implemented

### 1. Linear Regression (Baseline)
- Simple, interpretable model
- Test R²: ~0.58
- RMSE: ~$1,069

### 2. Random Forest (Default)
- Ensemble tree-based model
- Handles non-linear relationships
- Better performance than linear regression

### 3. Random Forest (Tuned with GridSearchCV)
- **Recommended Model** 
- Hyperparameters tuned: n_estimators, max_depth, min_samples_split, min_samples_leaf
- 5-fold cross-validation
- Best test performance

---

##  Data Preprocessing

### Cleaning Steps:
1.  Removed duplicate records
2. Standardized categorical variables (e.g., 'LF' → 'Low Fat')
3. Handled missing values:
   - Numerical: Median imputation
   - Categorical: Most frequent imputation
4.  Scaled numerical features (StandardScaler)
5.  Encoded categorical features (OneHotEncoder)

### Pipeline:
```python
Pipeline([
    ('preprocessor', ColumnTransformer([
        ('num', numerical_pipeline, numerical_cols),
        ('cat', categorical_pipeline, categorical_cols)
    ])),
    ('regressor', RandomForestRegressor())
])

