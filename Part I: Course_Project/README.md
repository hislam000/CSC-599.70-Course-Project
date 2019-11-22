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

# *REPORT* #

# (i) Expected Performance of the Model
    To attain a formidable mean squared error for the rents of New York City apartments posted on StreetEasy, we intended to use a couple of models to initialize our tests. The first model we thought of using was Linear Regression. 

# Mean Squared Error for Test1 using Linear Regression: 
     3313817.143868871

# The feature columns that we used to test this method were:

    feature_cols = ['bedrooms', 'year_built', 'bathrooms', 'min_to_subway',  'size_sqft', 'no_fee', 'has_doorman', 'Addr_zip', 'floor_count', 'has_gym', 'allows_pets',]

# We decided to eliminate the following features as they were beginning to increase the overall mean squared error:

    ['has_elevator', 'has_dishwasher', 'is_furnished', 'has_garage', 'has_pool', 'has_garden']

# Although 
    This method provided an acceptable error, it was still not efficient enough as we want to deviate as far left of the 4.0 mark as we can. Next, we tried using the Random Forest Regressor and we obtained the following results: 

# Mean Squared Error for Test1 using Random Forest Regressor: 
    1851745.5923584981

# Thus
     We were able to attain a much better result using the random forest method. This could be due to the large number of features that we taking into account. Generally, Linear Regression models can be useful for smaller ranges of continuous data. In this case, however, even though we are taking into account only one city, we have many features to handle, including numerous binary variables such as ‘has_doorman’ and ‘has_elevator’. Thus, as we move from one borough to another, more data is fed in and a random forest can handle messier data more efficiently than the regression model. 

    Another hidden factor that could be playing a role in this could be the fact that Linear Regressions require normalization to avoid overfitting, whereas Random Forest has this built-in.   

# --------------------------------------------------------
# (ii) Intended Strategy to improve the predictions
    For the final submission, we intend to improve our results by using more models for predicting larger datasets because we intend to add some additional data and functions. We are also planning to include popular restaurant spots or grocery shopping locations and see if those variables can be used to predict a higher or lower rent for each location. The k-nearest neighbors algorithm is one that we intend to feed our data to. However, since this algorithm can use both classification data and continuous data for regressions, we may fit the variables or separate them in such a way so that we run a separate compilation for classification variables and leave the continuous variables for a regression format of this algorithm. 

# Graphs for training data: 
![1](https://user-images.githubusercontent.com/36207058/69293321-8c1f7480-0bd6-11ea-9981-b41a9fd7c10e.png)
![2](https://user-images.githubusercontent.com/36207058/69293326-8de93800-0bd6-11ea-88aa-4346334a178b.png)
![33](https://user-images.githubusercontent.com/36207058/69293327-904b9200-0bd6-11ea-9d7a-8ecae9bb8649.png)
![4](https://user-images.githubusercontent.com/36207058/69293333-92adec00-0bd6-11ea-86dd-7e55cc1e21a1.png)
![5](https://user-images.githubusercontent.com/36207058/69293336-9477af80-0bd6-11ea-9561-1f2e7028ec24.png)
![6](https://user-images.githubusercontent.com/36207058/69293341-96da0980-0bd6-11ea-976c-5262106548a8.png)

# Graphs for test 2 data: 
![11](https://user-images.githubusercontent.com/36207058/69293419-cdb01f80-0bd6-11ea-9d9a-c7ed0c5ca086.png)
![22](https://user-images.githubusercontent.com/36207058/69293421-cf79e300-0bd6-11ea-9c66-dbdcedd59065.png)
![333](https://user-images.githubusercontent.com/36207058/69293423-d0ab1000-0bd6-11ea-8028-c3b3752ef921.png)

![44](https://user-images.githubusercontent.com/36207058/69293425-d1dc3d00-0bd6-11ea-8757-375c5afe43c2.png)
![55](https://user-images.githubusercontent.com/36207058/69293427-d30d6a00-0bd6-11ea-9617-35517d6c2845.png)
![66](https://user-images.githubusercontent.com/36207058/69293428-d3a60080-0bd6-11ea-8bdc-cf80a5f2a9d2.png)


# OLS Regression Results for Training Data: 
![1](https://user-images.githubusercontent.com/36207058/69293525-1ec01380-0bd7-11ea-896a-c6adcf24ce22.png)

# OLS Regression Results for Test2 Data: 
![2](https://user-images.githubusercontent.com/36207058/69293527-1f58aa00-0bd7-11ea-92c6-5fa201dc14fa.png)

