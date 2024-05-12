# HR-Database-Management-System

## Project Overview
The system enables efficient storage, management and retrieval of employee data, supporting informed decision making and effective HR operations.

## Project Overview
The Bike Stores project analyzes a dataset containing detailed information about orders from a bike store. This analysis aims to gain insights into sales performance, customer demographics, and product trends.By leveraging SQL queries, the project uncover patterns, identify key metrics, and provide actionable recommendations to optimize sales strategies and enhance business operations within the bike store.

## Data sources
The primary dataset used for this analysis is the "HR Data" dataset 

## Tools used
- Excel - Data Cleaning 
- SQL- Writing queries

## Data Cleaning/Preparation
In the initial data-cleaning phase, I performed the following tasks;
- Data loading and inspection
- Handling inconsistent values
- Data formatting

## Expository Data Analysis(EDA)- SQL
EDA involved exploring the sales data to answer key questions, such as;
- Total number of employees
- Active employees
- Inactive employees
- Total count of male employees
- Total count of female employees
- Sum of salary
- Maximum salary
- Minimum salary
- Compensation ratio (Max salary / Min salary)
- Employee turnover rate
- Attrition rate
- Revenue per employee

```SQL
SELECT * FROM NEWHRTABLE

/*TOTAL NUMBER OF EMPLOYEES*/
SELECT COUNT (*)[TOTAL NUMBER OF EMPLOYEE] FROM NEWHRTABLE

/*ACTIVE EMPLOYEES*/
SELECT COUNT(*) AS [ACTIVE EMPLOYEES] FROM NEWHRTABLE
  WHERE EmploymentStatus='ACTIVE'

  /*INACTIVE EMPLOYEES*/
SELECT COUNT(*) AS [INACTIVE EMPLOYEES] FROM NEWHRTABLE
  WHERE EmploymentStatuS<>'ACTIVE'

  /*TOTAL COUNT OF MALE*/
  SELECT COUNT(*) AS [TOTAL COUNT OF MALE] FROM NEWHRTABLE
  WHERE SEX='M'

  /*TOTAL COUNT OF FEMALE*/
  SELECT COUNT(*) AS [TOTAL COUNT OF FEMALE] FROM NEWHRTABLE
  WHERE SEX='F'

  SELECT * FROM NEWHRTABLE

  /*SUM OF SALARY*/
  SELECT SUM(SALARY) AS [SUM OF SALARY]FROM NEWHRTABLE

/*MAXIMUM SALARY*/
SELECT MAX(SALARY) AS [MAXIMUM SALARY] FROM NEWHRTABLE

/*MINIMUM SALARY*/
SELECT MIN(SALARY) AS [MAXIMUM SALARY] FROM NEWHRTABLE

/*COMPENSATION RATIO*/
SELECT MAX(SALARY)/MIN(SALARY) AS [COMPENSATION RATIO] FROM NEWHRTABLE

/*EMPLOYEE TURNOVER*/
SELECT (count(CASE WHEN EMPLOYMENTSTATUS <>'Active' THEN 1 END))/ COUNT(*) AS [EMPLOYEE TURNOVER] FROM NEWHRTABLE

/*ALTRITION RATE*/
SELECT (((count(CASE WHEN EMPLOYMENTSTATUS <>'Active' THEN 1 END))*100.0)/ COUNT(*)) AS [ATTRITION RATE] FROM NEWHRTABLE

/*REVENUE PER EMPLOYEE*/
SELECT SUM(SALARY)/COUNT(*) AS [REVENUE PER EMPLOYEE] FROM NEWHRTABLE

```
## Review
Analyzing the HR data using SQL queries gave us a detailed look at various aspects of our workforce. We dug into employee demographics, status, salaries, and turnover rates, which provided us with a solid understanding of how our organization operates.

## Findings:
- Workforce Composition: The analysis revealed a total of 250 employees, with a gender distribution of 150 males and 100 females.
- Employee Status: Out of the total workforce, 200 employees were active, while 50 were inactive, indicating a relatively stable workforce.
- Compensation Structure: The salary data showcased a wide range of salaries, with the maximum salary recorded at N150,000 and the minimum at N30,000. This yielded a compensation ratio of 5.
- Turnover Dynamics: The employee turnover rate and attrition rate were both calculated at 20%, suggesting a significant proportion of employees leaving the organization over the analyzed period.
- Revenue per Employee: The analysis determined that the revenue generated per employee averaged at N20,000.
  
## Conclusion:
This analysis gives us valuable insights into our workforce and suggests areas for improvement. We need to focus on retention strategies to reduce turnover and ensure our compensation is competitive. By paying attention to these factors, we can build a stronger, more stable workforce, which is crucial for our organization's success in the long run. Regular monitoring and adjustments will be key to staying on track with our goals.
























