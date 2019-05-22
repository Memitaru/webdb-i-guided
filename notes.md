#SQL

###Select all products where category ID is 2

SELECT * FROM [Products] WHERE CategoryID = 2;

## Built in Functions/Alias/Keywords

AS for Alias

###Count items

SELECT COUNT(*) FROM Products; - Gives count number
SELECT COUNT(*) ProductCount FROM Products; Gives you back count in a column called ProductCount

### Length

SELECT CustomerName AS Name, length(CustomerName) AS NameLength FROM [Customers];
Gives a column of names and a column of the length of names


### Order by
SELECT CustomerName AS Name, length(CustomerName) AS NameLength FROM [Customers] ORDER BY NameLength;
SELECT CustomerName AS Name, length(CustomerName) AS NameLength FROM [Customers] ORDER BY NameLength DESC;
SELECT CustomerName AS Name, length(CustomerName) AS NameLength FROM [Customers] ORDER BY NameLength LIMIT 3;
Order list by name length

### Destinct
SELECT DISTINCT City from Customers ORDER BY City; - Removes all of the duplicates

### Like
SELECT * FROM Customers WHERE City = 'London'
SELECT * FROM Customers WHERE City LIKE '%on%'; - Any that contain the part between %
SELECT * FROM Customers WHERE City LIKE 'L_o' - _ can be anything, anything can be after the string

SELECT * FROM Customers WHERE City NOT LIKE '%on%; - Any that do not contain on will display

### Case Insensitive

SELECT * FROM Customers WHERE Lower(City) LIKE %on%;


# SQLite Studio