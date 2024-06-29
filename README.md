# Demand Forecasting: Daily Demand Orders and Visualization using Python and Tableau

Determining the best ML models to forecast demand for a Brazilian logistics company and comparing results.

## Data
Dataset from a Brazilian logistics company collected over 60 days. [Data from here](https://archive.ics.uci.edu/dataset/409/daily+demand+forecasting+orders)

## ML Models Used:
- Linear Regression
- Random Forest Regression
- Gradient Boosting

**[Python File](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/blob/main/Demand%20Forecasting.ipynb)**

## Understanding the Data

1. The dataset includes 13 variables: *week of the month* and *day of the week* to denote the date, 10 different types of orders (*features*), and *total orders* as the target, with no missing values. Most orders are between 250 to 350 in quantity.

   ![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/b39d99e5-ae16-42d5-b154-ca214f3fbdd5)
   
   ![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/2d367f07-791c-4071-ac6e-420ccb8dab56)

2. A strong correlation is observed between *Non-urgent orders* and *Order type B* with *Total orders*. Other significant correlations include *Order type (c)*, *Banking orders(2)*, and *Urgent orders*. Notably, *Order type B* and *Non-urgent orders* are highly correlated with *Total orders*.

   ![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/1f3d85d4-9a8b-4cc7-b4b4-60b4fb91699e)

## Comparing the Performance of Various Models 

**[Collated Excel Sheet of Exported CSV Files](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/blob/main/Exported%20-Collated.xlsx)**

**[Tableau Visualization](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/blob/main/Demand%20Forecasting.twb)**

## Performance Parameters

1. Gradient Boosting shows the best performance with the lowest MAE, RMSE, MSE, and the highest R² value, consistently showing the smallest errors and best fit.
2. Gradient Boosting after hyperparameter tuning performs similarly well.
3. Random Forest models perform reasonably well but are slightly inferior to Gradient Boosting models.

**The Gradient Boosting model, especially without hyperparameter tuning, is the most effective for this demand forecasting task.**

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/b4c6de96-7a50-4c5e-a1b0-199e1ed0844a)

## Feature Importances

**Non-urgent orders** and **Order Type B** are the most significant features impacting the model's predictions.

_Note: The importance of these features changes significantly before and after hyperparameter tuning of Gradient Boosting._

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/5715759c-cb88-424b-ab2e-72334b7170f8)

## Forecast Results

**The Gradient Boosting model (orange line) most closely follows the actual demand trend.**

![image](https://github.com/Soundaryamerak/Demand-planning-python-tableau-Logistics/assets/170541567/b1906170-3be0-442b-b166-d6f0ce0ea19e)

## Steps Taken in Python Code

1. Import necessary libraries (matplotlib, seaborn, pandas, numpy, Scikit-learn, imblearn, collections, Ucimlrepo).
2. Understand the data with summarizing and visualization.
3. Split the data without dropping any variables into train and test samples.
4. Train and evaluate Linear Regression model.
5. Perform feature engineering using rolling window statistics.
6. Split data into train and test sets.
7. Train and evaluate Random Forest Regressor.
8. Evaluate Random Forest model.
9. Re-train Random Forest Regressor after selecting variables.
10. Hyperparameter tuning of the newly trained Random Forest model.
11. Evaluate the tuned Random Forest model.
12. Train and evaluate Gradient Boosting with selected variables.
13. Hyperparameter tuning of the Gradient Boosting model.
14. Evaluate the tuned Gradient Boosting model.
15. Export feature importance and forecast results into CSV files for further visualization.
