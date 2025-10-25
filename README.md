# ESG_Funding_Prediction

This project explores how Environmental, Social, and Governance (ESG) performance and financial metrics can be used to predict funding allocation for companies.

## What this notebook does
- Engineers features from ESG scores (Environmental, Social, Governance) and financial indicators (Revenue, Profit).
- Builds interaction terms like `Profit × Social Score` to capture how strong ESG PLUS good financials affects funding decisions.
- Trains and tunes multiple machine learning models:
  - Linear Regression
  - Random Forest Regressor
  - Gradient Boosting
  - XGBoost
  - Support Vector Regressor (SVR)
  - Neural Network (MLP)
  - Stacking Regressor (ensemble)
- Compares performance using R², MAE, MSE, RMSE.
- Extracts feature importance to understand what actually drives funding.

## Key result
A tuned Random Forest model explains ~86% of the variance in funding received.  
The most important predictors are combinations of profitability and ESG strength (for example, `Profit × Social Score`), suggesting that investors/funders tend to reward companies that are both financially strong and performing well on ESG.

## Data privacy notice
The dataset used in this analysis includes confidential ESG, financial, and funding information.  
It is **not included** in this public repository.

To run the notebook yourself:
1. Prepare your own dataset with similar columns, e.g.  
   - Environmental Score  
   - Social Score  
   - Governance Score  
   - Revenue (in million $)  
   - Profit (in million $)  
   - Funding Received (in million $)
2. Save it locally (not committed to GitHub), e.g. `data/Cleaned_ESG_Data2.csv`
3. Update the `DATA_PATH` / `cleaned_data_path` variable in the notebook to point to your local file.

Raw `.csv` data is intentionally excluded.

