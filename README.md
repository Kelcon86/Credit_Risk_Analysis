# Credit_Risk_Analysis

## Overview of the analysis
For this challenge I used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling to identify credit card risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. 

Using six machine learning models and the credit card dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combined approach of over- and undersampling using the SMOTEENN algorithm. I then compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. After evaluating the performance of these models in the conclusion, I made my recommendation on which one should be used to predict credit risk.

## Results

### Naive Random Oversampling

<img width="455" alt="BalancedAccuracyScore_NaiveRandomOversampling" src="https://user-images.githubusercontent.com/60076980/164895059-7b3a0746-133c-4528-b7d3-85ad540288e7.png">
<img width="726" alt="RandomOversampling_Report" src="https://user-images.githubusercontent.com/60076980/164895981-953e2ffd-7629-44d9-bf29-805ee9a76988.png">

- The balanced accuracy score for this model was 65%
- The precision score for high risk individuals was 1% with a recall score of 61%
- The precision score for low risk individuals was 100% with a recall score of 68%
- The overall average precision score was 99% with a recall score of 68%

### SMOTE Oversampling

<img width="371" alt="BalancedAccuracyScore_SMOTEOversampling" src="https://user-images.githubusercontent.com/60076980/164895139-fc629980-1ed5-4d47-aab4-8c87b87190c5.png">
<img width="752" alt="SMOTE_Report" src="https://user-images.githubusercontent.com/60076980/164895985-90be6be3-1362-4206-919f-6dafa9f8e703.png">

- The balanced accuracy score for this model was 52%
- The precision score for high risk individuals was 1% with a recall score of 61%
- The precision score for low risk individuals was 100% with a recall score of 64%
- The overall average precision score was 99% with a recall score of 64%

### Cluster Centroids

<img width="383" alt="BalancedAccuraryScore_ClusterCentroids" src="https://user-images.githubusercontent.com/60076980/164895324-bcd80c84-0871-4e8d-a7b3-5312af9c0df6.png">
<img width="723" alt="ClusterCentroids_Report" src="https://user-images.githubusercontent.com/60076980/164896030-9a0485e3-402e-4fd3-94e7-1af832f6f4c9.png">

- The balanced accuracy score for this model was 62%
- The precision score for high risk individuals was 1% with a recall score of 61%
- The precision score for low risk individuals was 100% with a recall score of 43%
- The overall average precision score was 99% with a recall score of 43%

### SMOTEENN

<img width="386" alt="BalancedAccuracyScore_SMOTEENN" src="https://user-images.githubusercontent.com/60076980/164895380-56fa13a6-69cf-4379-8862-60808a69058a.png">
<img width="759" alt="SMOTEENN_Report" src="https://user-images.githubusercontent.com/60076980/164896069-6eda4974-3521-4b5f-abb8-6f6bcdcc7d69.png">

- The balanced accuracy score for this model was 62%
- The precision score for high risk individuals was 1% with a recall score of 69%
- The precision score for low risk individuals was 100% with a recall score of 54%
- The overall average precision score was 99% with a recall score of 54%

### Balanced Random Forest Classifier

<img width="362" alt="BalancedAccuracyScore_BRFC" src="https://user-images.githubusercontent.com/60076980/164894911-5500be97-ebdb-40e0-8858-237a13666ab6.png">
<img width="718" alt="BalancedRandomForest_Report" src="https://user-images.githubusercontent.com/60076980/164896128-910746b2-49cf-43dc-b673-8024e1d19983.png">

- The balanced accuracy score for this model was 79%
- The precision score for high risk individuals was 4% with a recall score of 67%
- The precision score for low risk individuals was 100% with a recall score of 91%
- The overall average precision score was 99% with a recall score of 91%

### Easy Ensemble AdaBoost Classifier

<img width="366" alt="BalancedAccuracyScore_EasyEnsemble" src="https://user-images.githubusercontent.com/60076980/164894988-4c7d3fd4-0412-4278-9b79-e8cea5b1b4fc.png">
<img width="725" alt="EasyEnsemble_Report" src="https://user-images.githubusercontent.com/60076980/164896174-9714bc21-0a80-46b5-82b6-b2909411626b.png">

- The balanced accuracy score for this model was 93%
- The precision score for high risk individuals was 7% with a recall score of 91%
- The precision score for low risk individuals was 100% with a recall score of 94%
- The overall average precision score was 99% with a recall score of 94%

## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
The SMOTE model had the lowest balanced accuracy score at 52%. The Cluster Centroids and SMOTEENN models both had balanced accuracy scores of 62%, while the Naive Random Oversampling model was only slightly higher at 65%. Models 5 and 6 had the highest balanced accuracy scores at 79% for the Balanced Random Forest Classifier model and 93% for the Easy Ensemble AdaBoost Classifier.

I recommend the Easy Ensemble AdaBoost Classifier for predicting credit risk for individuals. The model had an accuracy score of 93%, the highest of all six models I tested.
