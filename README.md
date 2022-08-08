# Credit_Risk_Classification

## Overview of the Analysis

Credit risk poses a classification problem that’s inherently imbalanced, healthy loans easily outnumber risky loans. In this project I use various techniques to train and evaluate machine leaning models with imbalanced classes.

The lending data CSV file which was analysed contains various financial datapoints about borrowers which lead to a classification of them as either having a healthy loan or a high-risk loan. Initially the data is split into features (financial datapoints) labelled X, and targets (whether a loan is healthy or high-risk) labelled y. The targets contained 75036 healthy loans and 2500 high-risk loans which indicates an imbalanced class problem which will be addressed later. Then the features and targets are split again in training and testing data. 

The training data was first fit on a Logistic Regression model and then the testing features are used to predict the testing targets. An accuracy score, confusion matrix and classification report are generated to assess the effectiveness of the model's predictions. 

Then in order to address the imbalanced class problem, a Random Oversampler model is used to over-sample the minority class by replacing samples at random until the amount of healthy and high-risk loans are even. Then this resampled data is fit to a Logistic Regression model again and an accuracy score, confusion matrix and classification report are generated for comparison. 

## Results

* Machine Learning Model 1:
    * The logistic regression model performs very well predicting the healthy loans with 100% precision and 99% recall. It has an overall accuracy of 95%. However when predicting the high-risk loans there is room for improvement with 85% precision and 91% recall. This is most likely due to the imbalanced classes.


* Machine Learning Model 2:
    * Once again the model predicts healthy loans very well with 100% precision and 99% recall. Also the overall accuracy has improved from 95% to 99%. Using the oversampled data has slightly decreased precision for high-risk loans by 1% but has improved the recall from 91% to 99% percent which is important as this minimises false negatives. 
    

## Summary

Based to these results I would suggest using the second model which includes Random Oversampling. The overall accuracy is improved with this model but most importantly, the recall relating to high-risk loans is improved from 91% to 99%. This minimises false negatives i.e. incorrectly labelling an actual high-risk loan as healthy which is important to avoid.  


