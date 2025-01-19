# USDA Nutrient Data Analysis Project

## Overview
This project involves analyzing nutrient data from two USDA datasets, focusing on macronutrients and micronutrients. The analysis includes data cleaning, visualization, statistical analysis, and predictive modeling to gain insights into the relationships between nutrients and their effects on food healthiness.

**Programming Language**: R

**Libraries**: `ggplot2`, `GGally`, `corrplot`

**Techniques**: Data cleaning, correlation analysis, linear regression, data visualization

This project demonstrates proficiency in data preprocessing, exploratory analysis, statistical modeling, and visualization using R, providing actionable insights into nutrient data.

## Project Goals
- Clean and organize the data.
- Perform exploratory data analysis and visualization.
- Identify relationships between nutrients.
- Build predictive models for calorie content and determine health metrics for food items.

## Key Steps

### 1. Data Preprocessing
- Read and merge the datasets on a common key.
- Handle missing values
- Convert non-numeric data into numeric formats (e.g., Sodium and Potassium).
- Create a cleaned dataset (`USDAclean`) for analysis.

### 2. Exploratory Data Analysis (EDA)
- **Highest Sodium Food**: Identified "Table Salt" as the food with the highest sodium level (38,758 mg).
- **Visualizations**:
  - Histogram for Vitamin C distribution.
  - Boxplot for Total Fat, Protein, and Carbohydrate distribution.
  - Scatterplot to illustrate the relationship between Total Fat and Calories.

### 3. Feature Engineering
- Added binary indicators for high sodium, calories, protein, sugar, and fat based on averages.
- Created a `HealthCheck` variable to classify foods as "Pass" or "Fail" based on high sodium, sugar, and fat content.

### 4. Statistical Analysis
- **Correlation Analysis**:
  - Visualized correlations among Calories, Protein, Total Fat, Carbohydrate, Sodium, and Cholesterol using a correlation plot.
- **Statistical Significance**:
  - Established that the correlation between Calories and Total Fat is statistically significant (p < 0.05).

### 5. Predictive Modeling
- Built a linear regression model to predict Calories based on Protein, Total Fat, Carbohydrate, Sodium, and Cholesterol.
- Identified Sodium as the least significant variable (p > 0.05).
- Created a refined model excluding Sodium, achieving better significance for predictors.

### 6. Insights
- **Impact of Carbohydrate Increase**:
  - A 10,000% increase in Carbohydrate content leads to a ~1083% increase in Calories, reflecting the direct proportionality in the model.
- **Protein, Total Fat, and Carbohydrate Relationships**:
  - Scatter plots and pair plots revealed strong positive relationships between these nutrients and calorie content.

### 7. Predictive Applications
- Predicted Calories for a new food product with specific nutrient values, estimating a caloric content of **1827.41 Calories**.
- Determined 1,827 foods in the cleaned dataset fail the `HealthCheck`.
