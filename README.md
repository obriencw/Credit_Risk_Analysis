# Credit_Risk_Analysis

## Overview of the Analysis
This project revolves around the process of using financial technology for approving or declining loans.  The purpose of this analysis was to use python and Scikit-learn to build and evaluate several machine learning models to predict credit risk.  In this analysis, we also compare the strengths and weaknesses of different machine learning models.  Finally, we assess how well a model classifies and predicts data.
## Results
For this analysis, we used the credit card dataset from LendingClub to predict credit risk.  From this data, we applied several different machine learning models and analyzed the results to determine which model was the most accurate at predicting credit risk.
The first model we applied to the data was the Random Oversampler.  The results of this model are outlined below.
- Accuracy Score = 66.48%
- Precision High Risk = 0.01
- Recall High Risk = 0.73
- Precision Low Risk = 1.00
- Recall Low Risk = 0.60

![Oversampling](/naive_random_oversampling.PNG)

The second model we applied to the data was the Smote Over Sampler.  The results of this model are outlined below.
- Accuracy Score = 64.48%
- Precision High Risk = 0.01
- Recall High Risk = 0.72
- Precision Low Risk = 1.00
- Recall Low Risk = 0.57

![Smote Oversampling](/smote_oversampling.PNG)

The next model we applied to the data was the Random Under Sampler.  The results of this model are outlined below.
- Accuracy Score = 64.48%
- Precision High Risk = 0.01
- Recall High Risk = 0.66
- Precision Low Risk = 1.00
- Recall Low Risk = 0.54

![Undersampling](/undersampling.PNG)

The next model we applied to the data was the combination sampler SMOTEENN.  The results of this model are outlined below.
- Accuracy Score = 64.48%
- Precision High Risk = 0.01
- Recall High Risk = 0.72
- Precision Low Risk = 1.00
- Recall Low Risk = 0.57

![Smoteen](/smoteen.PNG)

The next model we applied to the data was the Balanced Random Forest Classifier.  The results of this model are outlined below.
- Accuracy Score = 0.60%
- Precision High Risk = 0.01
- Recall High Risk = 1.00
- Precision Low Risk = 0.00
- Recall Low Risk = 0.00

![BRF](/balanced_random_forest.PNG)

The final model we applied to the data was the Easy Ensemble AdaBoost Classifier.  The results of this model are outlined below.
- Accuracy Score = 94.12%
- Precision High Risk = 0.09
- Recall High Risk = 0.89
- Precision Low Risk = 0.94
- Recall Low Risk = 0.00

![EEC](/easy_ensemble_classifier.PNG)

## Summary
When we analyze the results of the various machine learning models that we tested, there is no clear model that stands out as the best.  While the Easy Ensemble Classifier model returned the highest accuracy score of all the models, the score for precision of high risk applicants was far too low to recommend using this model.  The combination SMOTEENN sampler had an accuracy score that was too low for us to recommend this model.  The remaining models tested all returned similar accuracy scores with those scores ranging from 64.48% - 66.48% and all had identical precision scores for both high risk and low risk applicants.  Of these models, the random oversampling model had the highest socres for recall of high risk applicants and recall of low risk applicants; combined with the fact that this model had the highest accuracy score of the remaining models means that the Random Over Sampler model is the model that we would recommend using for this particular dataset.  