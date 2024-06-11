
Business Problem Overview:
This project involves predicting quarterly sales for a steel manufacturer with various business clients in Auto, Metal Fabrication, and Infrastructure. The dataset includes company-specific financial indicators and general economic indicators. The goal is to accurately predict sales using a variety of machine learning models and techniques.

Dataset:
The dataset consists of the following features:

ID: Unique identifier for each row.
Company: Name of the company/customer.
Quarter: Quarter for which sales data is provided or to be predicted.
QuickRatio: Indicator of the customer’s liquidity.
InventoryRatio: Ratio of sales over inventory.
RevenueGrowth: Projected revenue growth.
MarketshareChange: Projected market share growth.
Bond rating: Bond rating of the company.
Stock rating: Stock rating of the company.
Region: Region where the company operates.
Industry: Industry area of the company.
Sales: Target variable, sales for the given quarter.
Economic Indicators: Including Consumer Sentiment, Interest Rate, PMI, Money Supply, NationalEAI, EastEAI, WestEAI, SouthEAI, and NorthEAI.
Approach and Submissions:
Here’s a summary of the various models and approaches used, along with their respective performance metrics and insights:

Basic Linear Regression Model: Replacing missing values with median, resulted in:

Train MAE: 1284.6
Validation MAE: 1866.7
Test MAE: 1634.4

Categorical Data Handling: Created dummy variables, leading to significant improvement:

Train MAE: 730.1
Validation MAE: 974.5
Test MAE: 872.94

Outlier Removal: Identified via boxplots, resulting in similar performance:

Train MAE: 716.4
Validation MAE: 973.4
Test MAE: 878.92

4-6. Feature Selection: Backward elimination improved feature selection:

Train MAE: 725.5
Validation MAE: 988.1
Test MAE: 884.15

7-8. Decision Tree Model: Performance declined on validation and test sets:

Train MAE: 143.6
Validation MAE: 1806.6
Test MAE: 1701.8

Random Forest: Improved over Decision Tree:

Train MAE: 105.8
Validation MAE: 1089.4
Test MAE: 1352.7

10-11. Incorporation of Economic Indicators: Led to overfitting issues:

Train MAE: 820.4
Validation MAE: 850.7
Test MAE: 2281.6
12-14. XGBoost and Feature Reduction: Mixed results:

Test MAE: 836.94
Further reduction didn't help significantly.
15-18. Ridge Regression with Regularization: Improved performance:

Train MAE: 815.4
Validation MAE: 884.6
Test MAE: 819.14

19-22. Advanced Validation Techniques: Used k-fold and bootstrapping:

Improved generalization and performance consistency.
23-26. Scaling Techniques: MinMaxScaler, PowerTransformer:

Test MAE: 850.69
PowerTransformer proved beneficial.

27-31. Ensemble Methods and Hyperparameter Tuning: Random Forest and Gradient Boosting:

Varied performance, best results from PowerTransformer + Ridge Regression:

Test MAE: 728.74

Final Insights and Recommendations:
Feature Engineering: Creating dummy variables for categorical features and combining rare categories improved the model.
Scaling: PowerTransform scaling stabilized the model performance.
Regularization: Ridge Regression with regularization provided the best results, preventing overfitting.
Validation Techniques: Bootstrapping and k-fold validation helped in reducing overfitting and assessing model performance.
Economic Indicators: While useful, they led to overfitting when added without careful consideration.
