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
  - Bal. Accuracy Rep.: 0.65
  - Precision:          0.99
  - Recall:             0.61

   ![naive](/naive.png)
  
### SMOTE
  - Bal. Accuracy Rep.: 0.66
  - Precision:          0.99
  - Recall:             0.69

   ![smote](/smote.png)

### SMOTE Oversampling
  - Bal. Accuracy Rep.: 0.66
  - Precision:          0.99
  - Recall:             0.69

   ![smote](/smote.png)

### Undersampling
  - Bal. Accuracy Rep.: 0.58
  - Precision:          0.99
  - Recall:             0.58

   ![under](/under.png)
   
### Combination (Over and Under) Sampling
  - Bal. Accuracy Rep.: 0.64
  - Precision:          0.99
  - Recall:             0.57

   ![combi](/combi.png)   
   
### Balanced Random Forest Classifier
  - Bal. Accuracy Rep.: 0.79
  - Precision:          0.99
  - Recall:             0.87

   ![BRF](/BRF.png)   

### Easy Ensemble AdaBoost Classifier
  - Bal. Accuracy Rep.: 0.93
  - Precision:          0.99
  - Recall:             0.94

   ![EEC](/EEC.png)   
  
## Summary

Looking at the results, we can conclude that there is in fact a positivity bias for reviews in the Vine program (47.06% against 31.69% non-Vine reviews).  A possible reason is the fact that unpaid reviewers tend to be more critic, while participants tend to be more constructive.

One additional analysis that could be done with the dataset is using machine learnimg validate the rating against the written reviews, and get more insight from the these reviews.
