# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

SELECT p.productName, c.categoryName FROM Products as p
join categories as c on p.categoryID = c.categoryID

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

select o.orderId, s.shipperName, o.orderDate from orders as o
join shippers as s on o.shipperId = s.shipperID
where o.orderDate < "1997-01-09"

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

select o.orderID, o.quantity, p.productName from orderDetails as o
join products as p on o.productID = p.productID
where o.orderID = "10251"
order by p.productName

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

select o.orderID, c.customerName, e.lastName from orders as o inner join customers as c on o.customerID = c.customerID inner join employees as e on o.employeeId = e.employeeID

### (Stretch) Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a column called ItemCount that shows the total number of products placed on the order. Shows 196 records.
