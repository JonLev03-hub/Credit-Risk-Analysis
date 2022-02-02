# Credit-Risk-Analysis
A credit company wants to have a basic algorithm to speed up the process of credit approval, To achieve this I will be using machine learning to predict the risk associated with a particular credit account

Throughout this work I tested multiple machine learning algorithms, and resampling strategies trying to find a method that could reliably determine the risk level of a credit account. 

## Results 
Below I have assorted the resulting data, Low Risk is represented as 1 and high risk is represented as 0

#### Native Random Oversampling With Linear Regression
Balanced Accuracy Score : 0.6560

                      pre       rec       spe        f1       geo       iba       sup
              0       0.01      0.69      0.62      0.02      0.65      0.43       101
              1       1.00      0.62      0.69      0.76      0.65      0.43     17104
    avg / total       0.99      0.62      0.69      0.76      0.65      0.43     17205
#### SMOTE Oversampling with linear regression
Balanced Accuracy Score : 0.6623
 
                      pre       rec       spe        f1       geo       iba       sup
              0       0.01      0.63      0.69      0.02      0.66      0.44       101
              1       1.00      0.69      0.63      0.82      0.66      0.44     17104
    avg / total       0.99      0.69      0.63      0.81      0.66      0.44     17205
#### Undersampling with Linear Regression
Balanced Accuracy Rating : 0.5447

                      pre       rec       spe        f1       geo       iba       sup
              0       0.01      0.69      0.40      0.01      0.52      0.28       101
              1       1.00      0.40      0.69      0.57      0.52      0.27     17104
    avg / total       0.99      0.40      0.69      0.56      0.52      0.27     17205
#### Combination Sampling with Linear Regression
Balanced Accuracy Rating : 0.6447

                      pre       rec       spe        f1       geo       iba       sup
              0       0.01      0.72      0.57      0.02      0.64      0.42       101
              1       1.00      0.57      0.72      0.72      0.64      0.40     17104
    avg / total       0.99      0.57      0.72      0.72      0.64      0.40     17205
#### Balanced Random Forest Classifier
Balanced Accuracy Rating : 0.7835

                      pre       rec       spe        f1       geo       iba       sup
              0       0.03      0.68      0.88      0.06      0.78      0.59       101
              1       1.00      0.88      0.68      0.94      0.78      0.62     17104
    avg / total       0.99      0.88      0.68      0.93      0.78      0.62     17205
#### Easy Ensemble AdaBoost Classifier
Balanced Accuracy Score : 0.9324

                      pre       rec       spe        f1       geo       iba       sup
              0       0.09      0.92      0.94      0.16      0.93      0.87       101
              1       1.00      0.94      0.92      0.97      0.93      0.87     17104
    avg / total       0.99      0.94      0.92      0.97      0.93      0.87     17205
    
## Summary

In summary the obvious choice for an effective algorithm is the Easy Ensemble AdaBoost Classifier. 

When looking at the results there really isn't a super good stand alone use for these algoritms because even the best of these could only detect 9% of the High risk credit accounts, but when paired with a human to check the results it could be a useful tool to help guide the decision to reduce the failure rate of that individual as it doesn't take much time to have the algorithm predict the scores. 

