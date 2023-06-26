# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Tanya Mohanka

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I realized that in order to submit my prediction I have to check that there is no negative value in my submission. Even if there was a negative value we set it to zero before submission.

### What was the top ranked model that performed?
The top ranked model was WeightedEnsemble_L3 with the score -52.556431.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I used the datetime features to separate out the datetime into hour, day, or month parts.I did an exploratory data analysis by creating a histogram to show the distribution of all features.By using these new features, I could analyse the bike demand by hour of the day, day of the week, and month of the year to discover new information pattern.

### How much better did your model preform after adding additional features and why do you think that is?
The initial RMSE score from the first model is 1.84. By using the additional features I managed to significantly improve the model and gained the score of 0.65.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
I tried to further improved the model by tuning the hyperparameters. I specified hyperparameter values for LightGBM models. I also set the hyperparameter_tune_kwargs by playing around with num_trials, scheduler, and searcher hyperparameters.

### If you were given more time with this dataset, where do you think you would spend more time?
 I would try to explore the dataset and create additional features, and try more options on the hyperparameter tunings.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|eval_metrics|time_limit|presets|num_bag_sets|individual model parameters|score| |--|--|--|--|--| 
|initial|RMSE|600|best_quality|None|None|1.79| 
|add_features|RMSE|600|best_quality|None|None|0.65| 
|hpo|RMSE|900|best_quality|1|None|0.49|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![image](https://github.com/Tanya-1109/Bike-Sharing-Demand-with-Autogluon/assets/107848751/93cb138b-e8f3-4bc5-bb5e-0430973d3f1e)



### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![image](https://github.com/Tanya-1109/Bike-Sharing-Demand-with-Autogluon/assets/107848751/8731c686-65d6-4818-bdb7-ec9e76d87e0a)


## Summary
This project is a great way for me to have a hands-on experience in building a machine learning model. I practice each aspect of ML workflow and build a model to predict the bike sharing demand using AutoGluon. I also learned how we could start by creating a baseline model using default parameters as an initial experiment, how to further improve the model with EDA and feature engineering, and perform hyperparameter tuning to optimize the model. I learned a lot from this project and I am excited to learn more.
