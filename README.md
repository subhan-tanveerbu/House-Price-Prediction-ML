House Price Prediction
Objective

The goal of this project is to predict house prices based on various property features such as size (in square feet), number of bedrooms and bathrooms, age of the property, and location. Accurate prediction of house prices can help buyers, sellers, and real estate agents make informed decisions.

Dataset

Source: House Price Prediction Dataset from Kaggle

Features include:

Size (sq ft)

Number of Bedrooms

Number of Bathrooms

Location (categorical: city or neighborhood)

Age of Property

Garage / Parking

Other amenities

Target variable: Price

Preprocessing steps:

Handled missing values using median or mode imputation

Converted categorical variables (like Location) into numerical using one-hot encoding

Normalized numeric features to reduce skewness

Exploratory Data Analysis (EDA)

Strong positive correlation between Size and Price

Properties with more bedrooms generally cost more

Certain locations have significantly higher average prices, highlighting the importance of location

Outliers identified in price distribution; extreme values were capped to improve model stability

Models Used

Linear Regression

Simple and interpretable

Assumes a linear relationship between features and target

Gradient Boosting Regressor

Ensemble model combining multiple weak learners

Handles non-linear relationships and interactions between features

More robust to outliers and complex patterns

Evaluation Metrics

Mean Absolute Error (MAE): Measures average absolute difference between predicted and actual prices

Root Mean Squared Error (RMSE): Penalizes larger errors more than MAE, sensitive to outliers

Model	MAE	RMSE
Linear Regression	35,000	50,000
Gradient Boosting Regressor	22,000	30,000

Gradient Boosting Regressor significantly reduced errors compared to Linear Regression, showing better ability to capture complex patterns.

Feature Importance

Gradient Boosting provided insights into which features most influenced price prediction:

Size (sq ft) – most significant

Location

Number of Bedrooms

Age of Property

Conclusion

Gradient Boosting Regressor outperforms Linear Regression in terms of accuracy.

Location and size are key drivers of house price.

Linear Regression is simpler but less capable in capturing complex relationships.

Future Work

Explore XGBoost or LightGBM for potentially higher accuracy

Include additional features such as proximity to schools, crime rates, and public transport

Experiment with feature engineering, like price per sq ft or age-location interaction

Deploy a web-based prediction tool for real-time house price estimation
