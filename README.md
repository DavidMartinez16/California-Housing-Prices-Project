# California Housing Prices Estimator: Project Overview

_This is a project where I create some machine learning models in order to predict the value of a house in California by analyzing features as total rooms, total bedrooms, ocean proximity, median income, housing median age, among others._

* [Dataset](https://www.kaggle.com/camnugent/california-housing-prices) - The used dataset was downloaded from the kaggle repository
* Created a machine learning model that estimates the price of a house in California by analyzing different features.
* The evaluated models were Linear Regression, Polynomial Regression, K-Nearest Neighbors and Random Forest. The selected model was the RF which obtained the best performance, with a 10-Fold Cross Validation Score grater than 78 %. 

## Code and Resources Used 🛠️

* **Python Version:** 3.7
* **Packages:** Pandas, Numpy, Matplotlib, Seaborn and Sklearn
* **Scraper Project:** https://www.kaggle.com/manisood001/california-housing-optimised-modelling

## Features of the data 📦
_The following are the features contained in the California Housing Price Dataset :_

* **Median House Value (Target Variable)**
* Longitude           
* Latitude            
* Housing Median Age  
* Total Rooms         
* Total Bedrooms      
* Population          
* Households         
* Median Income       
* Ocean Proximity 

## Data Cleaning

* Replace the missing values in total rooms column for the median of the same column
* Remove the outliers in the median house value and population columns
* Save the processed data

## EDA

_Verify the correlation between the features with the house price_
![cm](https://user-images.githubusercontent.com/63115543/91671102-425ea580-eae9-11ea-9d14-c17f91e127b1.jpg)

_Boxplot of the median house value and ocean proximity_ 
![img1](https://user-images.githubusercontent.com/63115543/91671138-7afe7f00-eae9-11ea-8b42-9425f73e3711.jpg)

_Plot the number of houses according to the age group_
![img2](https://user-images.githubusercontent.com/63115543/91671157-af723b00-eae9-11ea-8f00-7caa9ee2e16d.jpg)

## Model Building

First , I split the data into train and test sets with a test size of 20 %. Then i tried four different models and evaluated them using the 10-Fold Cross Validation Score.

The models i tried are the following models with the respective cv score:

* **Linear Regression:** 61.22 %
* **Polynomial Regression:** 61.22 %
* **K-Nearest Neighbors:** 67.93 %
* **Random Forest:** 78.60 %

The i proceeded to tune the model using the GridSearchCV function

## Model Tunning

According with the GridSearchCV function the best parameters for the Random Forest model are 'max_depth'= 9 and 'n_estimators'= 5.  It's important to mention that there are no more higher parameters due to computational cost, and probably with higher values the performance of the model will improve.

Finally, i decided to plot the feature importance of this model
![img3](https://user-images.githubusercontent.com/63115543/91671305-2a882100-eaeb-11ea-9bf3-cdcb410395a4.jpg)

And the R-Squared value for this model was: **74.28 %**.

The performance of the model with the testing data is no the best, however, this could improve if the number of estimators and the max depth of the trees is higher, in fact, if tunning the model with more parameters probably you'll get a better model than this.
