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
 I also used two ensemble classifier models to predict credit risk. These were: Balanced Random Forest Classifier and Easy Ensemble Classifier
 
 <strong>Random Forest Classifier</strong></br>
 The Random Forest Classifier had the following metrics:
 - Balanced Accuracy: 0.788
 - Precision and Recall: This model predicted high risk datapoints with a precision of 0.03 and a recall of 0.70 </br>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/rANDOMfOR.PNG?raw=true">
   
 <strong>Easy Ensemble Classifier</strong></br>
 The Easy Ensemble Classifier had the following metrics:
 - Balanced Accuracy: 0.931
 - Precision and Recall: This model predicted high risk datapoints with a precision of 0.09 and a recall of 0.92 </br>
   <img src = "https://github.com/Kee2u/Credit_Risk_Analysis/blob/main/Pictures/ADA.PNG?raw=true">


## Summary: 
### Balanced Accuracy: </br>
The Easy Ensemble classifier had the highest balanced accuracy at 93%. However, this number can be misleading in an unbalanced dataset. This model might just be performing well because it is predicting low risk applicants correctly. This is what we see in the precision and recall scores. 

### Precision: </br>
All the models had a very low precision for high risk applicants of < 10%. This means that the models assigned the high risk label to candidates that were not actually high risk.

### Recall: </br>
The Easy Ensemble Classifier algorithm had the highest recall for high risk applicants of 93%. This means that the model was good at detecting high risk applicants.

Going forward I would recommend using the Easy Ensemble Classifier but with caution. It was good at detecting high risk applicants, but it also generated a number of false positives (high risk label) to low risk applicants. The low risk candidates vastly outnumber the high risk ones so these false positives still allow the algorithm to detect low risk candidates with an F score of 97%. The results can be used as a recommendation to investigate potentially high risk candidates further.
