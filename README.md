# Credit_Risk_Analysis

## Overview of the analysis
The purpose of this analysis is to predict credit risk using Machine Learning algorithms based on a set of features. The intention is to find good candidates for loans which will lead to low loan default rates. Different machine learning models were used for the task and their results were compared by calculating their precision and recall scores.

## Results
### Logistic Regression
I started with a logistic regression classification model to predict credit risk. Credit risk is an unbalanced classification problem as good loans outnumber bad ones. To get more accurate results, I resampled the training data to include more instances of bad loans. I did this using four methods: Random Oversampling, SMOTE, clustercentroids and SMOTEEN.

<strong>Random Oversampling</strong></br>
The logistic regression with random oversampling model had the following metrics.
 - Balanced Accuracy: 0.677
 - Precision and Recall: This model predicted high risk datapoints with a precision of 0.01 and a recall of 0.76 </br>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/RandomOversampling.PNG?raw=true">
 
<strong>SMOTE Oversampling</strong></br>
The logistic regression with SMOTE model had the following metrics.
 - Balanced Accuracy: 0.662
 - Precision and Recall: This model predicted high risk datapoints with a precision of 0.01 and a recall of 0.63 </br>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/SMOTE.PNG?raw=true">
 
<strong>Clustercentroids Undersampling</strong></br>
The logistic regression with clustercentroids oversampling model had the following metrics.
 - Balanced Accuracy: 0.662
  - Precision and Recall: This model predicted high risk datapoints with a precision of 0.01 and a recall of 0.69 </br>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/Cluster.PNG?raw=true">
 
<strong>SMOTEEN sampling</strong></br>
The logistic regression with SMOTEEN model had the following metrics.
 - Balanced Accuracy: 0.640
  - Precision and Recall: This model predicted high risk datapoints with a precision of 0.01 and a recall of 0.70 </br>r>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/SMOTEEN.PNG?raw=true">
   
 ### Ensemble Classifiers
 I also used two ensemble classifier models to predict credit risk. These were: Balanced Random Forest Classfier and Easy Ensemble Classifier
 
 <strong>Random Forest Classifier</strong></br>
 The Random Forest Classifier had the following metrics:
 - Balanced Accuracy: 0.788
 - Precision and Recall: This model predicted high risk datapoints with a precision of 0.03 and a recall of 0.70 </br>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/rANDOMfOR.PNG?raw=true">
   
 <strong>Easy Ensemble Classifier</strong></br>
 The Easy Ensemble Classfier had the following metrics:
 - Balanced Accuracy: 0.931
 - Precision and Recall: This model predicted high risk datapoints with a precision of 0.09 and a recall of 0.92 </br>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/ADA.PNG?raw=true">


Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
