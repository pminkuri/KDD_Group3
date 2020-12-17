## Project Group 3
## Exploratory Data Analysis of COVID’19 impact on Community Mobility
 
### Team Members: 

- Shiva Sai Praneeth Chakinala-  801147603
- Chaitanya Kintali 	          -	 801097831
- Prashanth Minkuri    	       -  801166901
- Pranitha Amrutha Veldanda    -  801166969
 
 
## Project Introduction:
 
We will be performing Exploratory Data Analysis on the Community Mobility Reports data provided by Google during the pandemic period and analyze how the mobility of people to various popular public places has changed. We will try to extract various insights such as how the visits and duration of stay at different places changed compared to a baseline and the number of COVID positive cases. The baseline is considered as the median value for the corresponding day of the 5- week period duration Jan 3–Feb 6, 2020.

 
## Research Question:
 
The Research Question we are focusing on is how COVID’19 has affected the mobility of people in various public places listed below with respect to a number of daily positive cases across different states in the United States. This analysis can help public health authorities to take effective measures such as implementing social distancing restrictions and improving access to essential services. We also analyze how mobility has affected in different Red and Blue states of the US.

1. 	Groceries & pharmacy
2. 	Retail & recreation
3. 	Transit stations and
4. 	Parks 
5.  Residential
6.  Workplace categories

 
## Data Sources:
 
We are performing our research on the data provided by Google that is collected from users who have opted-in to Location History for their Google Account. For daily COVID cases, we are using data provided by the CDC.
 
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
- Plotly Express

## CRISP-DM Process

We have undergone these steps as a part of CRISP-DM:

Research Phase
Data Understanding Phase
Data Preparation Phase
Data Exploration
Modeling Phase
Evaluation Phase

### 1. Research Phase

COVID-19 has rapidly spread in the world and social distancing or stay-at-home measures have been adopted by many countries. Mobility of people has been restricted to many public places. It will be valuable to learn from this research how the mobility to certain public places has changed with respect to the growing number of positive cases. We are conducting this analysis on 50 states of the United States. In this project, we aim to gather and analyze the data related to mobility to various places and understand how we can better social-distancing measures at these public places.

### 2. Data Understanding Phase

In this phase, we are understanding what data can be used in order to make our research more effective. We have chosen our data from Google which they collected from the users who opted-in to Location History for their Google Account. We also collected data related to state wise number of covid data to understand the daily trend of positive cases in different states. We will combine both the datasets to perform analysis on different mobility trends with respect to COVID positive cases.

### 3. Data Preparation Phase

- Our datasets contain the values corresponding to each county within the state. We are primarily focusing on analyzing the state-wise trends. Hence, we are dropping all the rows corresponding to each county
- We are creating a new column 'cases_percent' and store the values by computing the percentage of COVID positive cases using the columns 'New_cases' and 'Total_tests'
- We have a few null values in the columns 'parks' and 'transit_stations'. We will replace those values with zeros so that we can calculate accurate trends of the mobility to those categories of places
- Dataset "cases" contains a large number of null values; we will drop those columns and replace other null values with zeros.
- We convert the data type of the date column to the DateTime data type so that we can use that column to filter the data based on the DateTime values of the dataset.

### 4. Data Exploration phase

- Summarizing the mobility trends of different public place categories across all the US States
- Identifying the states with the highest and lowest number of positive cases.
- We are finding the correlation between different features of the dataset using the heatmaps
- Identifying the outliers in each of the different categories of places

### 5. Modeling Phase

As our project primarily focused on exploratory data analysis, we are not dealing with any specific machine learning algorithms for modeling, instead we will perform descriptive analysis on the effects of mobility during the COVID’19 period. Based on the daily data provided by google analytics between the dates 2/15/2020 to 11/20/2020, we have constructed a new data frame in which we included mobility details of each state in the US. We have identified Red states (Republican won states) and Blue states (Democrats won state) as part of constructing association rules and included them in our mobility data frame. We have performed an extensive analysis on the COVID’19 has impacted the mobility of people to different public places such as 

1. 	Groceries & pharmacy
2. 	Retail & recreation
3. 	Transit stations and
4. 	Parks 
5.  Residential
6.  Workplace categories


We also constructed our association rules by implementing the apriori algorithm on our selected dataset. Some of the associations we found are 

-	Poverty is high in the Red counties with support of 70% and confidence of 80%.
-	Number of cases is high in the counties which have more property with the support of 8% and confidence of 85%.


### 6. Evaluation Phase

We used exploratory data analysis to analyze the mobility trends of different places across all the US states, we observed that mobility has dropped to a greater extent in retail and recreation, transit_stations, and workplaces. We used heatmap to show the correlation between the columns of the mobility dataset. Histogram plots show us the number of cases in different states and also states with the highest positive cases wrt to the state’s population.

We are visualizing the trends of mobility during COVID19 to different public places using the graphs plotted using the plotly library. Hovering on each individual state gives the statistics such as the total number of positive cases, change in mobility to 6 mentioned public places. States with darker colors indicate the mobility is high and as the color intensity decrease, it indicates the states with low mobility than that of baseline.
As part of the representation of these graphs, we need to install the following two libraries namely plotly and chart_studio

![mobility](https://github.com/pminkuri/KDD_Group3/blob/main/img/mobility_redblue.png)

## Summary
After we have performed our analysis on the mobility dataset we have got to following conclusions. The mobility of cases has dropped mostly in Blue states and the mobility increased in Red states.

![lowdrop](https://github.com/pminkuri/KDD_Group3/blob/main/img/lowdrop.png)

![highdrop](https://github.com/pminkuri/KDD_Group3/blob/main/img/highdrop.png)

We also plotted graphs for individual graphs for each of the 6 mentioned public places and those graphs can be found in the notebook. 




## Results and Observations


After we have performed our analysis on the mobility dataset we have got to following conclusions. 
- The mobility of cases has dropped mostly in Blue states and the mobility increased in Red states. 
- There is a huge amount of mobility drop in the states like Washington DC, Hawaii, and Florida.
- We can understand that as these states are mostly visited by tourists, due to the pandemic there is a huge drop in mobility in such places.
- On another hand, there is no much decrease in the mobility of people in the states like Idaho, Wisconsin, Wyoming, and South Dakota.
- We can observe that these states are mostly the mid-central states which are not affected by the COVID'19 much.


## summary

#### What was unique about the data?  Did you have to deal with imbalance? What data cleaning did you do? 

We have combined the covid-19 community mobility dataset and the covid-19 cases dataset from February to November to get the required results and there was a lot of imbalance between the two datasets and  We have 2 different data types and they are numeric and categorical. We have a column "Date" which is of data type object and we converted it to date type. Also removed unwanted extra columns this includes duplicate or irrelevant observations which are not useful for our analysis for example in feature selection we have data corresponding to each county within the state and as we concentrated more on state-wise data we dropped the county wise data. We had many missing values in the datasets which we cannot ignore missing values in our dataset, So we have dropped some observations and have replaced some with the 0. We have also observed that there are outliers in all places.

#### Did you create any new additional features / variables?

We have added new columns 'new_cases', cases_percent' of df_cases1 to df_mobility dataset.

#### What was the process you used for evaluation?  What was the best result?

We used exploratory data analysis to analyze the mobility trends of different places across all the US states, we observed that mobility has dropped to a greater extent in retail and recreation, transit_stations, and workplaces. We used a heatmap to show the correlation between the columns of the mobility dataset. Histogram plots show us the number of cases in different states and also states with the highest positive cases wrt to the population of the state.We used plotly and chart_studio library to analyze the mobility trends in different places with hovering on the states. States with darker colors indicate the mobility is high and as the color intensity decrease, it indicates the states with low mobility than that of baseline



### Future work

In our current project, we have performed our analysis just to the state level in the US, as part of future work we can extend this model to the county level. The county-level analysis gives more accurate results with more possible insights. As we are dealing with time series data including the counties would have become more extensive data and we may have required more time.

### Instructions

- This project needs python 3.7.
- This solution requires Jupyter Notebooks or Google Colab to run.
- Packages to be installed: Numpy, Pandas, Sklearn, Matplotlib, Seaborn,Plotly, chart_studio.
 
Open Terminal or Command Prompt, Enter the following line to open the jupyter notebook.
Once the Jupyter Notebook opens, you can run the Notebook and make appropriate changes.
Make sure to put both Dataset and Notebook in the same folder.

Now you can have access to the model we have built you can make an analysis using our dataset.

You can find all the visualisations we have performed in seperate pdf file 
https://github.com/pminkuri/KDD_Group3/blob/main/Visualizations.pdf






 
## References:  
 
1. https://www.google.com/covid19/mobility/
 
2. https://www.gstatic.com/covid19/mobility/2020-11-13_US_Mobility_Report_en.pdf

3. https://docs.oracle.com/cd/E11882_01/datamine.112/e16808/algo_apriori.htm#DMCON287

4. https://plotly.com/python/choropleth-maps/

5. https://matplotlib.org/gallery/index.html#event-handling
 
 
 
