# Rusty Bargain Car Price Prediction
![Car Sales](carsales.png)
## Project Overview
Rusty Bargain, a used car sales service, is developing a mobile app to help customers quickly estimate the market value of their cars. This project involves building a machine learning model that accurately predicts car prices based on historical data, including technical specifications, trim versions, and other relevant features. The model must balance quality, speed of prediction, and training time, making it a critical component for the app's success.

## Project Objectives
- Quality of Prediction: Develop a model that provides accurate price predictions using the RMSE (Root Mean Square Error) as the evaluation metric.
- Speed of Prediction: Ensure that the model's predictions are generated quickly to enhance user experience.
- Training Time: Optimize the training process to minimize time without compromising the model's accuracy.

## Data Description
The dataset contains various features related to cars, including:

- DateCrawled: Date the profile was downloaded from the database
- VehicleType: Type of vehicle body
- RegistrationYear: Year the vehicle was registered
- Gearbox: Type of gearbox
- Power: Power of the car in horsepower (hp)
- Model: Vehicle model
- Mileage: Mileage in kilometers
- RegistrationMonth: Month of registration
- FuelType: Type of fuel used
- Brand: Vehicle brand
- NotRepaired: Indicates if the vehicle has been repaired or not
- DateCreated: Date the profile was created
- NumberOfPictures: Number of pictures available for the vehicle
- PostalCode: Postal code of the profile owner
- LastSeen: Date of the last activity from the user
- Price (Target): The price of the vehicle in Euros

## Methodology
- Data Preprocessing
- Data Cleaning: Handled missing values, inconsistent data, and irrelevant features to ensure a clean dataset.
- Feature Engineering: Created new features and transformed existing ones to improve model performance.
- Encoding: Applied appropriate encoding techniques for categorical variables to ensure compatibility with machine learning models.
- Model Training & Evaluation

Multiple models were trained and evaluated using the RMSE metric to determine the best approach for predicting car prices:

Random Forest:

- Best Parameters: {'n_estimators': 200, 'max_depth': 25}
- Training Time: 696.2977 seconds
- Prediction Time: 3.3918 seconds
- RMSE: 1452.4524

LightGBM:

- Best Parameters: {'num_leaves': 50, 'max_depth': 20, 'learning_rate': 0.05, 'n_estimators': 200, 'min_child_samples': 30, 'subsample': 0.8, 'colsample_bytree': 0.8, 'reg_alpha': 0.1, 'reg_lambda': 0.1}
- RMSE: 1475.0054

CatBoost:

- Best Parameters: {'iterations': 200, 'depth': 8, 'learning_rate': 0.05, 'l2_leaf_reg': 3, 'border_count': 50, 'bagging_temperature': 0.5}
- Training Time: 5.8202 seconds
- Prediction Time: 0.0488 seconds
- RMSE: 1493.9498

Results:
- Random Forest was the most accurate model with an RMSE of 1452.4524, making it the recommended choice for predicting car prices.
- LightGBM offered a strong performance with an RMSE of 1475.0054 and faster training times.
- CatBoost was the fastest in terms of both training (5.8202 seconds) and prediction (0.0488 seconds) times, but with a slightly higher RMSE of 1493.9498.

Conclusion:
- The Random Forest model stands out as the best performer, delivering the highest accuracy for car price predictions. LightGBM provides a good balance between accuracy and training efficiency, while CatBoost excels in speed, making it suitable for real-time applications where quick predictions are critical.

## Future Work
- Further hyperparameter tuning and feature engineering can be explored to improve model performance.
- Incorporating additional data sources or external factors (e.g., market trends) may enhance the model's predictive capabilities.

## Skills Demonstrated
- Machine Learning: Proficient in training and evaluating various machine learning models, including Random Forest, LightGBM, and CatBoost.
- Data Processing: Expertise in data cleaning, feature engineering, and encoding techniques.
- Model Evaluation: Strong ability to assess models using appropriate metrics (e.g., RMSE) and optimize them for performance.
- Efficient Programming: Experience with handling large datasets and optimizing computational resources for model training and prediction.
