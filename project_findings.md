# Questions and Tasks

(1) Data Usage.
- (a) What outside data have you appended to the original data set? Why did you choose this data?
- (b) Does the inclusion of this additional data raise any ethical considerations?

(2) Data Exploration.
- (a) What outliers present issues for your analysis? How have you chosen to handle them? Why?
- (b) To what extent do missing values pose a challenge for your analysis? How have you chosen to
handle them? Why?
- (c) Are there any other aspects of the data your exploration shows might be problematic?
- (d) Create at least one visualization that demonstrates the predictive power of your data.

(3) Transformation and Modeling.
- (a) Describe 5 features you think play the biggest role in your model.
• How did you create these features?
• How do you know these features are playing key roles?
If your modeling process uses less than five features, explain why you think other features didn’t
add value.

- (b) Describe how you are implementing your model. Why do you think this works well?
- (c) Describe your methodology for selecting your model. Why do you think this type of model works
well?

(4) Metrics, Validation, and Evaluation.
- (a) How well do you think you model will perform on the hold out test set? How do you know?
- (b) Is your model useful? Why or why not?
- (c) Are there any special cases in which your model works particularly well or particularly poorly?
- (d) Create at least one visualization that demonstrates the predictive power of your model.

(5) Conclusion
- (a) How would you use this model?
- (b) If you could have additional modeling features, what would they be?
- (c) Would you rather have more data, or more features?


# Answers

1. Additional data was used to append to our original datasets to help our predictions. The main data we added includes the building value, number of units, population within that area, and median income of each Borough. Essentially our data sets gives us some insight on how Boroughs perform overall when it comes to real estate property. Since rent and property prices are heavily associated with the location it's in, it makes sense to bring in data regarding each borough for more accurate predictions. There are some ethical considerations for the dataset we are using, for example the median income of each borough can be seen as problematic in an ethical sense. 

2. The main outliers that were problematic for our analysis were the values that the missing/null values which we chose to impute in order to cover for them. Since our goal is to be able to predict prices for each Rental ID (or row), we cannot choose to simply drop the rows with null values. Meaning our only option is to impute and utilize artificial values, which we have done using the median and mean values for that column. While this lets us use generalized values for the outliers, a better approach would have been to find relational trends between the missing values and a different column without missing values. Another problematic aspect of our data is that we attempted to use categorical values using pd.get_dummies in order to use them for our models. This may not be the best way to utilize these values compared to other encoding methods. 

3. The main features we utilized are known to be directly related to a property's rent value, for example the number of bedrooms, bathrooms, general size of the property, as well as any extra benefits such as a doorman or dishwasher. In developing the model we use for our prediction, we experimented with various different models and utilized them in the same training and tests to determine effectiveness using the resulting mean squared error. From there we experimented with different features asa well as tuning the hyperparameters of each model to try to achieve a better MSE and as a result, a better model for our predictions. 

4. Our model may not be the most accurate when it comes to directly calculating prices, but should be effective enough in predicting a rent price within a reasonable range. After testing our different models we checked a portion of the predicted prices within the resulting spreadsheet to see if they were reasonable given the properties of that rental id. Since we had missing values in several features that we utilized, our model is not as strong when it comes to those properties as we had to impute values for them. In these cases, our predictive model may work rather poorly compared to other rental properties where no value had to be substituted for. 

5. We can use our model to ballpark a price on a particular piece of property given the features we chose from the dataset. While the accuracy of our model may not perform too well, it should at least be effective enough to detect a general trend. For example how much the value of the property may increase compared to other rental ideas, or a rough estimate of how much the property's value will increase in general. Additional modeling features we would've liked to have is perhaps the past prices of the properties over the last few years to check for a general trend to help our prediction. There are also other aspects of estate property's that may be more influential than those present in our dataset such as the number of schools nearby, income of residents within the neighborhood, building material such as wood flooring or brick walls. While having both more data and features would be ideal, features would most likely be more effective than more data. This is due to the fact that our goal is to predict house prices, and we are missing other important features that are taken into consideration when purchasing a house. 
