# Credit Risk Analysis
  Analysis of credit risk on a loans portfolio.
  
## Overview of the analysis
In 2019, more than 19 million Americans had at least one unsecured personal loan. That's a record-breaking number! Personal lending is growing faster than credit card, auto, mortgage, and even student debt. With such incredible growth, FinTech firms are storming ahead of traditional loan processes. By using the latest machine learning techniques, these FinTech firms can continuously analyze large amounts of data and predict trends to optimize lending.

We will use Python to build and evaluate several machine learning models to predict credit risk. Being able to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud.
  
We will employ different techniques to train and evaluate models with unbalanced classes.  We will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once we are done, we will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

The following outpits will be produced:

- Use Resampling Models to Predict Credit Risk
- Use the SMOTEENN Algorithm to Predict Credit Risk
- Use Ensemble Classifiers to Predict Credit Risk
- A Written Report on the Credit Risk Analysis (README.md)

## Resources
- Data Source: LoanStats_2019Q1.csv file
- Software: Python, SKLearn, ImbLearn, Pandas, Numpy, Jupyter Notebook

## Results
We analysed different models, and below we present the balanced accuracy, precision and recall scores for each of them:

### Naive Random Oversampling
  - Bal. Accuracy: 0.65
  - Precision:     0.99
  - Recall:        0.61

   ![naive](/naive.png)
  
### SMOTE Oversampling
  - Bal. Accuracy: 0.66
  - Precision:     0.99
  - Recall:        0.69

   ![smote](/smote.png)

### Undersampling
  - Bal. Accuracy: 0.58
  - Precision:     0.99
  - Recall:        0.58

   ![under](/under.png)
   
### Combination (Over and Under) Sampling
  - Bal. Accuracy: 0.64
  - Precision:     0.99
  - Recall:        0.57

   ![combi](/combi.png)   
   
### Balanced Random Forest Classifier
  - Bal. Accuracy: 0.79
  - Precision:     0.99
  - Recall:        0.87

   ![BRF](/BRF.png)   

### Easy Ensemble AdaBoost Classifier
  - Bal. Accuracy: 0.93
  - Precision:     0.99
  - Recall:        0.94

   ![EEC](/EEC.png)   
  
## Summary

Please find below a summary table of all analysis:

Model | Bal Accy | Precision | Recall
--- | --- | --- | --
NRO | 0.65 | 0.99 |0.61
SMOTE | 0.66 | 0.99 | 0,69
Undersampling | 0.58 | 0.99 | 0.58
Combination | 0.64 | 0.99 | 0.57
BRF | 0.79 | 0.99 | 0.87
EEC | 0.93 | 0.99 | 0.94

Looking at the results, we can conclude that we have high precision scores for all models, since given data assymetry, not many low risk are predicted as high risk.  However we can see a lot of difference in the models through the recall score, which shows the ability of finding all positive high risk samples.

Therefore, we recommend using Easy Ensemble AdaBoost Classifier, since it ensemblse AdaBoost learners trained on different balanced boostrap samples, increasing the ability of finding positive high risk samples, providing the highest ballanced accuracy score.

In the other hand we don't recommed for this exercise the use of undersampling, since it involves loss of data from the majority class, decreasing even more the recall rate, and therefore, the ballanced accuracy score.
