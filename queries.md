# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

SELECT ProductName, CategoryName FROM Products p INNER JOIN Categories c on p.CategoryID = c.CategoryID

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

SELECT OrderID, ShipperName FROM Orders o INNER JOIN Shippers s on o.ShipperID = s.ShipperID where o.OrderDate < "1997-01-09"

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

SELECT Quantity, ProductName
FROM [OrderDetails]
INNER JOIN Products where OrderDetails.ProductID = Products.ProductID AND OrderID = 10251

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

SELECT OrderID as "Id of Order", CustomerName as "Le name du Customere", LastName as "Employee's Surname" FROM (( Orders INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID ) INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID)

### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 