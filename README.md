# Credit Risk Classification
Train and evaluate a classification model based on loan risk for a finance company.

### Overview
To determine the credit worthiness of a borrower I will evaluate a model based on loan risk. I will use a dataset of historical activity from a peer-to-peer lending service provider for the model evaluation. To achieve this we will split the dataset into a training set (75%) and a test set (25%), train a LogisticRegression model, predict the values from the test set and evaluate the accuracy, precision, recall, false positives, and false negatives of the model. Next, we rebalance the training dataset using the immbalanced-learn library to create equal number of labels and retrain the model. Finally, I will compare the results of the two models and reccommend one of them.

### Results
1.  The logistic regression model on the original data has an overall accuracy of 99% and a balanced accuracy score of 95.44%. 
2. For Healthy loans (0) the model precision is at 100% while the recall is 99% with a 100% f1 score. However, the model does not perform as well for the High-Risk loans (1) predictions, the model precision drops to 85% and the f1 score to 88%. 
3. The recall is 99% and 91% for the healthy and high-risk bale predictions respectively. Type I or false postives are 0.55% and Type II or false negatives are 8.56% respectively.
4. The overall accuracy of the model with the oversampled data remains the same at 99%. The balanced accuracy score increased from 95% to 99% after resampling. 
5. The mean accuracy for the rebalanced training data and the hold out test data are at 99% suggesting the prediction results are good. 
6. The precision for healthy loans (0) is 100% and for high-risk loans (1) it drops to 84%.
7. The type 1 error or false positives is 0.62% and type 2 error or false negatives is 0.65%.
8. The model with rebalanced data (second model) has a higher balanced accuracy score (99%) as compared the model trained on the original dataset (95%). The overall false positives increases by 0.1% with the second model, however the type 2 errors or false negatives drop from 8.56% to 0.65%. 

### Summary
The model with the original data has 53 type 2 errors or false negatives or 8.56%, i.e. more borrowers were identified as credit risks when they are actually credit worthy as compared to the model with the rebalanced data, the false negative drops to 4 or 0.65%. With the rebalanced data, the model type 1 error or false postives increase by 0.1%, i.e. classifying a borrower as credit worthy when they are actually not increased. This might pose a risk to the company as they will end up lending money to more risky borrowers. However, considering the bigger drop in false negatives and higher balanced accuracy, I recommend the company use the model with the rebalanced data

