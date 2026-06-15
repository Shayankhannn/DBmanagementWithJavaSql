Scenario
The Chinook Music Store operates globally and manages its sales transactions through a comprehensive digital database. As part of the financial team, you have been tasked with analyzing various aspects of sales data to provide insights into business performance, customer spending behaviours, and overall revenue generation. The analysis will support strategic decisions regarding marketing campaigns, customer relationship management, and product placement.

Goal

Apply SQL operations to analyze sales data, focusing on identifying high-value transactions, measuring total revenue, and segmenting high-spending customers to enhance strategic decision-making and optimize marketing and sales efforts.



Write the SQL query:

Construct an SQL query to retrieve all columns from the Invoice table.

Apply the ORDER BY clause to sort the results by the Total column in descending order.

ans :

SELECT * FROM Invoice ORDER BY Total DESC;

---

Formulate the SQL query:



Write a query that uses the SUM() function to calculate the total revenue. Multiply UnitPrice by Quantity for each line item before summing up these values.

ANS :

SELECT UnitPrice ,Quantity , SUM(UnitPrice*Quantity) AS TotalRevenue FROM InvoiceLine GROUP BY Quantity,UnitPrice;

WRONG 
CORRECT ONE :
SELECT SUM(Quantity*UnitPrice) AS TotalRevenue FROM InvoiceLine;




Construct the SQL query:

Write a query to calculate the total amount spent by each customer using the SUM() function on the Total column of the Invoice table.

Use the GROUP BY clause to organize sums by customer.

Include a HAVING clause to filter out customers who have spent more than a certain threshold (e.g., $45).

ANSWER :

without join 

SELECT CustomerId , SUM(Total) AS TotalSpent FROM Invoice  GROUP BY CustomerId HAVING SUM(Total) > 45;

with join

SELECT c.FirstName,c.LastName, SUM(i.Total) AS TotalSpent FROM Customer c
JOIN Invoice i ON c.CustomerId = i.CustomerId GROUP BY c.CustomerId , c.FirstName , c.LastName HAVING SUM(i.Total) > 45;
