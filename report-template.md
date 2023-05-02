# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  * The purpose of the analysis was to see if the computer algorithm can analyze and make data-driven recommendations by training and evaluating a model based on loan-risk.

* Explain what financial information the data was on, and what you needed to predict.
  * We used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
  * With this model we were trying to predict which loans would be healthy and which would not be healthy, so that we can objectivly identify with confidence who is a good candidate to give a loan out to. We did this by looking at the "loan_status column" in the data frame. 

* Describe the stages of the machine learning process you went through as part of this analysis. Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
  -  Create labels and features
  - Check balance of our target values
  - Train, Test and Split the data
  - Create Logistic Regresion model with original data
  - Make predictions for original data set 
  - Evaluate performance:
    - Calculate the accuracy score of the model.
    - Generate a confusion matrix.
    - Print the classification report.
  - Use random oversampler model to generate new data set
  - Create Logistic Regresion model with oversampled data
  - Make predictions for oversampled data set 
  - Evaluate performance and compare with original data:
    - Calculate the accuracy score of the model.
    - Generate a confusion matrix.
    - Print the classification report.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
           

             precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.89      0.88       625

            accuracy                            0.99     19384
            macro avg       0.94      0.94      0.94     19384
            weighted avg    0.99      0.99      0.99     19384

  * balanced accuracy score: 0.9442676901753825 

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
            
            precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      1.00      0.93       625

            accuracy                             1.00     19384
            macro avg        0.94      1.00      0.96     19384
            weighted avg     1.00      1.00      1.00     19384

  * balanced accuracy score: 0.9959744975744975 


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?

 * The second oversampled model performs the best. I used two main features to ideantify this, the accuracy and the recall both improved. The accuracy is so important because it tells us generally how right we are. This is a nice indicator, but we cannot ignore false negatives and false posistives that can affect the values. That is why we also look at recall. Recall tells us about how well the model identifies true positives and at 1.00, that means that it did an excellent job. 

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

 * Healthy loans being identified as a non-healthy loan would be costly for a lending company as it is lost potential revenue, a loan that they should've given out but didn't. Non-Healthy loans being identified as a healthy loan would costly for a lending company becasue they are backing someone who cannot truly support what thy were given and the bank may never recover the funds. With this, I would say the bank loses more when non-healthy loans are deemed healthy. They profit off successful loans by collecting interest rates, if a non-healthy loan falls through, then the bank goes in the hole or sends it to a collection agency. I think they would rather risk losing potential revenue, than losing revenue that they were planning to have.

* If you do not recommend any of the models, please justify your reasoning.
