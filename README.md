# Final_Project
**Presentation Topic**
 Data Scientist Salary Analysis

**Questions They Hope to Answer With The Data**
How much would a data scientist get paid given certain skills set. 

**Reason Why They Selected Their Topic** We chose the topic because it would be interesting as data scientists to know how salaries may vary based on certain skills set

**Description of Their Source of Data** The compiled data was found on kaggle. The dataset was scraped from the Glassdoor website using Selenium scrapper by Nikhil Bhathi, a nuclear scientist at Nova Scotia. After scrapping the raw data, the duplicated rows was removed which reduced the records from 1000 to 742. The dataset has 42 columns including the Job title, Salary Estimate, Job Description, Rating, Company, Location, Company , Headquarters, etc 

**Description of the communication protocol**

For this analysis, Python and pandas in jupyter notebook was used to create a database and we implemented machine learning to predict data scientist salary based on multiple skillsets. GitHub was used to house the repository and to share files and code among the project team members. Each team member has a branch with at least four commits for each segment of the project. 
- We work together during class period on the project discussing the best approach to improve training and testing scores
- We also meet weekly outside of class via zoom to work on weekly deliverables and to discuss the different aspects of the project.
- We constantly communicate on Slack to update ourselves on the progress of the project
- On several occasions during class period, we have sought help and guidance from LAs and the instructor on the different steps during prepocessing of the data. For example, the LA helped us when we needed to convert categorical to numerical values and also during selection of the features of column that has highest correlation with the target. We employed Random forest feature importance to process the data for feature of importance in order to drop unimportant columns.

**Jupyter Notebook Link**

**Limitation**
The limitation of our model is that it is overfitting which might introduce some bias

**Benefits**

**Description of feature engineering**
Method of feature extraction was used to remove 'slash' and any spaces.

**Link to Google Slides presentation**

https://docs.google.com/presentation/d/1x0JC5fCtSMdJ1AgiCAaG_mN5k1WnZFaPY5DBJZMANQM/edit?usp=sharing

**Dashboard**
The dashboard consists of 6 tiles. The first two tiles in the upper left corner provide the Avg Salary ranges that were used in our data set. Below that we have a title that list all the industries that are part of our data set. At the bottom left we have a packed bubble tile for the industries that is weighted based on the Avg Salary information for each industry. The top tile on the right is a symbol map of the US. This map provides details on the Avg Salary be location. This map is also weighted be Salary to make the bubble bigger and darker in shade for the higher salaries. The bottom right tile provides the Avg Salary by sector and color codes the higher salaries darker.
The dashboard also includes radio button filters that allow you to select the skills that you would like information displayed for. Changes to these selections will adjust all the graphs on the dashboard.
https://public.tableau.com/app/profile/bjorn.dennisseur/viz/DataScientist_16477823775010/Dashboard1?publish=yes

**Machine Learning Model**
- The machine learning model we employed is Linear Regression model. This model allows us to create training and test groups from the dataset to  predict how much data scientists would get paid given certain skill sets. This analysis also alllows us to answer the following questions: 
- How are we training the model? 
- What is the model's accuracy score? 
- How does the model work?
- Several steps were taken to improve training and testing scores after reading the data into Jupyter notebook using pandas
    - The first step in the model is **data exploration** which involves visualizing the data, getting the shape of the data, checking for missing values, and using the .describe to get the overall statistics of the data as shown below

   ![Final_Project_image1](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image1.png)

    - The next step is **preprocessing** of the data which includes dropping unimportant columns and transforming the categorical data to numeric data by get dummies as shown below:
 
  ![Final_Project_image2](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image2.png)

    - In step 3, we separated the Features(X) from the Target(Y) using the code below:

    ![Final_Project_image3](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image3.png)

    - Next, we used the **70/30%** method to split the data for training and testing and created the model by using LinearRegression as shown below:

    ![Final_Project_image4](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image4.png)

    - We then predected and scored the test set results using the codes below:

    ![Final_Project_image5](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image5.png)
    
    - The resulting Training Score is 0.5774150405740237 while the Testing Score is -7.299880743582402e+16
    
    - Next, **RandomForestRegressor** was used to select all the features of columns that have highest correlation with the target and Feature_importances was used to remove all unimportant columns as shown below

    ![Final_Project_image6](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image6.png)

    - Random Forest Feature Importance returned the scores as follows: 
    model score on training data: 0.9431295661248498
    model score on testing data: 0.6492095833697138

    Finally, we ploted a horizontal bar graph as shown below:

    ![Final_Project_image7](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image7.png)

**Database**
Jupyter notebook was used to create the dataframe. The csv was read into python using pandas. The database will be created using PostgreSQL and pgAdmin to present a provisional database that mimics the final database structure.