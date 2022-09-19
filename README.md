# SQL-exercises-Module 

1 Quiz

1. Select the jobs below that may use SQL in their work (select all that apply).
Data Scientist, QA Engineer, Backend Developer, DBA, Data Analyst

2. How does a data scientist and DBA differ in how they use SQL?
DBAs manage the database for other users.

3. Which of the following statements are true of Entity Relationship (ER) Diagrams?
They usually are represented in a visual format.
They show you the relationships between tables.
They identify the Primary Keys
They are usually a representation of a business process.

4. Select the query below that will retrieve all columns from the customers table.
SELECT * FROM customers

5. Select the query that will retrieve only the Customer First Name, Last Name, and Company.
SELECT 
FirstName
,LastName
,Company
FROM customers

6. The ER diagram below is depicting what kind of relationship between the EMPLOYEES and CUSTOMERS tables?
One-to-many

7. The data model depicted in the ER diagram below could be described as a _______________.
Relational Model

8. When using the "CREATE TABLE" command and creating new columns for that table, which of the following statements is true?
You must assign a data type to each column

9. Look at the values in the two columns below. Based on the values in each column, which column could potentially be used as a primary key?
Column 1	Column 2
5	        2
6	        4
1	        5
2	        5
34	       32
8	        6
9	        4
Column 1

10. In order to retrieve data from a table with SQL, every SQL statement must contain?
SELECT

Module 1 Coding Questions

1.
Question 1
For all of the questions in this quiz, we are using the Chinook database. All of the interactive code blocks have been setup to retrieve data only from this database.

Retrieve all the records from the Employees table.
Select *
from Employees

Question 2
Retrieve the FirstName, LastName, Birthdate, AddrRetrieve all the columns from the Tracks table, but only return 20 rows.ess, City, and State from the Employees table.
SELECT  FirstName, LastName, Birthdate, Address, City, State
FROM Employees


Question 3
Retrieve all the columns from the Tracks table, but only return 20 rows.
SELECT *
FROM Tracks
LIMIT 20

Module 2 Practice Quiz

2.
Question 2
Find the distinct values for the extended step. The code has been started for you, but you will need to program the third line yourself before running the query.
SELECT 
distinct Extended_step
FROM  salary_range_by_job_classification

3.
Question 3
Excluding $0.00, what is the minimum bi-weekly high rate of pay (please include the dollar sign and decimal point in your answer)? The code has been started for you, but you will need to add onto the last line of code to get the correct answer.
Select 
(Biweekly_high_Rate)
From salary_range_by_job_classification

4.
Question 4
What is the maximum biweekly high rate of pay (please include the dollar sign and decimal point in your answer)? The code has been started for you, but you will need to add onto the last line of code to get the correct answer.
SELECT 
Max(Biweekly_high_Rate) 
FROM salary_range_by_job_classification

.
Question 5
What is the pay type for all the job codes that start with '03'? The code has been started for you, but you will need to program the fourth and fifth lines yourself before running the query.
Select
job_code,
pay_type
FROM salary_range_by_job_classification
WHERE job_code LIKE '03%'

Question 6
Run a query to find the Effective Date (eff_date) or Salary End Date
(sal_end_date) for grade Q90H0? The code has been started for you, but you will need to program the third through the sixth lines yourself before running the query. 

Select Eff_Date, Sal_End_Date, Grade
FROM salary_range_by_job_classification
WHERE Grade = 'Q90H0'

7.
Question 7
Sort the Biweekly low rate in ascending order. There is no starter code, as you need to write and run the query on your own. Hint: there are 4 lines to run this query.
SELECT Biweekly_Low_Rate 
FROM salary_range_by_job_classification
ORDER BY Biweekly_Low_Rate ASC

8.
Question 8
Write and run a query, with no starter code to answer this question: What Step are Job Codes 0110-0400? Hint: there are 6 lines to run this query.
SELECT Job_Code, Step
FROM salary_range_by_job_classification
WHERE Job_Code BETWEEN 0110 AND 0400
LIMIT 30;

9.
Question 9
Write and run a query, with no starter code or hints to answer this question: What is the Biweekly High Rate minus the
Biweekly Low Rate for job Code 0170?
Select
Job_code,
Biweekly_high_rate,
Biweekly_low_rate, 
(biweekly_high_rate - Biweekly_low_rate) as calc
From salary_range_by_job_classification
Where Job_code = '0170'

10.
Question 10

Write and run a query, with no starter code or hints to answer this question: What is the Extended Step for Pay Types M, H, and D? 
SELECT Extended_Step, Pay_Type
FROM salary_range_by_job_classification
WHERE Pay_Type IN ('M', 'H', 'D')

11.
Question 11
Write and run a query, with no starter code or hints to answer this question: What is the step for
Union Code 990 and a Set ID of SFMTA or COMMN? 

SELECT Step, Union_Code, SetID
FROM salary_range_by_job_classification
WHERE Union_Code ='990' AND (SetID='SFMTA' OR SetID='COMMN');


