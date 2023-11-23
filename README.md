
# Taxi-trip-time-Prediction




## Problem Statement
More than 7 billion people exist on earth. With necessities of food, water and shelter there also a key requirement of commutating from one place to other. Rapid advancement in technology in the last two decades leads to adaption of a more efficient way of transportation via internet and app-based transport system. New York city is one of such advanced city with extensive use of transportation via subways, buses and taxi services. New York has more then 10,000 plus taxi and nearly 50% of population doesn’t have a personal vehicle. Due to this facts most people used taxi has a there primary mode of transport and it accounts for more than 100 millions taxi trips per year.

The main objective is to build a predictive model, which could help them in predicting the trip duration of taxi. This would in turn help them in matching the right cabs with the right customers quickly and efficiently.
## Data Overview
### Data Description:

The dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC). The data was sampled and cleaned for the purposes of this project. Based on individual trip attributes, you should predict the duration of each trip in the test set.



### Data fields:

* id - a unique identifier for each trip

* vendor_id - a code indicating the provider associated with the trip record

* pickup_datetime - date and time when the meter was engaged

* dropoff_datetime - date and time when the meter was disengaged

* passenger_count - the number of passengers in the vehicle (driver entered value)

* pickup_longitude - the longitude where the meter was engaged

* pickup_latitude - the latitude where the meter was engaged

* dropoff_longitude - the longitude where the meter was disengaged

* dropoff_latitude - the latitude where the meter was disengaged

* store_and_fwd_flag - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a connection to the server - Y=store and forward; N=not a store and forward trip 

* trip_duration - duration of the trip in seconds

## Approach

The following steps were followed in the project:

Data Preprocessing and cleaning: Done data preprocessing by converting some columns' datatypes , by adding some new columns and removimng outliers

Exploratory Data Analysis: Did Exploratory Analysis which includes Univariate as well as Bivariate Analysis.

Data Split: The preprocessed data was split into training and test sets on a random state of 0. By using training data we trained our predictive model and we used testing data to evaluate our prediction.

Model Training: The models were trained using the training data, and these models are optimized by some Hyperparameter settings.

Model Evaluation: The performance of the trained models was evaluated using metrics such as mean absolute error, root mean squared error, and R-squared. The model that performed the best on the test data was selected.

Model Deployment: The selected model was deployed in a live production setting, where it could make real-time predictions of bike demand. The model's performance was monitored over time to ensure its accuracy and usefulness.
## Models Used 
Models Used For modeling we tried various regression models such as 

1)Linear Regression

2)Random Forest

3)XG Boosting

All these models were fine tuned using a random search method with repeated cross-validation (CV) to ﬁnd the best hyperparameters. We also found out Feature importance so that we get to know about the features which are highly important.
## Result
We got the best model accuracy in Xgboost model,r2 score of 0.83 in test data..The RMSE score of Xgboost model is 0.28
## Conclusion

During our analysis, Firstly did data preprocessing by creating few columns . I cleaned the data and removed outliers. Then conducted an exploratory data analysis (EDA) on all the features in our dataset. I have done Monovariate and Bivariate analysis on these variables . I also studied the numerical variables, calculated their correlations, and the their relationships with the dependent variable. I also handled multicollinearity issue using VIF. I also done OneHotencoding by adding dummy columns .

I employed 3 machine learning algorithms including Linear Regression, Random Forest and XG Boosting . I also performed hyperparameter tuning to enhance the performance of our models.

### Some Facts:

1)Our base model (Linear Regression) gave us a r2_score of 0.65 in test data and keep this model accuracy in reference to compare other model.

2)We got the best model accuracy in Xgboost model,r2 score of 0.83 in test data..The RMSE score of Xgboost model is 0.28

3)Our second best model is RandomForest Regressor with a r2 score of 0.72 in test data. The RMSE score of random forest is 0.36

4)If we dont use proper hypertunning parameter for Random Forest , it gives overfitting issues and takes to much time to run.(Practical observation)

5)As far as data is concern , we can see that there is rise in trip duration and number of rides at the time of evening , this looks like some natural pattern because of the trafic issues .

6)Also there are more pickup numbers durig 4-6 pm in the evening. This is due to Closing office hours may be.

7)March is the month where most of the Taxi rides happen this cound be due to all salaries are created due to budget end month or else it can be due to vacations as well

8)Taxi trips are lowest on Mondays and comparatively low at sSundays as well.

9)On Sundays people prefer to stay at home other than going outside in the traffic.
## Output

![taxi](https://github.com/ady909/-Taxi-trip-time-Prediction/assets/57126736/085a8fc0-0a3b-4eab-89ab-7efe121ed844)

