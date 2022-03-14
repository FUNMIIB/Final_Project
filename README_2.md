# Final_Project
**Presentation**

- Presentation Topic: Data Scientist Salary

**Second segment addition**
Our question was modified as follows: How much would a data scientist get paid given certain skills set. Also, the machine learning model to be used is Linear Regression model

**First segment response**
- Reason Why They Selected Their Topic: The machine learning model selected was a supervised Logistic Regression model. This model was selected because we are looking to see if we are able to predict having 5 or more skillsets equals a higher salary.

- Description of Their Source of Data: The compiled data was found on kaggle but the dataset was scraped from the Glassdoor website using Selenium scrapper by Nikhil Bhathi a nuclear scientist at Nova Scotia. After scrapping the raw data, the duplicated rows was removed which reduced the records from 1000 to 742. The dataset has 42 columns including the Job title, Salary Estimate, Job Description, Rating, Company, Location, Company , Headquarters, etc 

- Questions They Hope to Answer With The Data: If having 5 or more skillsets equals a higher salary.


**Description of the communication protocol**

**Second segment addition**
- We work together during class period on the project discussing the best approach to improve training and testing scores
- On a number of occasions during class period, we have sought help and guidance from LAs and the instructor on the different steps during prepocessing of the data. For example, the LA helped us when we needed to convert categorical to numerical values and also during selection of the features of column that has highest correlation with the target. We employed Random forest feature importance to process the data for feature of importance in order to drop unimportant columns.
- We also meet weekly outside of class via zoom to work on weekly deliverables and to discuss the different aspects of the project.
- We constantly communicate on Slack to update ourselves on the progress of the project

**First segment response**
For this analysis, API calls, AWS, and web scrapping were not used. We will use python and pandas in jupyter notebook to create a database and implement machine learning to predict data scientist salary based on multiple skillsets. GitHub will be used to house the repository and share files and code among the project team members. Each member will have a branch with each team member having at least four commits for the first segment of the project. 

The First_Branch is the square role responsible for setting up the repository, naming the repository, adding team members and ensures everyone has his or her own branch to work from.

The JHoward branch is the tringle role and is responsible for creating a simple machine learning model. 

The X role is mandatory for our team because we are a team of four. rasaq147-patch-1 is in the X role and focuses on the technology side of the project. 

Bjorn_Final is in the circle role  and is in charge of the mockup database using a SQL-based database and including an ERD of the database.


**Machine Learning Model**

**Second segment addition**
Following the instructor's feedback from our first segment deliverables, we have modified our approach and question:
- The machine learning model we will be employing is Linear Regression model. This model would allow us to predict how much data scientists would get paid given certain skill sets.
- Several steps were taken to improve training and testing scores
    - After reading the data into Jupyter notebook using pandas,
    - The first step in the model is **data exploration** which involves visualizing the data, getting the shape of the data, checking for missing values, and using the .describe to get the overall statistics of the data as shown below

   ![Final_Project_image1](https://github.com/FUNMIIB/Final_Project/blob/main/Final_Project_image1.png)

    - The next step is preprocessing of the data which includes dropping unimportant columns and transforming the categorical data to numeric data by get dummies as shown below:
 
  ![Final_Project_image2](https://github.com/FUNMIIB/Final_Project/blob/main/Final_Project_image2.png)

    - In step 3, we separated the Features(X) from the Target(Y) using the code below:

    ![Final_Project_image3](https://github.com/FUNMIIB/Final_Project/blob/main/Final_Project_image3.png)

    - Next, we split the data into training and testing and created the model by using LinearRegression as shown below:

    ![Final_Project_image4](https://github.com/FUNMIIB/Final_Project/blob/main/Final_Project_image4.png)

    - We then predected and scored the test set results using the codes below:

    ![Final_Project_image5](https://github.com/FUNMIIB/Final_Project/blob/main/Final_Project_image5.png)

    - Next, RandomForestRegressor was used to select all the features of columns that have highest correlation with the target and Feature_importances was used to remove all unimportant columns as shown below

    ![Final_Project_image6](https://github.com/FUNMIIB/Final_Project/blob/main/Final_Project_image6.png)

    Finally, we ploted a horizontal bar graph as shown below:

    ![Final_Project_image7](https://github.com/FUNMIIB/Final_Project/blob/main/Final_Project_image7.png)

**First segment response**
We will implement the supervised Logistic Regression machine learning model with the data scientist salary dataset. This model will allow us to create training and test groups from the dataset to predict if having 5 or more skillsets equals higher salary. This analysis will also answer the following questions: 
- How are we training the model? 
- What is the model's accuracy score? 
- How does the model work?

**Database**
Jupyter notebook was used to create the dataframe. The csv was read into python using pandas. The database will be created using PostgreSQL and pgAdmin to present a provisional database that mimics the final database structure.













