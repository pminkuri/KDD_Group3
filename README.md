### Project Group 3
### Exploratory Data Analysis of COVID’19 impact on Community Mobility
 
## Team Members:    
 
- Shiva Sai Praneeth Chakinala    -     801147603
- Chaitanya Kintali 	          -	   801097831
- Prashanth Minkuri    	          -     801166901
- Pranitha Amrutha Veldanda       -     801166969
 
GitHub Repo Link :  https://github.com/pminkuri/KDD_Group3

 
## Project Introduction:
 
We will be performing Exploratory Data Analysis on the Community Mobility Reports data provided by Google during the pandemic period and analyse how the mobility of people to various popular public places has changed. We will try to extract various insights such as how the visits and duration of stay at different places changed compared to a baseline and number of COVID positve cases. The baseline is considered as the median value for the corresponding day of the 5- week period duration Jan 3–Feb 6, 2020.

 
## Research Question:
 
The Research Question we are focusing on is how COVID’19 has impacted the mobility of people in various public places listed below with respect to number of daily positive cases across different states in the United States. This analysis can help public health authorities to take effective measures such as implementing social distancing restrictions and improving access to essential services. We also analyse how the mobility has impacted in different Red and Blue states of US.
1. 	Groceries & pharmacy
2. 	Retail & recreation
3. 	Transit stations and
4. 	Parks categories

 
## Data Sources:
 
We are performing our research on the data provided by Google that is collected from users who have opted-in to Location History for their Google Account. For daily COVID cases we are using data provided by CDC.
 
References: 

- https://www.google.com/covid19/mobility/
- https://data.cdc.gov/Case-Surveillance/United-States-COVID-19-Cases-and-Deaths-by-State-o/9mfq-cb36/data
 
## Technologies Used:

- Python (Programming Language)
- Jupyter Notebook(IDE)

Libraries used in python :
- Pandas
- Matplotlib
- Numpy
- Scikit-learn 
- Seaborn
- Sklearn
- statsmodels

## CRISP-DM Process

We have undergone these steps as a part of CRISP-DM:

Research Phase
Data Understanding Phase
Data Preparation Phase
Data Exploration
Modeling Phase
Evaluation Phase

### 1. Research Phase

COVID-19 has rapidly spread in the world and social distancing or stay-at-home measures have been adopted by many countries. Mobility of people have been restricted to many public places. It will be valuable to learn from this research how the mobility to certain public places have changed with respect to the growing number of positive cases. We are conducting this analysis on 50 states of United States. In this project we aim to gather and analyse the data  related to the mobility to varuous place and understand how we can better social distancing measures at these public places.

### 2. Data Understanding Phase
In this phase we are understanding what data can be used inorder to make our research more effective. We have chosen our data from Google which they collected from the users who opted-in to Location History for their Google Account. We also collected data related to state wise  number of covid data in order to understand the daily trend of positive cases in different states. We will combine both the datasets to make our analysis.

### 3. Data Preparation Phase


- Due to compute restrictions we had to cut the size of dataset from ~ 20 million to ~ 10 million. We did this by dropping the random selection of 10 million rows so as to avoid the bias.
- We scaled the data to normalize the relations between dependent and independent variables.
- We encoded categorical variables using one-hot encoding and label-encoding.
- Due to the large amount of missing values in the "year_built", "floor_count", "builiding_age" columns in the building metadata table, we dropped the columns.
- Dropped columns like "building_id", "site_id" which are not necessary.
- Instead of having the whole time stamp we just selected the hour value and stored.




## Approach:
 
Understanding the dataset and performing Exploratory Data Analysis. Preparing data by handling missing values.
 
 
## References:  
 
1. https://www.google.com/covid19/mobility/
 
2.  https://www.gstatic.com/covid19/mobility/2020-11-13_US_Mobility_Report_en.pdf 	 

 
 
 
 

