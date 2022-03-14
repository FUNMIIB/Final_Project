# Final_Project
#Presentation
**Topic**
Data Scientist Salary

**Reason Why They Selected Their Topic**
The machine learning model selected was a supervised Logistic Regression model. This model was selected because we are looking to see if we are able to predict having 5 or more skillsets equals a higher salary.

**Description of Their Source of Data**
The compiled data was found on kaggle but the dataset was scraped from the Glassdoor website using Selenium scrapper by Nikhil Bhathi a nuclear scientist at Nova Scotia.

**Questions They Hope to Answer With The Data**
If having 5 or more skillsets equals a higher salary.

***************Segment 2***************
***Description of the data exploration
phase of the project:***

-Dropping redundant columns.
-Removing rolls with "-1" dataset
-Changed "Categorical Data" to "Numerical Data" by the means of "pandas.get_dummies" though we tried "OneHotEncoder" but we untimately picked "pandas.get_dummies" to better exploration.

***Description of the analysis phase of
the project:***

-We separate the Features(X) from the Target(Y)
-Splitting the data into Training and Testing.
-Creating the model by using "LinearRegression" and fitting the model to the data.
-Predecting the test set result, mean squared error, 
-Creating features for Random Forest Regressor 
-Plotting Features Importances against Relative Importance