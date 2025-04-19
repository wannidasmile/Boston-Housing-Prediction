# Boston-Housing-Prediction
This report investigates Boston’s residential real estate using data-driven methods to predict property values through both regression and classification techniques. The goal is to understand how factors like living area, remodel year, and neighborhood characteristics influence housing prices. By testing various machine learning models, the study aims to offer stakeholders actionable insights into the key drivers of value in the Boston housing market, ultimately guiding investment and planning decisions.

## Data Preparation
The dataset was prepared for both regression and classification tasks. For regression, categorical variables like condition, crime grade, and school quality were transformed into dummy variables. The target variable "TOTAL_VALUE" was retained as a continuous variable. For classification, it was converted into a binary label ("High" or "Low") based on the median value. The dataset was then split into 80% training and 20% testing sets to ensure unbiased model evaluation.

## Exploratory Data Analysis (EDA)
The EDA highlighted trends in property characteristics across Boston. The average home had around 3 bedrooms, 1.7 full baths, and one kitchen. Most properties were remodeled around the year 2000, reflecting recent modernization trends. Graphs showed that neighborhoods like Boston and Dorchester had the highest property counts, while luxury properties skewed value distributions. Correlation analysis revealed that living area had the strongest relationship to total value (r = 0.49), while remodel year and total rooms had moderate correlations.
![EDA](https://github.com/wannidasmile/Boston-Housing-Prediction/blob/main/Screenshot%202025-04-19%20184932.png)
![Pair Plot for Correlation Matrix]
