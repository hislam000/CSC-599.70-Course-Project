# Intro to Data Science, Fall 2019 @ CCNY
    CSC59970 | CCNY
    Professor Grant M. Long
    Due December 7, 2019, 11:59pm

Team Member & Name: RentAdvisor (3-Member)
# *ABDUR RAFEY*
# *HASIBUL ISLAM*
# *DZHONIBEK PARMANKULOV*

- [X] Questions and Tasks
# (1) Data Usage.
(a) What outside data have you appended to the original data set? Why did you choose this data? 

- [X] We decided to append restaurant data. We used NYC Open data as data source, we used restaurant zip code to match the zip code of rental apartment and accordingly attached the restaurant zip code, restaurant name and restaurant grade.

(b) Does the inclusion of this additional data raise any ethical considerations? 

- [X] One ethical consideration could be that the zip codes act like a sector divider. Thus, we get an idea of the common rent prices in different areas of New York City, which gives an indication of the social classes of tanants living in those areas.

# (2) Data Exploration. 
(a) What outliers present issues for your analysis? How have you chosen to handle them? Why?

- [X] Outliers are luxury apartements with very high rent price and cheaply rented apartments.

(b) To what extent do missing values pose a challenge for your analysis? How have you chosen to handle them? Why?

- [X] Missing values effected our prediction model in negative way because it doesnt let us train with real values completely. Missing values do change the outlook of the conclusion of our analysis if not handled. We decided to use the median values of the other available data for the specific columns that had null values and filled them with those medians. We chose median over other statistics like mean because possible outliers don't have much affect at all on the median, whereas they can skew the mean quite a bit and possibly give a false analytical conclusion. We were planing to train model and predict missing values but didn`t have enough time.

(c) Are there any other aspects of the data your exploration shows might be problematic? 

- [X] The problem with our model is that, due to the missing data in the training set, we were forced to use medians of the available data to fill in the null values so our final results don't completely reflect what a perfect model would be like, but it is still fairly close to the actual results. 

(d) Create at least one visualization that demonstrates the predictive power of your data. 

- [X]![495a241f-1d0f-4908-a73d-069e94a2c2b8](https://user-images.githubusercontent.com/36207058/70367217-fe958300-186b-11ea-8402-a768fb6feae9.jpg)

# (3) Transformation and Modeling.
 (a) Describe 5-10 features you think play the biggest role in your model. 

- [X] These were the features that played the biggest role in our model

    - bedrooms
    - bathrooms
    - size_sqft
    - addr_zip
    - floor_count
  
  Num of bedrooms/bathrooms and floor_count had a positive correlation to the rent. 
  Also, the addr_zip is a feature we added to divide our data into sectors so we could see what incomes are most prevalent in    
  which areas.   
  
• How did you create these features? 

- [X] We created these features by importing the training dataset.

• How do you know these features are playing key roles? 

- [X] These features are playing key roles because as bedrooms or bathrooms increase, the rent goes up, especially size_sqft.Also OLS table give us and idea which variable effects the outcome most. 

(b) Describe how you are implementing your model. Why do you think this works well? 

- [X] WE are implementing it using features we chose and predicting the target which is rent. Initial training dataset with 12000 rental records and then we predcted 2000 records of test data to check for accuracy/mean squared error.

(c) Describe your methodology for selecting your model. Why do you think this type of model works well? 

- [X] Initially we started by using Linear Regression because we knew that we had continuous data to work with so that seemed too be the best option. Later, we tried Random Forest Tree and it gave a much smaller Mean Squared Error result due to its ability to navigate through more complex and larger datasets. With this idea in mind, we decided to try Gradient boosting Regressor and it worked in a very similar method and gave a slightly better result thus for submission of test3 rent we predicted using Ensemble Gradient Boosting REgressor.

# (4) Metrics, Validation, and Evaluation. 
(a) How well do you think you model will perform on the hold out test set? How do you know? 

- [X] Linear Regression:
  Mean Squared Error using Linear Regression: 3313817.143868871
---------------------------------------------------------------- 
- [X] Random Forest:
  Mean Squared Error using Random Forest Regressor: 1883630.165411068
-----------------------------------------------------------------------
- [X] Gradient Boosting:
  Mean Squared Error using GradientBoostingRegressor: 1720228.7848562498
--------------------------------------------------------------------------
We think our model would perform fairly well on the hold out test set. Based on the results for each model we tried, we got closer to a perfect score of 1, so our model was pretty consistent and our mean squared error decreased with each trial and gradient boosting gave the best results.   

(b) Is your model useful? Why or why not? 

- [X] Our model is useful as its variables correlate with each other at a fairly consistent rate based on the R-squared value.  

(c) Are there any special cases in which your model works particularly well or particularly poorly? 

- [X] Our model works well on rentals with average rent price, but it is poorer for luxury rentals. 


(d) Create at least one visualization that demonstrates the predictive power of your model. 

- [X]  Linear Regression:
  Explained variance regression score function
  Best possible score is 1.0, lower values are worse.
  0.5559738486087318

  R^2 (coefficient of determination) regression score function:
  0.5556196902015677
-------------------------------------------------------    
- [X] Random Forest:
  Explained variance regression score function
  Best possible score is 1.0, lower values are worse.
  0.7474068681056247

  R^2 (coefficient of determination) regression score function:
  0.7474066551922682
-------------------------------------------------------
******************************************************************
- [X] Gradient Boosting:
  Explained variance regression score function
  Best possible score is 1.0, lower values are worse.
  0.7693223390436726

 - [X] R^2 (coefficient of determination) regression score function:
  0.7693186536399759
******************************************************************  
# (5) Conclusion 
(a) How would you use this model? 

- [X] After analyzing our models accuracy, We can use this model to predict the rent for test3. 
We can use this model to determine if one sector of NYC would be best suited to your needs depending on the contributing environmental factors of that apartment location. For example, a higher rent based on better restaurants or close train stations can be seen differently from higher rent based on number of bedrooms/bathrooms. 

(b) If you could have additional modeling features, what would they be? 

- [X] Since we are mostly taking into account environmental factors as the additional data for our experiment, we could also choose to use number of playgrounds near apartment or best rated schools near apartment if the tenants have children. 

(c) Would you rather have more data, or more features?

- [X] We would rather have more data because having more data can bring the accuracy closer to the expected value.After adding extra data into our  model could produce better results. This is similar to the law of large numbers. As you perform more tests you get closer to an expected value.  
