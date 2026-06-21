# Sales & Demand Forecasting for Businesses

## Project Overview
This project forecasts monthly sales for a retail superstore using 4 years of historical order data (2015–2018), and translates the forecast into concrete business actions — not just numbers.

## Objective
Predict future sales/demand and present results in a clear, business-friendly way, while explicitly modeling trend **and** seasonality rather than just a flat trendline.

## Approach
- **Data cleaning:** checked and confirmed no missing values in the columns the model depends on
- **Feature engineering:** trend (month index) + seasonality (month-of-year, one-hot encoded) — without seasonality, retail forecasts miss holiday-season demand spikes entirely
- **Model:** Linear Regression
- **Evaluation:** chronological train/test split (last 6 months held out) — not evaluated on training data, so the error metric reflects real forecasting performance
- **Forecast:** 12 months ahead, visualized against historical actuals

## Results
- **Test MAE:** ~$14,681
- **Test MAPE:** ~17.7%
- Forecast shows a recurring seasonal pattern: low in Jan–Feb, peaking around Sept and Nov–Dec

## Business Impact
This forecast lets a store owner or manager plan inventory and staffing ahead of predicted demand peaks instead of reacting to them, and budget around realistic low-revenue months rather than treating them as anomalies.

## Tech Stack
Python · Pandas · NumPy · Scikit-learn · Matplotlib

## Files
- `sales_forecasting.ipynb` — full notebook, runs end-to-end with no manual file upload (data loads via GitHub raw URL)
- `train.csv` — Superstore sales dataset
