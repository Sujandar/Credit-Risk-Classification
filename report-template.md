# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The analysis aims to evaluate the likelihood of default or late payment by borrowers. By applying classification models to historical credit data, the analysis predicts the credit risk associated with each borrower. This information helps lenders determine whether to approve or deny a loan application.

* Explain what financial information the data was on, and what you needed to predict.
The analysis utilized a dataset containing historical lending activity data from a peer-to-peer lending services company. The dataset included various financial information related to borrowers and credit applicants. Key variables in the dataset included income, employment status, credit history, debt-to-income ratio, loan amount, loan purpose, and other relevant financial indicators.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
In this analysis, the dependent variable, also known as the y value, was the "loan status." The loan status variable indicated whether a loan was classified as "healthy" or "at risk." This variable served as the target variable that we aimed to predict.

On the other hand, the independent variables, also referred to as the x values or features, included several key factors that could potentially influence the loan status. These independent variables were laon size, interest rate, borrowe income, debt-to-income ratio, number of accounts and derogatory marks.

* Describe the stages of the machine learning process you went through as part of this analysis.
In this analysis, the data was initially divided into training and test sets. Following the data split, the dependent and independent variables were defined. Subsequently, a logistic regression model was constructed and trained using the original dataset. The trained model was then employed to make predictions. Finally, the performance of the model was evaluated.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
Two Logistic Regression models were developed in this analysis using different datasets: one model was trained on the original dataset, while the other model was trained on a randomly oversampled dataset to address class imbalances. The models' performance and results, obtained using the scikit-learn library, were subsequently compared.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
Accuracy: The accuracy of the model was 0.99, indicating that it correctly predicted the loan status for 99% of the observations in the dataset.
Precision: For the class 0 (healthy loans), the precision was 1.00. This means that among the loans predicted as healthy, 100% of them were actually classified correctly. For the class 1 (at-risk loans), the precision was 0.84, indicating that 84% of the loans predicted as at-risk were correctly classified.
Recall: The recall for class 0 was 0.99, indicating that the model correctly identified 99% of the healthy loans. For class 1, the recall was 0.92, meaning that the model successfully identified 92% of the at-risk loans.


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
Accuracy: The accuracy of the model was 0.99, indicating that it correctly predicted the loan status for 99% of the observations in the dataset.
Precision: For the class 0 (healthy loans), the precision was 1.00. This means that among the loans predicted as healthy, 100% of them were actually classified correctly. For the class 1 (at-risk loans), the precision was 0.83, indicating that 83% of the loans predicted as at-risk were correctly classified.
Recall: The recall for class 0 was 0.99, indicating that the model correctly identified 99% of the healthy loans. For class 1, the recall was 1.00, meaning that the model successfully identified all the at-risk loans.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?

Looking at the accuracy scores, both Model 1 and Model 2 achieved an accuracy of 0.99, indicating a high level of correct predictions overall. Therefore, accuracy alone does not provide a clear distinction between the two models.

We can examine the precision and recall scores for each model.

For Model 1:
Precision for class 1 (at-risk loans): 0.84
Recall for class 1 (at-risk loans): 0.92

For Model 2:
Precision for class 1 (at-risk loans): 0.83
Recall for class 1 (at-risk loans): 1.00

Comparing these scores, we observe that Model 2 achieved a higher recall score of 1.00 for class 1, indicating that it correctly identified all at-risk loans in the dataset. In contrast, Model 1 had a lower recall score of 0.92 for class 1, indicating that it missed a small portion of the at-risk loans.

Based on this comparison, Model 2 appears to perform slightly better than Model 1 in terms of correctly identifying at-risk loans. Its perfect recall score for class 1 suggests that it does not miss any at-risk loans in the dataset.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Yes, the performance of a model can depend on the specific problem we are trying to solve and the priorities associated with it. The importance of correctly predicting the "1"s (in this case, the at-risk loans) versus the "0"s (healthy loans) can vary based on the context and objectives of the analysis.

In the context of credit risk classification, the relative importance of predicting the "1"s and "0"s may differ based on the business goals and considerations.

* If you do not recommend any of the models, please justify your reasoning.
N/A
