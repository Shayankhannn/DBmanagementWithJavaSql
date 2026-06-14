Activity: Accessing, updating, and filtering
Scenario
Sam is very excited about the possibilities of managing the online bookshop's inventory with SQL. However, to effectively manage a relational database, you'll need more than the four foundational SQL commands: SELECT, INSERT, UPDATE, and DELETE. 

In this lab, you'll apply the SQL syntax you learned to date and apply new commands to access, update, and filter data. Combined with the previous commands you learned, you will have the critical skills to help manage Sam's inventory.

Sam provided an inventory table named Sales with 10 records. Each record details a transaction with a unique ID, sale date, quantity sold, book ISBN, and total sale amount, as shown in the Sales table below. View the table to familiarize yourself with the provided data.

WORKING :

TASK 2: Accessing Data

SELECT * FROM Sales;
--

TASK 2: Accessing Data

SELECT SaleDate, TotalSaleAmount
FROM Sales;
----
TASK 3: Updating Data

UPDATE  Sales SET QuantitySold = 2 WHERE TransactionID = 10;

---
Task 4: Filtering Data

SELECT * FROM Sales WHERE SaleDate > '2023-08-03';