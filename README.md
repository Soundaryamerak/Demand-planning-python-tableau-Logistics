## Demand forecasting & visualisation using Python and Tableau
Determining the best ML models to forecast demand for a Brazilian Logistics Company and comparing results.

## Data
The dataset of a brazilian logistics company collected over a period of 60 days. [Data from here](https://archive.ics.uci.edu/dataset/409/daily+demand+forecasting+orders)
/
## ML models used:
Linear Regression

Random Forest Regression

Gradiant Boosting

## Steps taken in Python code.
1. Import all necessary libraries (matplotlib, seaborn, pandas, numpy, Scikit-learn (Sklearn - model selection, linear model, preprocessing, metrics), imblearn, collections,Ucimlrepo)
2. Understand the data with summarizing & visualisation
3. Split the data without dropping any variables into train & test sample.
4. Train & evaluate Linear regression model.
5. Feature engineering using Rolling Window statistics.
6. Split data into train & test.
7. Train & evaluate Random Forest Regressor
8. Evaluate RF model.
9. Re-train RF regressor after dropping variables (with only selected variables)
10. Hyperparameter tuning of the newly trained RF model.
11. Evaluate the tuned RF model
12. Train & evaluate Gradiant Boosting with only selected variables.
13. Hyperparameter tuning of GB model.
14. Evaluate the tuned GB model.
15. Export feature importance & forecast results into csv files for furether visualisation.


## Understanding the data

1. A total of 13 variables, with *week of the month and day of the week* to denote the date, 10 different types of orders(*Features*), and total orders as *Target*, and no missing values. Most orders of the quantity between 250 to 350
   ![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/b39d99e5-ae16-42d5-b154-ca214f3fbdd5)
   ![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/2d367f07-791c-4071-ac6e-420ccb8dab56)


2. A strong corelation can be observed between features Non-urgent orders and order type B with Total orders. Order type (c), Banking orders(2), and Urgent orders follow next. Another notable correlation is between the features order type B and non-urgent orders. (The 2 more corelated features with total orders).
   ![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/1f3d85d4-9a8b-4cc7-b4b4-60b4fb91699e)

## Evaluation of Linear regression model
![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/d10624f3-f0ba-4672-8385-a6aec848784a)


## Evaluation after Random forest regression model


![image](https://github.com/Soundaryamerak/Fraud-detection-Python-credit-card-transactions/assets/170541567/23157d51-2525-42ce-b361-8f76a8dc4e02)

## Evaluation of Random forest classifier model

![image](https://github.com/Soundaryamerak/Fraud-detection-Python-credit-card-transactions/assets/170541567/635f8df3-a6f3-40ae-a90f-5b4c0685ef22)

## Evaluation of Random forest classifier model after hyperparamater tuning

![image](https://github.com/Soundaryamerak/Fraud-detection-Python-credit-card-transactions/assets/170541567/9eb090f2-00b8-4cc3-b091-f62aa4c1fab6)

## Comparing results

## Conclusion



