# Telcom-Company-Customer-Churn-Classification

# Binary Classification: Telcom company Customer Churn Classification
## Problem Statement :

In the telecom industry, customers are able to choose from a pool of companies to cater their needs regarding communication and internet. Customers are very critical about the kind of services they receive and judge the enitre company based on a single experience! These communication services have become so recurrent and inseparable from the daily routine that a 30 minute maintenance break kicks in anxiety in the users highlighting our taken-for-granted attitude towards these services! Coupled with high customer acquisation costs, churn analysis becomes very pivotal! Churn rate is a metric that describes the number of customers that cancelled or did not renew their subscription with the company. Thus, higher the churn rate, more customers stop buying from your business, directly affecting the revenue! Hence, based on the insights gained from the churn analysis, companies can build strategies, target segments, improve the quality of the services being provided to improve the customer experience, thus cultivating trust with the customers. That is why building predictive models and creating reports of churn analysis becomes key that paves the way for growth!

## Aim :
- To classify the potential churn customers based on numerical and categorical features.
- It is a **binary classification** problem for an imbalanced dataset.

## Dataset Attributes:
    
- **customerID** : Customer ID
- **gender** : Whether the customer is a male or a female
- **SeniorCitizen** : Whether the customer is a senior citizen or not (1, 0)
- **Partner** : Whether the customer has a partner or not (Yes, No)
- **Dependents** : Whether the customer has dependents or not (Yes, No)
- **tenure** : Number of months the customer has stayed with the company
- **PhoneService** : Whether the customer has a phone service or not (Yes, No)
- **MultipleLines** : Whether the customer has multiple lines or not (Yes, No, No phone service)
- **InternetService** : Customer’s internet service provider (DSL, Fiber optic, No)
- **OnlineSecurity** : Whether the customer has online security or not (Yes, No, No internet service)
- **OnlineBackup** : Whether the customer has online backup or not (Yes, No, No internet service)
- **DeviceProtection** : Whether the customer has device protection or not (Yes, No, No internet service)
- **TechSupport** : Whether the customer has tech support or not (Yes, No, No internet service)
- **StreamingTV** : Whether the customer has streaming TV or not (Yes, No, No internet service)
- **StreamingMovies** : Whether the customer has streaming movies or not (Yes, No, No internet service)
- **Contract** : The contract term of the customer (Month-to-month, One year, Two year)
- **PaperlessBilling** : Whether the customer has paperless billing or not (Yes, No)
- **PaymentMethod** : The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
- **MonthlyCharges** : The amount charged to the customer monthly
- **TotalCharges** : The total amount charged to the customer
- **Churn** : Whether the customer churned or not (Yes or No)

## Data Modeling:
Trained different classifier models - XGBoost, Random Forest, Decision Tree Classifier, Logistic Regression, Naive Bayes, SVM and KNN  and optimized hyperparameters (GridsearchCV) to enhance performance.

Implemented a validation pipeline utilizing 5-fold cross-validation. For each classifier, reported F1 score, Cross-validation score, Precision, Recall, Accuracy). Also, for each model, plotted the ROC-AUC curve.

Then, combined classifiers into an ensemble that outperforms each individual classifier. 
![image](https://github.com/kashmira92/Telcom-Company-Customer-Churn-Classification/assets/48323327/9277c4ca-781d-40c7-b9ee-8c6803a1f7ce)


## Evaluation and Reporting:
Selected a model that is expected to perform optimally on the unseen data and provide the predictions accordingly. After evaluating the results on the unseen data (X_test), it's evident that the XGBoost and KNN models have demonstrated excellent performance in the ensemble. Therefore, we have decided to utilize these models for making predictions on the test.csv dataset.

## External validation:

A dataset named ‘test.csv’ is being used for external validation in which the label is hidden. You have to choose the best model(the model which has the highest score) and then use that model to predict the label on the ‘test.csv’.

After prediction, converted the array of 0's and 1's to csv file, named it as ‘submission.csv'.


