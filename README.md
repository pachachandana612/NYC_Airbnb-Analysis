---
title: "NYC Airbnb Data Analysis"
author: "Chandana Pacha"
---

# Problem Statement
The goal of this project is to analyze Airbnb listings in NYC to identify key factors that affect pricing and to build predictive models to estimate listing prices.

# Objectives
1. **Data Collection**: Obtain and structure Airbnb listing data with features like location, room type, minimum nights, and reviews.
2. **Data Preprocessing**: Clean and transform the data by handling missing values, removing outliers, and converting variables.
3. **Exploratory Data Analysis (EDA)**: Explore relationships among variables through visualizations.
4. **Model Building**: Develop and evaluate linear regression models for price prediction.

# Data Collection
The dataset `ab.csv` includes features such as:
- Location (latitude, longitude)
- Room Type
- Minimum Nights
- Number of Reviews

# Data Preprocessing
Steps performed:
- **Removing Outliers**: Applied Z-scores to detect and remove outliers.
- **Log Transformation**: Transformed the target variable, price, using a log transformation.
- **Categorization**: Converted numerical variables into categorical groups.
- **Feature Selection**: Removed unused columns for model efficiency.

# Exploratory Data Analysis
Visualizations were created to investigate:
- Distribution of prices by neighborhood and room type.
- Correlation between number of reviews and listing prices.

# Model Building
Two models were developed:
1. **Simple Linear Regression**
2. **Multiple Linear Regression**

**The final model:**
```r
lm(formula = log_price ~ number_of_reviews + neighbourhood_group + room_type + 
    latitude + longitude + minimum_nights_group + availability_365, 
    data = ab_nyc_final)


Model Evaluation

**Performance metrics used:**

	•	R-Squared
	•	RMSE
	•	AIC

Plots compared actual and predicted values, validating model fit.

Conclusion:

This analysis identifies key factors influencing Airbnb listing prices in NYC and demonstrates the application of linear regression techniques for predictive analysis.
