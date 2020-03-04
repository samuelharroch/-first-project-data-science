# project-data-science
In this project i worked on two datasets: Apple store and Race Result Horse.
## Apple Store visualization
On this data set i plot more than 12 graphs using matplotlib and seaborn functions in target to visualize the data. In most graphs the
goal was to find a connection between the features, and especially for the "user_rating" feature. 
 
## Race Result Horse

### Presentation of the data 
This data is the results of Hong Kong horse racing that took place between 2014 and 2016. In the notebook I explained a little about the
race and the procedures (rules). In addition, some of the explanations and data were presented by graphs. 

### Cleaning the data and filling nan values
Of course the notebook focuses on running machine learning models in order to predict a result as will be explained below.
Before running the models it was necessary to change the features values, with which we would predict the results, from object to numeric.
In addition, the cleaning of the data was performed mainly by an interpolation function for filling in nan values and by deleting 2 features (running_position_5, running_position_6) that more than half of the values were nan.

### Running Machine Learning Models

#### Classifying

The purpose of running the models is to predict the final position. Because most races have 14 final positions, it will be very difficult to predict the results for each horse very well, so I divided the final positions into two categories as is common to some bets: 1.0 - which is the top five places and 2.0 - the rest.

#### Choosing the features 

The selected features are 'draw', 'running_position_1', 'running_position_2', 'running_position_3', 'win_odds' as there is a connection between them and the classification (as we can see in the heat map) and because the reasons given in the notebook during the data explanation.

Features like 'horse_number',	'horse_name',	'horse_id	jockey',	'trainer',	'actual_weight',	'declared_horse_weight' were not selected because they do not contribute in predicting the result. 

Of course the 'length_behind_winner' feature was not selected because it already leads us to an even accurate result.
#### The Models 
The models selected are KNN - where i ran all the K's in the interval (1-30) and also used KFold and Cross Validation, Logistic Regression, Decision tree, Random Forest, Gaussian Naive Bayes and Support Vector Machine.
All models accuracies range from 0.76 to 0.80 , which is a good result, in relation to the distribution of the classification.
