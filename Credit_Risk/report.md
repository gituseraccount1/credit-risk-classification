# Module 20 Report Template

## Overview of the Analysis
We were given a dataset of historical lending activity from a company to build a model that can identify the creditworthiness of borrowers. The column we set as our “y” is the “loan_status” in our dataset. In the “loan_status” columns are 1s and 0s – 1s means the loan has ahigh risk of defaulting and 0s means the loan is healthy. We will then set our “X” as the other columns besides “loan_status.” Now we split the data into training and testing datasets using the train_test_split.

Model 1. We created a logistic regression model with the original data to see how well the logistic regression model predicts the creditworthiness of borrowers. The counts of 0s and 1s in the “loan_status” column in the original data were uneven (75036 counts of 0s and 2500 counts of 1s). First, we used the train data on the logistic regression model and then we save the predications for the test data. We then evaluated the regression model’s performance by generating a confusion matric and classification report. 

Model 2. We resample X and y’s using the RandomOverSampler from the imbalanced-learn library to make sure the counts of 1s (which was 2500) are the same as the counts of 0s (which was 75036). Then test and train the X and y’s again on the resampled X and y’s using the logistic regression model. The steps are the same as the Model 1 above, but on the resample X and y’s. We also use the confusion matric and classification report on this logistic regression model on the resampled X and y’s.



## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best? 
Overall it looks like model 2 performed the best since the accuracy score is 100 but model 1’s accuracy score is right behind it. 
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s?)
If you do not recommend any of the models, please justify your reasoning. The model is doing the best it can do with the dataset given to it. With these two models, it depends how important it is about using the actual data (when there are more 0s compared to 1s) or if resample (creating not original data) to get a better accuracy is better. It really depends on the situation but I would feel confident with model 1 since it was already quite high in accuracy (not 100%) on actual dataset given. 
