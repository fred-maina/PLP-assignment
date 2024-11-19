# **Advanced SQL Queries and Aggregations**

## **Learning Objectives**
- Utilize SQL aggregation functions such as `COUNT`, `SUM`, `AVG`, `MIN`, and `MAX`.
- Perform grouped data analysis using `GROUP BY` and filter groups with `HAVING`.
- Sort and organize query results based on complex criteria.

---

## **What You'll Need**
- A computer with internet access.
- A code editor (e.g., Visual Studio Code).

---

## **Scenario**
You’ve collected valuable data in your database. Now, it's time to dive deep into that data and uncover insights by writing advanced SQL queries!

---

## **Submission Instructions**
1. Clone the project to your local computer.
2. Create a file named `answers.sql` in your project folder.
3. Run each query on MySQL Workbench and, once successful, copy and paste the query into `answers.sql` in VS Code.
4. Use comments to document your queries. For example:
   ```sql
   -- Question 1.1
   SELECT * FROM orders;
Push the code to GitHub when finished.
Assignment Questions
Part 1: Aggregation Basics
1.1). Write a query to calculate the total amount of all orders in the table.

sql
Copy code
-- Question 1.1
SELECT SUM(Total_Amount) AS Total_Orders_Amount
FROM orders;
1.2). Write a query to find the average order amount across all customers.

sql
Copy code
-- Question 1.2
SELECT AVG(Total_Amount) AS Average_Order_Amount
FROM orders;
1.3). Write a query to count the total number of orders placed for each product category.

sql
Copy code
-- Question 1.3
SELECT Product_Category, COUNT(*) AS Order_Count
FROM orders
GROUP BY Product_Category;
Part 2: Grouped Data Analysis
2.1). Write a query to retrieve the total quantity ordered for each product category.

sql
Copy code
-- Question 2.1
SELECT Product_Category, SUM(Quantity) AS Total_Quantity_Ordered
FROM orders
GROUP BY Product_Category;
2.2). Write a query to find product categories where the total quantity ordered exceeds 500.

sql
Copy code
-- Question 2.2
SELECT Product_Category, SUM(Quantity) AS Total_Quantity_Ordered
FROM orders
GROUP BY Product_Category
HAVING SUM(Quantity) > 500;
2.3). Write a query to calculate the average order amount for each customer and sort the results by the average amount in descending order.

sql
Copy code
-- Question 2.3
SELECT Customer_ID, AVG(Total_Amount) AS Average_Order_Amount
FROM orders
GROUP BY Customer_ID
ORDER BY Average_Order_Amount DESC;
Part 3: Using HAVING for Group Filtering
3.1). Write a query to find customers who have placed more than 10 orders. Display the Customer_ID and Order_Count.

sql
Copy code
-- Question 3.1
SELECT Customer_ID, COUNT(*) AS Order_Count
FROM orders
GROUP BY Customer_ID
HAVING COUNT(*) > 10;
3.2). Write a query to retrieve product categories where the total sales (sum of Total_Amount) is more than 10,000.

sql
Copy code
-- Question 3.2
SELECT Product_Category, SUM(Total_Amount) AS Total_Sales
FROM orders
GROUP BY Product_Category
HAVING SUM(Total_Amount) > 10000;
3.3). Write a query to calculate the total revenue for orders placed after '2024-01-01'.

sql
Copy code
-- Question 3.3
SELECT SUM(Total_Amount) AS Total_Revenue
FROM orders
WHERE Order_Date > '2024-01-01';
Part 4: Sorting and Combining Conditions
4.1). Write a query to retrieve all orders and sort them by Total_Amount in descending order.

sql
Copy code
-- Question 4.1
SELECT *
FROM orders
ORDER BY Total_Amount DESC;
4.2). Write a query to retrieve all customers who have spent more than 5,000 across all their orders, and sort the results by their total spending in descending order.

sql
Copy code
-- Question 4.2
SELECT Customer_ID, SUM(Total_Amount) AS Total_Spending
FROM orders
GROUP BY Customer_ID
HAVING SUM(Total_Amount) > 5000
ORDER BY Total_Spending DESC;
Bonus Challenge (Optional)
Write a query to list all orders placed in December 2024, grouped by product category, with a total sales value for each category.

sql
Copy code
-- Bonus Challenge
SELECT Product_Category, SUM(Total_Amount) AS Total_Sales
FROM orders
WHERE Order_Date BETWEEN '2024-12-01' AND '2024-12-31'
GROUP BY Product_Category;
