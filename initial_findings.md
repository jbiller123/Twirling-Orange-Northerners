In our part 1 of the project, we used multiple sklearn ensemble models in addition to a standard linear regression model. Comparatively, we saw that linear regression worked the best in regards to mean squared error for the test2.csv. Using GridSearch and RandomSearch we were able to explore different potential fit models for the RandomForest Regressor and our KNN regressor. However, these resulted in a higher mean squared error than Linear Regression in the end. Perhaps further fine tuning of the hyperparameters for our regression models could result in better MSE performance. Unfortunately, there was not much variation to be had in the features selected, however we utilized 'bedrooms', 'bathrooms', 'floor_count', 'size_sqft', 'has_washer_dryer', 'has_roofdeck', 'has_doorman', 'has_dishwasher' to form our test2 predictions. We also looked at some different methods of imputing the missing values from our target and test data. Ultimately, we utilized a standard mean method, however we would look to explore machine learning methods for imputing data like MICE from fancyimpute.

For the next part of our project, we have several ideas in mind in order to improve our performance. Given that, intuitively, the location of the residence is one of the major drivers of rent price we will attempt to use categorical data from our sets in order in addition to the features we used in round 1. This will mainly be neighborhood or borough, but not both due to the fact that these two are heavily correlated with each other. We will do this by encoding these features with one method or another such as one hot encoding, label encoding, etc. As mentioned we only experimented with hyperparameters with KNN and RSCV, for the next part we will see if we can achieve a more significant prediction by tweaking the hyperparameters of our most successful models. In addition we are looking for other datasets online that may bring another predictive factor we can train our models on. 


### Mean Squared Errors (Test 1)
| Model | Mean Squared Errors |
| ------ | ------ |
| Random Forest | 570364.2794636443|
| Bagging Regressor | 447217.7302967674 |
| Gradient Boosting | 2133050.236497565 |
| Ada Boost Regressor | 5835605.475630233 |
| KNN | 3197265.023415816 |
| Voting Regressor | 1347268.2668490182 |
| Linear Regression | 3680742.7922809115 |
| Randomized Search CV | 2290575.5521978405 |
| Randomized Search CV (Best Params) | 2290575.5521978405 |

### Mean Squared Errors (Test 2)
| Model | Mean Squared Errors |
| ------ | ------ |
| Random Forest | 7469921.004313083 |
| Bagging Regressor | 7779442.2744454695|
| Gradient Boosting | 7469921.004313083 |
| Ada Boost Regressor | 12070655.83057286 |
| KNN | 5121476.26826033 |
| Voting Regressor | 6096437.819029653 |
| Linear Regression | 4765059.741542864 |
| Randomized Search CV | 6796516.256468636|
| Randomized Search CV (Best Params) | 6796516.256468636|

