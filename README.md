# How Can Organizations Predict and Curb Attrition Of Employees ?
## Introduction
One of the most common problems at work is turnover.

Replacing a worker earning about 50,000 dollars cost the company about 10,000 dollars or 20% of that worker’s yearly income according to the Center of American Progress.

Replacing a high-level employee can cost multiple of that...

Cost includes:

Cost of off-boarding
Cost of hiring (advertising, interviewing, hiring)
Cost of onboarding a new person (training, management time)
Lost productivity (a new person may take 1-2 years to reach the productivity of an existing person)
Annual Cost of Turnover = (Hiring + Onboarding + Development + Unfilled Time) * (# Employees x Annual Turnover Percentage)

Annual Cost of Turnover = (1,000 + 500) x (15,000 * 24%)

Annual Cost of Turnover) = 1500 x 3600

Annual Cost of Turnover) = 5400000

Example
Jobs (earning under 30k a year): the cost to replace a 10/hour retail employee would be 3,328 dollars.
Jobs (earning 30k-50k a year) - the cost to replace a 40k manager would be 8,000 dollars.
Jobs of executives (earning 100k+ a year) - the cost to replace a 100k CEO is 213,000 dollars.

## Objective:
To understand what factors contributed most to employee turnover.

To perform clustering to find any meaningful patterns of employee traits.

To create a model that predicts the likelihood of a certain employee will leave the company or not.

To create or improve different retention strategies for targeted employees.

The implementation of this model will allow management to create better decision-making actions.

We'll be covering:
Descriptive Analytics - What happened?
Predictive Analytics - What might happen?
Prescriptive Analytics - What should we do?

## Data Collection
All the data that I used for this project came from the Kaggle website(IBM HR Attrition Dataset). There were 35 features and 1499 observations. 
## Data Cleaning
As part of data cleansing, I implemented the following steps:

Dropped 4 features which had no predictive power(had constant values)
Checked for duplicate records
Checked for missing values and outliers
checked Datatypes of features for any anomalies
## Exploratory Data Analysis
Before building my predictive models, I undertook exploratory data analysis to see if I could uncover any evidence of a relationship between the attrition of an employee and its other attributes. These were the important findings
1)Single attrition rate is 50% in marital status.
2) Job Level -1 attrition rate is also high compared to other job levels
3)EnvironmentSatisfaction Level 1 has a high attrition rate.
4)Attrition rates are high in these attribute Sales Department, Male, Job satisfaction 
5) Employees who travel rarely have  higher attrition than employees who travel frequently
## Preprocessing
Created dummy variables for categorical features and then combined them with numerical features
Handled the problem of class imbalance by upsampling and downsamplimg the data. Concluded that SMOTE produced the best results.
## Modeling
Trained three models 
1) Logistic Regression
2) Random Forest Classifier
3) Gradient Boosting Classifier. 
Gradient Boosting Classifier provided the best results, so I used it to  predict the probability of employee leaving.
## Conclusion
Binary Classification: Turnover V.S. Non-Turnover

Instance Scoring: Likelihood of employee responding to an offer/incentive to save them from leaving.

Need for Application: Save employees from leaving

In our employee retention problem, rather than simply predicting whether an employee will leave the company within a certain time frame, we would much rather have an estimate of the probability that he/she will leave the company. We would rank employees by their probability of leaving, then allocate a limited incentive budget to the highest probability instances.

Consider the employee turnover domain where an employee is given treatment by Human Resources because they think the employee will leave the company within a month, but the employee  does not. This is a false positive. This mistake could be expensive, inconvenient, and time-consuming for both the Human Resources and employee but is a good investment for relational growth.

Compare this with the opposite error, where Human Resources does not give treatment/incentives to the employees and they do leave. This is a false negative. This type of error is more detrimental because the company lost an employee, which could lead to great setbacks and more money to rehire. Depending on these errors, different costs are weighed based on the type of employee being treated. For example, if it’s a high-salary employee then would we need a costlier form of treatment? What if it’s a low-salary employee? The cost for each error is different and should be weighed accordingly.

Solution 1:

We can rank employees by their probability of leaving, then allocate a limited incentive budget to the highest probability instances. OR, we can allocate our incentive budget to the instances with the highest expected loss, for which we'll need the probability of turnover. Solution 2: Develop learning programs for managers. Then use analytics to gauge their performance and measure progress. Some advice:

Be a good coach Empower the team and do not micromanage Express interest for team member success Have clear vision /strategy for team Help team with career development
