
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

Final Insights and Recommendations:

Feature Engineering: Creating dummy variables for categorical features and combining rare categories improved the model.

Scaling: PowerTransform scaling stabilized the model performance.

Regularization: Ridge Regression with regularization provided the best results, preventing overfitting.

Validation Techniques: Bootstrapping and k-fold validation helped in reducing overfitting and assessing model performance.

Economic Indicators: While useful, they led to overfitting when added without careful consideration.
