# Capstone-Project-GDP-QOL

Capstone Project: GDP and its relationship with Quality of Life

__Goal:__

Our goal is to assess what indicators have a measurable impact on GDP or GDP per capita and build a model that can predict it effectively. 

As we are operating in an imperfect world, we assume that there are differences in the impact countries will experience from each factor. Thus, our main aim is not to simply predict GDP, but assess and attain insight into what a possible model to estimate GDP would rely on as predictors.

__Findings:__

We found that engaging in feature selection generally resulted in a less accurate model. What this means is that all of the factors play a small role in determining GDP, and we lose a piece of this picture, as we eliminate features. 

Our Random Forest and KNN models generally performed worse when reducing features. Upon transforming our data with PCA, it was found that we were able to slightly improve model performance over our previous (Random Forest & KNN) models, using a bagging regressor. PCA also allowed us to reduce our feature list from 16 to 3.

__Limitations:__

* Collapse of data: Due to the way in which we reduced the complexity of our data through collapsing of the timeseries (completed in part 2 of 3), we have overly simplified our data. It does not take into consideration seasonal, cyclical, and trend information. This doesn't mean that our results have no merit, however, it does mean that our model shouldn't be used as an accurate predictor of GDP per capita.
* Removal of outliers: A great deal of outliers exist in reality. Although we have kept a great deal of outliers to mimic actual conditions, we have eliminated extreme cases to make our model function better. 
* Imputation/Removal of nulls: We removed a number of observations that contained null values greater than 3 in our imputation phase (part 2 of 3)*

Assumption
If Imputation of values greater than 20% is required (Greater than 3.6 missing values),  an observation could result in being too artificial and reduce the efficacy or application of our model

*Dropped Haiti and all countries with greater than 3 missing values