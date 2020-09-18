# Data Scientists Jobs - Glassdoor (US)
This project serves as a foundation and platform for a future project exploring salary estimates for data science related jobs in the UK. The following project will contain new data collected by myself using Selenium from Glassdoor.com.


## Resources Used
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, selenium, flask, json, pickle  
**Data:** https://www.kaggle.com/andrewmvd/data-analyst-jobs  
**Flask:** https://towardsdatascience.com/productionize-a-machine-learning-model-with-flask-and-heroku-8201260503d2  

## Data Cleaning
After loading the data from Kaggle I needed to go through some cleaning processes to make it useable for the future modelling. Below are a list of changes made and variables created:
* Removed unecessary text from the job title
* Parsed numeric data from the salary figures
* Extracted occurances of Python in the job description and created a Python(Y/N) variable
* Removed unecessary text from the company name
* Calcuated company age and created a new variable
* Added a variable if the job was located at the company HQ
* Added a column for description length
* Added a column for seniority
* Classified job titles into broader categories and added as a new variable

## EDA
TBC
- images showing salary by job title/type/level
- salary by state/location
- correlation between continuous variables

## Model Building
Transformed the categorical variables into dummy variables then split data into train and test sets.

- Multiple Linear Regression – Baseline
- Lasso Regression
- Random Forest

## Model Performance
- Linear Regression: MAE = N/A
- Lasso Regression: MAE = 17.46
- Random Forest : MAE = 15.3

# Putting Into Production
Flask API endpoint hosted on local webserver following tutorial. Takes a list of values and returns estimated salary.
