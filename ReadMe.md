# Credit Risk Analysis
## Overview
The goal of the project was to gain introductory experience to supervised machine learning. In this project, credit-card risk is assessed using six different supervised 
machine learning models. The first four models all are Logistical Regression models, but they each use different resampling techniques; the data was oversampled with 
random oversampling and SMOTE, undersampled with cluster centroids, and resampled with a combination of oversampling and undersampling with SMOTEENN. The final two models 
were BalancedRandomForestClassifier and EasyEnsembleClassifier which are both ensemble learning models. The end goal of using six models was to determine if there is 
justification for using any of the models over the others.
## Results
The Imbalanced Classification Reports are obtained with classification_report_imbalanced(y_test, predictions) which is where the precision and recall values are obtained.
balanced_accuracy_score(y_test, predictions) was used to determine the Balanced Accuracy Scores.
### Random Oversampling:
* [Imbalanced Classification Report](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/Images/RandomSamplingbcr.png)
* Precision: High Risk: 0.01, Low Risk: 1.00
* Recall:  High Risk: 0.72, Low Risk: 0.6
* Balanced Accuracy Score: 0.66
### SMOTE:
* [Imbalanced Classification Report](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/Images/SMOTEbcr.png)
* Precision: High Risk: 0.01, Low Risk: 1.00
* Recall: High Risk: 0.61, Low Risk: 0.7
* Balanced Accuracy Score: 0.65
### ClusterCentroids:
* [Imbalanced Classification Report](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/Images/ClusterCentroidsbcr.png)
* Precision: High Risk: 0.01, Low Risk: 1.00
* Recall: High Risk: 0.69, Low Risk: 0.4
* Balanced Accuracy Score: 0.54
### SMOTEENN:
* [Imbalanced Classification Report](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/Images/SMOTEENNbcr.png)
* Precision: High Risk: 0.01, Low Risk: 1.00
* Recall: High Risk: 0.69, Low Risk: 0.59
* Balanced Accuracy Score: 0.64
### BalancedRandomForestClassifier:
* [Imbalanced Classification Report](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForestClassifierbcr.png)
* Precision: High Risk: 0.03, Low Risk: 1.00
* Recall: High Risk: 0.70, Low Risk: 0.87
* Balanced Accuracy Score: 0.79
### EasyEnsembleClassifier:
* [Imbalanced Classification Report](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleClassifierbcr.png)
* Precision: High Risk: 0.09, Low Risk: 1.00
* Recall: High Risk: 0.92, Low Risk: 0.94
* Balanced Accuracy Score: 0.93
## Summary
There was very little difference in the precision between the various models. In all cases, the precision for low risk cases was 1.0 meaning that the models correctly predicted
low risk cards 100% of the time. However, the precision for high risk was extremely bad. The best precision being a 0.09 or correct 9% of the time using the 
EasyEnsembleClassifier. This being said, recall may be the more important metric in this scenario as it is more important to avoid false negatives (where a high risk is 
deemed low risk) then to avoid the false positives (where low risk is deemed high risk) associated with poor precision. Recall scores were much higher in general across all
models and low and high risk recall scores were comparable within models. However, the EasyEnsembleClassifier model stands out amongst the rest. With a high risk recall score
of 0.92 and a low risk recall score of 0.94, it outperformed the other models by about 20% across the board. This in addition to its higher balanced accuracy score of 0.93
makes this model seem like the best to recommend for the particular dataset used in this project. 
## Resources
* [Resampling Models Code](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb)
* [Ensemble Models Code](https://github.com/MDaily7/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb)
* [Images](https://github.com/MDaily7/Credit_Risk_Analysis/tree/main/Images)
* Python 3.7.11
* Anaconda 4.11.0
 
