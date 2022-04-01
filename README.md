# Final_Project

**Data Scientist Salary Analysis

**Analysis Overview**
For this analysis, Python and Pandas in Jupyter notebook were used to create a dataframes and to implement our machine learning to predict data scientist salary based on multiple skillsets. This analysis aimed to answer the question: How much would a data scientist get paid given certain skills set. We chose this topic because it would be interesting as data scientists to know how salaries may vary based on certain skillsets. In addition, Postgres was used to create our table and tableau to create visualizations of our findings.  Below is a link to the google slides that presents our analysis in a concise matter. 

*Link to Google Slides presentation
https://docs.google.com/presentation/d/1x0JC5fCtSMdJ1AgiCAaG_mN5k1WnZFaPY5DBJZMANQM/edit?usp=sharing


**Data Source:
The compiled data was found from kaggle and it was scraped from the Glassdoor website using Selenium scrapper by Nikhil Bhathi, a nuclear scientist at Nova Scotia. After scrapping the raw data, the duplicated rows were removed which reduced the records from 1000 to 742. The dataset has 42 columns including the Job title, Salary Estimate, Job Description, Rating, Company, Location, Company, Headquarters, etc. 

**Description of the Communication Protocol**
GitHub was used to house the repository and to share files and code among the project team members. Each team member has a branch with at least four commits for each segment of the project. 
- We worked together during class period on the project discussing the best approach to improve training and testing scores
- We also met weekly outside of class via zoom to work on weekly deliverables and to discuss the different aspects of the project.
- We constantly communicated on Slack to update ourselves on the progress of the project
- On several occasions during class period, we have sought help and guidance from LAs and the instructor on the different steps during preprocessing of the data. For example, the LA helped us when we needed to convert categorical to numerical values and during selection of the features of column that has highest correlation with the target. We employed Random Forest feature importance to process the data for feature of importance to drop unimportant columns.

**Results

*Machine Learning Model
The machine learning model we employed was a Linear Regression model. This model allows us to create training and test groups from the dataset to predict how much data scientists would get paid given certain skill sets. This analysis also allowed us to answer the following questions: 
- How are we training the model? 
- What is the model's accuracy score? 
- How does the model work?
The first step in the model is data exploration which involves visualizing the data, getting the shape of the data, checking for missing values, and using the describe () function to get the overall statistics of the data as shown below

   ![Final_Project_image1](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image1.png)

    -The second step to do conduct any feature engineering to our data, in our data we used the feature extraction method on our company name column to remove slashes '/' and any spaces that was irrelevant to the data or would cause adding more unnecessary columns.

    - The next step is preprocessing of the data which included dropping unimportant columns and transforming the categorical data to numeric data by get dummies as shown below:
 
  ![Final_Project_image2](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image2.png)

    - In step 3, we separated the Features(X) from the Target(Y) using the code below:

    ![Final_Project_image3](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image3.png)

    - Next, we used the **70/30%** method to split the data for training and testing, then created the model by using Linear Regression and fitted the model as shown below:

    ![Final_Project_image4](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image4.png)

    - We then predicted and scored the test set results using the codes below:

    ![Final_Project_image5](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image5.png)
    
    - The resulting Training Score is 0.5774150405740237 while the Testing Score is -7.299880743582402e+16
    
    - Next, Random Forest Regressor was used to select all the features of columns that have highest correlation with the target and Feature importance was used to remove all unimportant columns as shown below:

    ![Final_Project_image6](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image6.png)

    - Random Forest Feature Importance returned the scores as follows: 
    model score on training data: 0.9431295661248498
    model score on testing data: 0.6492095833697138

    Finally, we plotted a horizontal bar graph of our feature importance columns as shown below:

    ![Final_Project_image7](https://github.com/FUNMIIB/Final_Project/blob/main/Resources/Final_Project_image7.png)

**Dashboard**
The dashboard consists of 6 tiles. The first two tiles in the upper left corner provide the 'Avg. Salary' ranges that were used in our data set. Below that we have a title that list all the industries that are part of our data set. At the bottom left we have a packed bubble tile for the industries that is weighted based on the Avg. Salary information for each industry. The top tile on the right is a symbol map of the US. This map provides details on the Avg. Salary be location. This map is also weighted be Salary to make the bubble bigger and darker in shade for the higher salaries. The bottom right tile provides the Avg. Salary by sector and color codes the higher salaries darker.
The dashboard also includes radio button filters that allow you to select the skills that you would like information displayed for. Changes to these selections will adjust all the graphs on the dashboard.
https://public.tableau.com/app/profile/bjorn.dennisseur/viz/DataScientist_16477823775010/Dashboard1?publish=yes

**Database**
Jupyter notebook was used to create the dataframe. The csv was read into python using pandas. The database was created using PostgreSQL and pgAdmin to present a provisional database that mimics the final database structure.

**Summary 
In sum, our Linear Regression machine learning model provided insight that given a certain skillset it will impact the salary a data analyst will get however, it did not perform well to show significant influence on the salary. The limitation in our model is that it is overfitting which might introduce some bias. In order to improve the accuracy of our model we used a Random Forest Regressor which performed better showing that certain skillsets as well as other factors like job location, company, sector, and other elements play a significant role in determining a data analyst salary.  In the future we would use all the columns to predict salary and pinpoint features that determines the highest salary. 

