# Intro to Data Science, Fall 2019 @ CCNY
    CSC-599.70-Course-Project 
    Professor Grant M. Long
Team Member & Name: RentAdvisor (3-Member)
# *ABDUR RAFEY*
# *HASIBUL ISLAM*
# *DZHONIBEK PARMANKULOV*

# --------------------------------------------------------
# Due November 23, 2019, 11:59pm: RentAdvisor.ipynb 
Click: https://colab.research.google.com/drive/1Y2cKlUINbW7e-5iO-tLz6p88FMko8ku7


# (i) Expected Performance of the Model

To attain a formidable mean squared error for the rents of New York City apartments posted on StreetEasy, we intended to use a couple of models to initialize our tests. The first model we thought of using was Linear Regression. 

Mean Squared Error for Test1 using Linear Regression: 3313817.143868871

The feature columns that we used to test this method were:

feature_cols = ['bedrooms', 'year_built', 'bathrooms', 'min_to_subway',  'size_sqft', 'no_fee', 'has_doorman', 'Addr_zip', 'floor_count', 'has_gym', 'allows_pets',]

We decided to eliminate the following features as they were beginning to increase the overall mean squared error:

['has_elevator', 'has_dishwasher', 'is_furnished', 'has_garage', 'has_pool', 'has_garden']

Although this method provided an acceptable error, it was still not efficient enough as we want to deviate as far left of the 4.0 mark as we can. Next, we tried using the Random Forest Regressor and we obtained the following results: 

Mean Squared Error for Test1 using Random Forest Regressor: 1851745.5923584981

Thus, we were able to attain a much better result using the random forest method. This could be due to the large number of features that we taking into account. Generally, Linear Regression models can be useful for smaller ranges of continuous data. In this case, however, even though we are taking into account only one city, we have many features to handle, including numerous binary variables such as ‘has_doorman’ and ‘has_elevator’. Thus, as we move from one borough to another, more data is fed in and a random forest can handle messier data more efficiently than the regression model. Another hidden factor that could be playing a role in this could be the fact that Linear Regressions require normalization to avoid overfitting, whereas Random Forest has this built-in.   


# (ii) Intended Strategy to improve the predictions

For the final submission, we intend to improve our results by using more models for predicting larger datasets because we intend to add some additional data and functions. We are planning to include popular restaurant spots or grocery shopping locations and see if those variables can be used to predict a higher or lower rent for each location. One of the algorithms we intend to feed our data to is the k-nearest neighbors algorithm. However, since this algorithm can use both classification data and continuous data for regressions, we may fit the variables or separate them in such a way so that we run a separate compilation for classification variables and leave the continuous variables for a regression format of this algorithm. As we use this algorithm against test 3, we will be looking to see how the continuous variables are being predicted compared to our Linear Regression results. In this manner, we can fairly compare each variable with its equal counterpart and see how the classification, binary variables affect the total rental prediction output and the mean squared error with each test run. Afterwards, we will follow the same sequence of steps as our run against test 2 and generate tables and plots of our concluding results.    

# Graphs for training data: 
![Screen Shot 2019-11-22 at 3 28 08 PM](https://user-images.githubusercontent.com/36207058/69458154-bab75f80-0d3c-11ea-8dac-4c2a3a1b9059.png)
![Screen Shot 2019-11-22 at 3 28 19 PM](https://user-images.githubusercontent.com/36207058/69458158-bbe88c80-0d3c-11ea-92f3-4bd79b2433a5.png)
![Screen Shot 2019-11-22 at 3 28 39 PM](https://user-images.githubusercontent.com/36207058/69458175-c4d95e00-0d3c-11ea-9c90-2ff8945a909b.png)
![Screen Shot 2019-11-22 at 3 29 06 PM](https://user-images.githubusercontent.com/36207058/69458220-dcb0e200-0d3c-11ea-9ab5-12cb13e6081e.png)
![Screen Shot 2019-11-22 at 3 29 15 PM](https://user-images.githubusercontent.com/36207058/69458224-dde20f00-0d3c-11ea-9e1e-e2a870510970.png)
![Screen Shot 2019-11-22 at 3 29 34 PM](https://user-images.githubusercontent.com/36207058/69458247-e63a4a00-0d3c-11ea-9ece-75699bb4564d.png)

