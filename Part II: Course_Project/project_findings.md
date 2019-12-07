# Intro to Data Science, Fall 2019 @ CCNY
    CSC59970 | CCNY
    Professor Grant M. Long
    Due December 7, 2019, 11:59pm

Team Member & Name: RentAdvisor (3-Member)
# *ABDUR RAFEY*
# *HASIBUL ISLAM*
# *DZHONIBEK PARMANKULOV*

    Questions and Tasks
# (1) Data Usage.
(a) What outside data have you appended to the original data set? Why did you choose this data? 

- We decided to append apartment zip codes and income. We wanted to use the zip codes to see if the income of tenants have anything to do with the rents at the areas. 

(b) Does the inclusion of this additional data raise any ethical considerations? 

- One ethical consideration could be that the zip codes act like a sector divider. Thus, we get an idea of the common rent prices in different areas of New York City, which gives an indication of the social classes of tanants living in those areas.

# (2) Data Exploration. 
(a) What outliers present issues for your analysis? How have you chosen to handle them? Why?

- 

(b) To what extent do missing values pose a challenge for your analysis? How have you chosen to handle them? Why?

- Missing values didn't really affect our results too much, but they do change the outlook of the conclusion of our analysis if not handled. We decided to use the median values of the other available data for the specific columns that had null values and filled them with those medians. We chose median over other statistics like mean because possible outliers don't have much affect at all on the median, whereas they can skew the mean quite a bit and possibly give a false analytical conclusion.    

(c) Are there any other aspects of the data your exploration shows might be problematic? 

-

(d) Create at least one visualization that demonstrates the predictive power of your data. 

-

# (3) Transformation and Modeling.
 (a) Describe 5-10 features you think play the biggest role in your model. 

- These were the features that played the biggest role in our model

    - bedrooms
    - bathrooms
    - size_sqft
    - addr_zip
    - floor_count
  
  Num of bedrooms/bathrooms and floor_count had a positive correlation to the rent. 
  Also, the addr_zip is a feature we added to divide our data into sectors so we could see what incomes are most prevalent in    
  which areas.   
  
• How did you create these features? 

- We created these features by importing the training dataset and for the zip codes, we used an external dataset from data.cityofnewyork.us.

• How do you know these features are playing key roles? 

- These features are playing key roles because as bedrooms or bathrooms increase, the rent goes up, especially in certain zip codes. Another feature to take into account is best nearest restaurant. We used grades of the best nearest restaurant to see how rent increases/decreases based on this feature. 

(b) Describe how you are implementing your model. Why do you think this works well? 

- 

(c) Describe your methodology for selecting your model. Why do you think this type of model works well? 

- Initially we started by using Linear Regression because we knew that we had continuous data to work with so that seemed too be the best option. Later, we tried Forest Tree and it gave a much smaller Mean Squared Error result due to its ability to navigate through more complex and larger datasets. With this idea in mind, we decided to use gradient boosting and it worked in a very similar method and gave a slightly better result. 

# (4) Metrics, Validation, and Evaluation. 
(a) How well do you think you model will perform on the hold out test set? How do you know? 

-


(b) Is your model useful? Why or why not? 

- 

(c) Are there any special cases in which your model works particularly well or particularly poorly? 

-


(d) Create at least one visualization that demonstrates the predictive power of your model. 

-

# (5) Conclusion 
(a) How would you use this model? 

- We can use this model to determine if one sector of NYC would be best suited to your needs depending on the contributing environmental factors of that apartment location. For example, a higher rent based on better restaurants or close train stations can be seen differently from higher rent based on number of bedrooms/bathrooms. 

(b) If you could have additional modeling features, what would they be? 

- Since we are mostly taking into account environmental factors as the additional data for our experiment, we could also choose to use number of playgrounds near apartment or best rated schools near apartment if the tenants have children. 

(c) Would you rather have more data, or more features?

- We would rather have more data because sometimes more data can give us an opportunity to test out more features and see the differences in the results if any. Also, having more data can also bring the accuracy closer to the expected value so using more features after adding extra data into a model could produce better results. This is similar to the law of large numbers. As you perform omre tests you get closer to an expected value.  
