# HR_Employee_Retention


### ** Data **
###### Data is from https://www.kaggle.com/giripujar/hr-analytics. This dataset contains variables that describe employees at a company as well as a variable "left" that indicates whether or not the employee was retained the following work year. I'm using this data purely for the purpose of practicing binary classification.


### Project
##### For this project I am trying to predict employee retention based on employee data such as salary, number of hours worked, evaluation score etc.
##### My goal is to solve this classification problem two ways : with Logistic Regression and with Random Forest. I want to compare the scores of each model and come to a conclusion about which method is the best to use for this particular problem.


### EDA on Employee Turnover
##### I first created a heatmap, looking at the correlation between each numeric variable and the variable "left". 

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/heatmap.PNG)

##### ** Looking at the Correlation Heatmap it looks as if the top 5 factors for employee retention are: **

##### 1) Employee Satisfaction Level

##### 2) Whether or Not the Employee was in a Work Accident

##### 3) Time Employee has Spent with the Company

##### 4) Employees Average Monthly Hours

##### 5) Whether or Not the Employee was Promotted in the Last 5 Years

##### My initail though was that not many employees would identify as having been in a work accident, so perhaps I could throw that variable out for my analysis. After looking into the data, 16.9% of the employees have identified as being in a workplace accident. This is higher than I originally thought, so I will try my logistic regression with and without this variable.

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/salary_bar.PNG)

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/bar_department.PNG)


### Cleaning
##### This data is from Kaggle and therefore did not require mcuh initial cleaning. After I renamed some columns and preformed EDA, I created dummy columns from the categorical salary data to use in my logistic regressiona nd random forest.
![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/dummy_var.PNG)


### Logistic Regression


### Random Forest


### Predictive Probability

![](https://github.com/savyrosea/HR_Employee_Retention/blob/main/pictures/percents.PNG)


