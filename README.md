# Credit_Risk_Analysis

## Background/Overview
This peer-to-peer credit lending company is seeking to using machine learning as a way to better identify good candidates for giving loans in order to prevent loaning to candidates more likely to default. Machine learning is a tool that can make the loan application process much quicker for applicants. This in part because intant approval can be given for good candidates, poor candidates can be instantly denied, and only those that are in question need to be sent on for further review by a person. On the surface, this is a wonderful tool because it is able to remove biases that humans may have duringt the decision-making process. However, institutional racism along with general classism is a real issue within the economy and the abilities for individuals to be able to get and build credit, and due to these factors, machine learning often is unable to overcome the structure of society to identify candidates who happen to come from disadvantaged backgrounds[1]. This analysis does not address this aspect of machine learning as this is a foundational analysis. However, this should be considered a priority for addressing in future work. 

### Algorithms
For this analysis, 6 different algorithms were created to predict credit using resampling models and ensemble classifiers. Below are the algorithms used:

- RandomOverSampler (oversampling)
- SMOTE (oversampling)
- ClusterCentroids (undersampling)
- SMOTEENN (combination over and undesampling)
- BalancedRandomForestClassifier
- EasyEnsembleClassifier

### Main Objectives
This analysis is using the 6 algorithms above to tackle 3 main objectives:

1) Use the resampling models to predict credit risk and determine which one is best at doing so.
2) Use the SMOTEENN algorithm to predict credit risk, which is a combinatorial approach of both over and undersampling. Compare the results here to the resampling model results.
3) Use ensemble classifiers to predict credit risk using the BalancedRandomForestClassifier and EasyEnsembleClassifier. 

## Results
### 1 and 2) RandomOverSampler, SMOTE, ClusterCentroids, and SMOTEENN were the algorithms used for this objective. Between all of them, the SMOTEENN algorithm performed best (see the credit_risk_resampling.ipynb file for code). Below are the algorithm outcomes with SMOTEENN at the top of each performance category:


### Balanced Accuracy Score:
#### -  SMOTEENN
![SMOTEENN_BalancedAccuracyScore](https://user-images.githubusercontent.com/101941048/217343475-4b9bc987-38fe-4176-ac09-e3b7bf741fb5.png)

#### -  RandomOverSampler
![NaiveRandomOversampling_BalancedAccuracyScore](https://user-images.githubusercontent.com/101941048/217345819-49b6fc78-6c43-4a2b-9cdd-c88f1755b81e.png)

#### -  SMOTE
![SMOTE_BalancedAccuracyScore](https://user-images.githubusercontent.com/101941048/217346040-519ea975-db46-4211-9d70-7b0c460a97c0.png)

#### -  ClusterCentroids
![ClusterCentroids_BalancedAccuracyScore](https://user-images.githubusercontent.com/101941048/217346123-2bf979fe-61ca-4dfd-bae6-a1176a70f344.png)

### Confusion Matrix:
#### -  SMOTEENN
![SMOTEENN_ConfusionMatrix](https://user-images.githubusercontent.com/101941048/217343489-ff7d845b-c58a-4ed9-b9fa-7ef5c5a92c56.png)

#### -  RandomOverSampler
![NaiveRandomOversampling_ConfusionMatrix](https://user-images.githubusercontent.com/101941048/217345885-734b2882-4fb2-45da-b011-44e558dc1d7f.png)

#### -  SMOTE
![SMOTE_ConfusionMatrix](https://user-images.githubusercontent.com/101941048/217346070-2df67548-6f9c-4b25-9cdc-7ff033faee22.png)

#### -  ClusterCentroids
![ClusterCentroids_ConfusionMatrix](https://user-images.githubusercontent.com/101941048/217346156-9b686943-9941-44c5-b221-c484d7b3cc94.png)

### Classification Report Imbalanced:
#### -  SMOTEENN
![SMOTEENN_ClassificationReportImbalanced](https://user-images.githubusercontent.com/101941048/217343500-d11304c3-bf67-40c2-9205-cd52710ee922.png)

#### -  RandomOverSampler
![NaiveRandomOversampling_ClassificationReportImbalanced](https://user-images.githubusercontent.com/101941048/217345895-9a4f6fda-638c-4ad5-9aa5-c6d5aa7ec960.png)

#### -  SMOTE
![SMOTE_ClassificationReportImbalanced](https://user-images.githubusercontent.com/101941048/217346084-38f13ce0-3eb2-48db-856a-2f0d69c5b34d.png)

#### -  ClusterCentroids
![ClusterCentroids_ClassificationReportImbalanced](https://user-images.githubusercontent.com/101941048/217346179-cc46a39f-d108-4e81-b73a-866186229dfc.png)

### 2) BalancedRandomForestClassifier and EasyEnsembleClassifier were the 2 algorithms used in this objective. Between them, the EasyEnsembleClassifier performed best (see the credit_risk_ensemble.ipynb file for code). Below are the algorithm outcomes with EasyEnsembleClassifier at the top of each performance category:

### Balanced Accuracy Score:
#### -  EasyEnsembleClassifier
![EasyEnsembleAdaBoostClassifier_BalancedAccuraryScore](https://user-images.githubusercontent.com/101941048/217343945-5134fb26-bf18-4a68-a94e-dc0f29ea3291.png)

#### -  BalancedRandomForest Classifier
![BalancedForestClassifier_BalancedAccuraryScore](https://user-images.githubusercontent.com/101941048/217346368-7c18588a-ea81-487f-99b0-407963f6426f.png)

### Confusion Matrix:
#### -  EasyEnsembleClassifier
![EasyEnsembleAdaBoostClassifier_ConfusionMatrix](https://user-images.githubusercontent.com/101941048/217343964-84716a48-e419-4ff9-9049-3826f1c74399.png)

#### -  BalancedRandomForest Classifier
![BalancedForestClassifier_ConfusionMatrix](https://user-images.githubusercontent.com/101941048/217346383-8e5bcf60-5d1e-4aae-8260-4c2cbe88e1b7.png)

### Classification Report Imbalanced:
#### -  EasyEnsembleClassifier
![EasyEnsembleAdaBoostClassifier_ClassificationReportImbalanced](https://user-images.githubusercontent.com/101941048/217343982-0a8999c3-933c-420e-ae59-6fe057ed5f2c.png)

#### -  BalancedRandomForest Classifier
![BalancedForestClassifier_ClassificationReportImbalanced](https://user-images.githubusercontent.com/101941048/217346393-2f040da0-9eaa-4e7b-b3dd-5ea707f5d2f3.png)

## Summary/Conclusion
Had the EasyEnsembleClassifier algorithm not been run, none of the algorithms would have been given a recommendation due to none of them scoring particularly well on the balanced accuracy, precision, or recall scores - being ~60-80% range. However, the EasyEnsembleClassifier algorithm performed with a balanced accuracy score of 96%, precision score of 99%, and a recall score of 95%. By far this outperforms all other algorithms tested, and does so well that this is a recommended algorithm for use in determining who may or may not be good/bad candidates to give loans.

## Tools/Languages
### Languages/Libraries
- Python
    - from collections import Counter
    - import numpy as np
    - import pandas as pd
    - from pathlib import Path
    - from imblearn.combine import SMOTEENN
    - from imblearn.metrics import classification_report_imbalanced
    - from imblearn.over_sampling import RandomOverSampler
    - from imblearn.under_sampling import RandomUnderSampler
    - from imblearn.over_sampling import SMOTE
    - from sklearn.ensemble import GradientBoostingClassifier
    - from sklearn.linear_model import LogisticRegression
    - from sklearn.metrics import accuracy_score
    - from sklearn.metrics import balanced_accuracy_score
    - from sklearn.metrics import confusion_matrix
    - from sklearn.metrics import classification_report
    - from sklearn.model_selection import train_test_split
    - from sklearn.preprocessing import StandardScaler

### Tools
- GitHub
- Visual Studio

## Resources
[1] https://www.forbes.com/advisor/credit-cards/from-inherent-racial-bias-to-incorrect-data-the-problems-with-current-credit-scoring-models/ 

[2] https://ieeexplore.ieee.org/document/9275986
