# Food Demand Forecasting

Here we have applied and compared multiple Time Series Models to get the best one to forecast food demand
Then use the forecast to create a useable dashboard to use the forecast for alarming OOS weeks and when to upstock

The data is taken from kaggle dataset: https://www.kaggle.com/datasets/kannanaikkal/food-demand-forecasting?select=train.csv

Here is the problem statement and data description as described in the kaggle problem:

## Context

It is a meal delivery company which operates in multiple cities. They have various fulfillment centers in these cities for dispatching meal orders to their customers. The client wants you to help these centers with demand forecasting for upcoming weeks so that these centers will plan the stock of raw materials accordingly.

## Content

The replenishment of majority of raw materials is done on weekly basis and since the raw material is perishable, the procurement planning is of utmost importance. Secondly, staffing of the centers is also one area wherein accurate demand forecasts are really helpful. Given the following information, the task is to predict the demand for the next 10 weeks (Weeks: 146-155) for the center-meal combinations in the test set

### Data Dictionary:

1. **Weekly Demand data (train.csv):** Contains the historical demand data for all centers, test.csv contains all the following features except the target variable

| Variable | Definition |
|----------|--------------|
| id | Unique ID |
| meal_id | Unique ID for Meal |
| checkout_price | Final price including discount, taxes & delivery charges |
| base_price | Base price of the meal |
| emailer_for_promotion | Emailer sent for promotion of meal |
| homepage_featured | Meal featured at homepage |
| num_orders | (Target) Orders Count |

2. **fulfilment_center_info.csv:** Contains information for each fulfilment center

| Variable | Definition |
|----------|--------------|
| center_id | Unique ID for fulfillment center |
| city_code | Unique code for city |
| region_code | Unique code for region |
| center_type | Anonymized center type |
| op_area | Area of operation (in km^2) |

3. **meal_info.csv:** Contains information for each meal being served

| Variable | Definition |
|----------|--------------|
| meal_id | Unique ID for the meal |
| category | Type of meal (beverages/snacks/soups….) |
| cuisine | Meal cuisine (Indian/Italian/…) |