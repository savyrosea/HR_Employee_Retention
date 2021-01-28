# HR_Employee_Retention



## Data
###### Data is from https://www.kaggle.com/giripujar/hr-analytics. This dataset contains variables that describe employees at a company as well as a variable "left" that indicates whether or not the employee was retained the following work year. I'm using this data purely for the purpose of practicing binary classification.



## Project
##### For this project I am trying to predict employee retention based on employee data such as salary, number of hours worked, evaluation score etc.
##### My goal is to solve this classification problem two ways : with Logistic Regression and with Random Forest. I want to compare the scores of each model and come to a conclusion about which method is the best to use for this particular problem.



## EDA on Employee Turnover
##### I first created a heatmap, looking at the correlation between each numeric variable and the variable "left". 

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/heatmap.PNG)

##### Looking at the Correlation Heatmap it looks as if the top 5 factors for employee retention are: 

##### 1) Employee Satisfaction Level

##### 2) Whether or Not the Employee was in a Work Accident

##### 3) Time Employee has Spent with the Company

##### 4) Employees Average Monthly Hours

##### 5) Whether or Not the Employee was Promotted in the Last 5 Years

##### My initail though was that not many employees would identify as having been in a work accident, so perhaps I could throw that variable out for my analysis. After looking into the data, 16.9% of the employees have identified as being in a workplace accident. This is higher than I originally thought, so I will try my logistic regression with and without this variable.

##### Next, I used bar charts to analyze the categorical variables in the data.

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/salary_bar.PNG)

##### Percent with low salary that left: 42.2%

##### Percent with medium salary that left: 25.7%

##### Percent with high salary that left: 7.1%

##### These percents vary greatly. Therefore, I am concluding salary has a high impact on whether or not an employee will leave the following year.

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/bar_department.PNG)

##### Percent in Sales that left: 32.4%

##### Percent in HR that left: 41%

##### Percent in Technical that left: 34.5%

##### Percent in Support that left: 33.2%

##### These percents are much closer to each other, so I am not going to use department in my analysis.



## Cleaning
##### This data is from Kaggle and therefore did not require much initial cleaning. After I renamed some columns and preformed EDA, I created dummy columns from the categorical salary data to use in my logistic regressiona nd random forest.
![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/dummy_var.PNG)



## Binary Classification

### Logistic Regression

##### I ran sklearn logistic regression models both with and without standardizing independent features. I used a random_state to make my results repeatable and got a slightly better result when I did not standardize the data with an accuracy score of 76.2%.

### Random Forest

##### My random forest model worked even better with a accuracy score of 97.6%.


## Predictive Probability

##### Since I had more success with my random foret model, I used that model to get the predictive probablity that each employee would stay the following year.

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/percents.PNG)


