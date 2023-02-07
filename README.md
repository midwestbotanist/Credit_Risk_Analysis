# Credit_Risk_Analysis

## Background/Overview
This peer-to-peer credit lending company is seeking to using machine learning as a way to better identify good candidates for giving loans in order to prevent loaning to candidates more likely to default. Machine learning is a tool that can make the loan application process much quicker for applicants. This in part because intant approval can be given for good candidates, poor candidates can be instantly denied, and only those that are in question need to be sent on for further review by a person. On the surface, this is a wonderful tool because it is able to remove biases that humans may have duringt the decision-making process. However, institutional racism along with general classism is a real issue within the economy and the abilities for individuals to be able to get and build credit, and due to these factors, machine learning often is unable to overcome the structure of society to identify candidates who happen to come from disadvantaged backgrounds[1]. This analysis does not address this aspect of machine learning as this is a foundational analysis. However, this should be considered a priority for addressing in future work. 

For this analysis, 6 different algorithms were created to predict credit using resampling models and ensemble classifiers. Below are the algorithms used:

### Algorithms:
- RandomOverSampler
- SMOTE
- LogisticRegression
- SMOTEENN
- BalancedRandomForestClassifier
- EasyEnsembleClassifier

## Results


## Summary/Conclusion

## Tools/Languages
### Languages
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

There is a title, and there are multiple sections (2 pt)
Each section has a heading and subheading (2 pt)
Links to images are working, and code is formatted and displayed correctly (2 pt).
Analysis
The written analysis has the following:

Overview of the loan prediction risk analysis:

The purpose of this analysis is well defined (4 pt)
Results:

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
