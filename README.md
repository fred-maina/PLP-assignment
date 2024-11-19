# SQL Assignment Week 2: Bill Management System (Introduction to SQL)

## Learning Objectives
- Practice basic SQL syntax and retrieval operations.
- Retrieve and filter data from a database using SQL.
- Understand how to apply conditions, sorting, and aggregations.

## What You'll Need
- A computer with internet access.
- A code editor (e.g., Visual Studio Code).
- MySQL Workbench or another SQL database environment.

## Scenario
You are tasked with retrieving and managing data from a Bill Management System's database. The system tracks customer bills, including their status, due dates, and amounts. This assignment will help you practice SQL queries related to data retrieval and filtering operations.

## Submission Instructions
1. Clone the project to your local computer.
2. Create a file named `answers.sql` in your project folder.
3. Run each query on MySQL Workbench and, once successful, copy and paste the query into `answers.sql` in VS Code.
4. Use comments to document your queries. For example:
   ```sql
   -- Question 1.1
   SELECT * FROM orders;
Push the code to GitHub when finished.

## Assignment Questions

1. Retrieving All Data
Write an SQL query to retrieve all columns for all the bills in the Bills table.

2. Selecting Specific Columns
Write an SQL query to retrieve only the Bill_ID and TotalAmount columns from the Bills table.

3. Filtering Data by Amount
Write an SQL query to retrieve all bills where the TotalAmount is greater than 100. Display the Bill_ID, TotalAmount, and Due_Date.

4. Filtering Data by Status
Write an SQL query to retrieve all bills where the Status is 'Pending'. Show the Bill_ID, Amount, Due_Date, and Status.

5. Filtering Data by Date
Write an SQL query to retrieve all bills where the Issue_Date is after '2024-01-01'. Show the Bill_ID, Amount, Issue_Date, and Due_Date.

6. Combining Conditions
Write an SQL query to retrieve all bills where the TotalAmount is greater than 50 and the Status is 'Pending'. Display the Bill_ID, TotalAmount, Status, and Due_Date.

7. Sorting Data by Amount
Write an SQL query to retrieve all bills, but sort them by TotalAmount in descending order (highest to lowest). Display Bill_ID, Amount, and Status.

8. Sorting Data by Due Date
Write an SQL query to retrieve all bills sorted by Due_Date in ascending order. Show Bill_ID, TotalAmount, Due_Date, and Status.

9. Filtering and Sorting Combined
Write an SQL query to retrieve all bills where the Status is 'Overdue', and sort the results by Due_Date in ascending order. Show the Bill_ID, TotalAmount, Due_Date, and Status.

10. Finding Bills by Customer
Write an SQL query to retrieve all bills for a specific customer, say with Customer_ID = 123. Show the Bill_ID, TotalAmount, Due_Date, and Status.
