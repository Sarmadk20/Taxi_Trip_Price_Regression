# Taxi_Trip_Price_Regression

# Taxi Trip Pricing Prediction

## Task Objective
The main objective of this project is to develop and evaluate machine learning models to accurately predict taxi trip prices based on various trip attributes, including distance, time, traffic conditions, weather, and more.

## Dataset Used
- **Source:** Local CSV file (`taxi_trip_pricing.csv`)
- **Features Include:**
  - Trip_Distance_km
  - Time_of_Day
  - Day_of_Week
  - Passenger_Count
  - Traffic_Conditions
  - Weather
  - Base_Fare
  - Per_Km_Rate
  - Per_Minute_Rate
  - Trip_Duration_Minutes
  - Trip_Price
- The dataset contains some missing values (NaN) in columns such as distance, base fare, and rates, which were appropriately handled during preprocessing.

## Models Applied
The following regression models were trained and evaluated for trip price prediction:
- **RandomForestRegressor**
- **KNeighborsRegressor** (for k values: 1, 5, 10)
- **Support Vector Regression (SVM)**
- **GradientBoostingRegressor**
- **AdaBoostRegressor**

## Key Results and Findings

| Model                      | MAE   | MSE    | R²    |
|----------------------------|-------|--------|-------|
| RandomForestRegressor      | 6.03  | 75.74  | 0.88  |
| KNeighborsRegressor (k=1)  | 16.65 | 445.94 | 0.30  |
| KNeighborsRegressor (k=5)  | 13.42 | 277.72 | 0.56  |
| KNeighborsRegressor (k=10) | 13.03 | 267.89 | 0.58  |
| SVM                        | 8.55  | 132.62 | 0.79  |
| GradientBoostingRegressor  | 5.38  | 66.61  | 0.90  |
| AdaBoostRegressor          | 9.83  | 143.99 | 0.77  |

- **GradientBoostingRegressor achieved the best performance**, with the lowest errors and highest R² score, indicating it explains 90% of the variation in taxi trip prices.
- **RandomForestRegressor** also performed very well and is robust with good generalization.
- **KNeighborsRegressor** showed significantly inferior performance for all k values, indicating it is not ideal for this regression task.
- **SVM and AdaBoostRegressor** provided reasonable predictions but were outperformed by ensemble tree methods.

## Final Insights
Tree-based ensemble models (especially GradientBoostingRegressor and RandomForestRegressor) are best suited for predicting taxi trip prices in this dataset. Further improvements could include feature engineering, hyperparameter tuning, and in-depth analysis of feature importance.



