# EDA-repository
# Credit Risk Prediction using Machine Learning

##  Project Overview

This project aims to predict whether a loan applicant is likely to default or (value given to it as 1) or not default (or value given to it as 0) using different machine learning classificatin models. The goal is to help financial institutions minimize their risk by accurately identifying high-risk applicants.


##  Problem Statement

Loan defaults can lead to significant financial losses. The objective of this project is to build a predictive model that can:

* Identify potential defaulters
* Reduce financial risk
* Improve decision-making in loan approvals


##  Dataset

The dataset contains applicant details such as:

* Age
* Income
* Employment length
* Loan amount
* Loan intent
* Credit history
* Historical default record

Target variable:

* loan status , which has a value of 1 , if there is a defualt and 0 if not


##  Data Preprocessing

#Steps performed:

* Removed irrelevant columns such as age more than 100 or employement years more than 60
* Handled missing values:

* Used median because the numerical data was skewed

* Encoded categorical variables:

* One-Hot Encoding ( when there was no heirarchy between the variables in columns )
* Ordinal Encoding (for categories which had heirarchy between them )
* Yhen Scaling of data using Standard Scalar


##  Models Used

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier


##  Evaluation Metrics

Since predicting defaulters is critical, the following metrics were used:

* Recall → How many of the defualters did we catch
* Precision → Avoid false alarming
* ROC-AUC Score → Overall model performance
* Confusion Matrix → Error analysis


##  Model Performance


Performance of LOGISTIC REGRESSION:
Recall score is: 0.4929378531073446
Precision score is: 0.7173689619732785
Auc score is: 0.8662265393790518
Confusion matrix of this model is: [[4824 275] [ 718 698]]

Performance of Decision Tree:
Recall score is: 0.7189265536723164
Precision score is: 0.955868544600939
Auc score is: 0.9195322446076166
Confusion matrix of this model is: [[5052 47] [ 398 1018]]

Performance of RANDOM FOREST:
Recall score is: 0.719632768361582
Precision score is: 0.9714013346043852
Auc score is: 0.92971494909271
Confusion matrix of this model is: [[5069 30] [ 397 1019]]



## Key Insights

* Logistic Regression underperformed due to low recall, missing many defaulters
* Decision Tree showed strong performance but slightly less stability
* Random Forest performed best overall, achieving:

* High recall (detecting most defaulters)
* Very high precision (few false positives)
* Highest ROC-AUC score


##  Final Conclusion

The Random Forest model is the most suitable for this problem as it provides the best balance between:

* Identifying risky applicants (high recall)
* Avoiding incorrect rejections (high precision)

This makes it highly effective for real-world credit risk prediction.


##  Visualizations Included

* ROC Curve comparison of all models
* Confusion Matrix heatmap


##  Tech Stack

* Python
* Pandas, NumPy
* Scikit learn
* Matplotlib, Seaborn



Feel free to star ⭐ the repo and share feedback!
