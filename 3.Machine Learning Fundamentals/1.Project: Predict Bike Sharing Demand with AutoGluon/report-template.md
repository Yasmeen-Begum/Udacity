# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Yasmeen Begum

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I have tried in both google-colab and in Amazon sagemaker studio .I had some trouble starting the tasks on my local environment and I decided to do everything in the SageMaker studio and while in the beginning I get scores of above 1.7 and i managed to improve my results and get a score of below 1.3 

### What was the top ranked model that performed?
My top score was achieved my the completing the second  run with more features but no tuning og hyperparameters. The score was 0.70291.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I managed to derive from the distriutions that the temperature categories were normally distributed. The datetime needed to be split into more features and I chose to split it into year, month, day and hour which is what improve my model the most. About the season I suppose that we see the four seasons in the distribution and it is the same for the weather which has three categories of input. Workday and holiday are both binary fields and humidity are right and windspeed are left skewed respectively.

### How much better did your model preform after adding additional features and why do you think that is?
The model performed much better than the initial model but a little bit worse than the improvement with just the features. 

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The best improvement was because of the split of the datetime field into  year,month, day and hour and the result in based in my opinion on the. It imporved the model by 50%.

### If you were given more time with this dataset, where do you think you would spend more time?
I would try to figure out more ways to improve on the features as they seem to be the ones that lead to improvement of the score. Maybe some one-hot encoding or adjusting for the seasons or working hours will provide us with a better result.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|timelimit (seconds)|presets|others|score|
|--|--|--|--|--|
|initial|600|best_quality|-|1.79833|
|add_features|600|best_quality|-|0.70291|
|hpo|720|best_quality|nn:activation -- dropout_prob; gmb:num_boost_round -- num_leaves; scheduler; searcher|1.33318|
### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score](https://github.com/Yasmeen-Begum/Udacity/assets/91931504/146dee1f-fe91-40e5-86bc-3de15768e680)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.
![model_test_score](https://github.com/Yasmeen-Begum/Udacity/assets/91931504/ce1eef4a-e61c-456d-9e94-234d33fbc2e2)

## Summary
The most benefit is received by working with the features and you can gain great insights from the EDA.  My goal would be to improve the model by taking into consideration the working hours which impact the bike demand and the seasonal spikes.I have got score of  1.33318  
