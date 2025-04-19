# Boston-Housing-Prediction
This report investigates Boston’s residential real estate using data-driven methods to predict property values through both regression and classification techniques. The goal is to understand how factors like living area, remodel year, and neighborhood characteristics influence housing prices. By testing various machine learning models, the study aims to offer stakeholders actionable insights into the key drivers of value in the Boston housing market, ultimately guiding investment and planning decisions.

## Data Preparation
The dataset was prepared for both regression and classification tasks. For regression, categorical variables like condition, crime grade, and school quality were transformed into dummy variables. The target variable "TOTAL_VALUE" was retained as a continuous variable. For classification, it was converted into a binary label ("High" or "Low") based on the median value. The dataset was then split into 80% training and 20% testing sets to ensure unbiased model evaluation.

## Exploratory Data Analysis (EDA)
The EDA highlighted trends in property characteristics across Boston. The average home had around 3 bedrooms, 1.7 full baths, and one kitchen. Most properties were remodeled around the year 2000, reflecting recent modernization trends. Graphs showed that neighborhoods like Boston and Dorchester had the highest property counts, while luxury properties skewed value distributions. Correlation analysis revealed that living area had the strongest relationship to total value (r = 0.49), while remodel year and total rooms had moderate correlations.
![EDA](https://github.com/wannidasmile/Boston-Housing-Prediction/blob/main/Screenshot%202025-04-19%20184932.png)
![Pair Plot for Correlation Matrix](https://github.com/wannidasmile/Boston-Housing-Prediction/blob/main/Picture2.png)

## Regression VS Classification Modelling
Three regression models—XGBoost, Random Forest, and Linear Regression—were evaluated. XGBoost showed the best balance of low error (MAE ≈ $214,770) and high R² (0.71), followed closely by Random Forest (R² = 0.776). Linear Regression had the weakest performance (R² = 0.574), tending to underestimate or overestimate mid-to-high values. Feature importance analysis revealed that crime rate and living area were the strongest predictors, while school quality had surprisingly little impact on property value.
For classification tasks, all four models were tested to classify homes as high or low value. Decision Tree and Logistic Regression showed fair accuracy (81% and 76% respectively), while Random Forest and XGBoost performed best with 82% accuracy and AUC scores of 0.91. Hyperparameter tuning slightly improved performance for all models. Feature importance analysis showed living area, year of remodel, and total rooms as top contributors, with crime rate and school quality having moderate influence.
![DT](https://github.com/wannidasmile/Boston-Housing-Prediction/blob/main/decisiontree.png)

## Comparison
Comparing models, Random Forest and XGBoost clearly outperformed Linear Regression in regression tasks, while also leading in classification with higher accuracy and AUC. In regression, XGBoost had the lowest error rates, but Random Forest had the highest R² (0.776). In classification, both ensemble models scored 82% accuracy and 0.91 AUC, with Decision Tree and Logistic Regression trailing slightly behind. These results highlight the superior performance of ensemble methods in handling diverse housing data.
![ROC](https://github.com/wannidasmile/Boston-Housing-Prediction/blob/main/roc.png)
