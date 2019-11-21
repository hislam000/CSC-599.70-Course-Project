# Intro to Data Science, Fall 2019 @ CCNY
# CSC-599.70-Course-Project 
# Professor Grant M. Long
Team Member & Name: RentAdvisor (3-Member)

# *DZHONIBEK PARMANKULOV*
# *HASIBUL ISLAM*
# *ABDUR RAFEY*
## Due November 23, 2019, 11:59pm: RentAdvisor.ipynb ###
CLICK Here: https://colab.research.google.com/drive/1Y2cKlUINbW7e-5iO-tLz6p88FMko8ku7

# *REPORT* #

# (i) Expected Performance of the Model
    To attain a formidable mean squared error for the rents of New York City apartments posted on StreetEasy, we intended to use a couple of models to initialize our tests. The first model we thought of using was Linear Regression. 

# Result: 
Mean Squared Error for Test1 using Linear Regression: 3313817.143868871

# The feature columns that we used to test this method were:

    feature_cols = ['bedrooms', 'year_built', 'bathrooms', 'min_to_subway',  'size_sqft', 'no_fee', 'has_doorman', 'Addr_zip', 'floor_count', 'has_gym', 'allows_pets',]

# We decided to eliminate the following features as they were beginning to increase the overall mean squared error:

    ['has_elevator', 'has_dishwasher', 'is_furnished', 'has_garage', 'has_pool', 'has_garden']

# Although this method provided an acceptable error, it was still not efficient enough as we want to deviate as far left of the 4.0 mark as we can. Next, we tried using the Random Forest Regressor and we obtained the following results: 

    Mean Squared Error for Test1 using Random Forest Regressor: 1851745.5923584981

# Thus,
     we were able to attain a much better result using the random forest method. This could be due to the large number of features that we taking into account. Generally, Linear Regression models can be useful for smaller ranges of continuous data. In this case, however, even though we are taking into account only one city, we have many features to handle, including numerous binary variables such as ‘has_doorman’ and ‘has_elevator’. Thus, as we move from one borough to another, more data is fed in and a random forest can handle messier data more efficiently than the regression model. 

    Another hidden factor that could be playing a role in this could be the fact that Linear Regressions require normalization to avoid overfitting, whereas Random Forest has this built-in.   

# ----------------------------------------------
# (ii) Intended Strategy to improve the predictions
    For the final submission, we intend to 
