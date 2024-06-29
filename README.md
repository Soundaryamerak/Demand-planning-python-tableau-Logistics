# Demand forecasting & visualisation using Python and Tableau
Determining the best ML models to forecast demand for a Brazilian Logistics Company and comparing results.

## Data
The dataset of a brazilian logistics company collected over a period of 60 days. [Data from here](https://archive.ics.uci.edu/dataset/409/daily+demand+forecasting+orders)

## ML models used:
Linear Regression

Random Forest Regression

Gradiant Boosting





## Visualising the GB Model results in Tableau



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


## Evaluation after inital Random forest regression model with feature engineering.

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/c91cd572-740c-42bc-bfab-e643cce7caa2)

## Selecting top features of importance>0.1.

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/0b67957f-d048-472f-b236-82b5e0d0bc0d)

## Evaluation after Random forest regression model with only Top features.

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/e9c75d46-e559-4a78-98a2-0b35e9be2570)

## Evaluation of Random forest regression model after hyperparameter tuning.

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/64e58081-c64d-45b3-aca7-eb741e63b1e1)


## Evaluation of Gradient boosting

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/117ad70d-3fae-4609-ba8e-99b12e87aad5)

## Evaluation of Gradiant boosting after hyperparameter tuning

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/9ba4e8d5-07ad-4772-8ba4-6a925f2cdc08)

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/740f65a5-8fe3-49dc-a42c-a05675afbdb6)



## Comparing results

## Conclusion



