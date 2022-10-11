<h1 align="center">MYSQL ASSIGNMENT</h1>

# CREATE DATABASE

```javascript
CREATE DATABASE testdb; 
```

# SHOW EXISTING DATABASE

```javascript
SHOW CREATE DATABASE testdb; 
```
# USE COMMAND

```javascript
USE testdb;  
```

# CREATE TABLE EMPLOYEE

```javascript
CREATE TABLE Employee  
(  
EmployeeID int,  
FirstName varchar(255),  
LastName varchar(255),  
Email varchar(255),  
AddressLine varchar(255),  
City varchar(255)  
); 
```

# INSERT RECORDS IN EMPLOYEE TABLE

```javascript
INSERT INTO Employee (EmployeeID, FirstName, LastName, Email, AddressLine, City)
VALUES ('101', 'Lucas', 'Santos', 'lucassantos@gmail.com', 'Brazil', 'Sao Paulo'),
('102', 'Carlos', 'Santiago', 'carlossantiago@gmail.com', 'Argentina', 'Buenos Aires'),
('103', 'Emanuel', 'DaSilva', 'emanueldasilva@gmail.com', 'Brazil', 'Rio Grande do Sul'),
('104', 'Abril', 'Rodriguez', 'abrilrodrigues@gmail.com', 'Argentina', 'Mendoza'),
('105', 'Carolina', 'Bentresca', 'carolinabentresca@gmail.com', 'Chile', 'Concepsion'),
('106', 'Carol', 'Santos', 'carolsantos@gmail.com', 'Chile', 'Santiago'),
('107', 'Gabriela', 'Lopez', 'Gabrielalopez@gmail.com', 'Brazil', 'Amazonas'),
('108', 'Michael', 'DeCarvalho', 'michaeldecarvalho@gmail.com', 'Brazil', 'Fortaleza'),
('109', 'George', 'Spencer', 'georgespencer@gmail.com', 'United Kingdom', 'London'),
('110', 'Christina', 'Diemert', 'christinadiemert@gmail.com', 'United States', 'California');
```

# QUERIES 

1. From the following table return complete information about the employees.

```javascript
SELECT * FROM Employee;
```

2. From the following table, write a SQL query to find the cities of all employees. Return city.

```javascript
SELECT City FROM Employee;
```

3. From the following table, write a SQL query to find the unique addressline of the employees. Return addressline.

```javascript
SELECT DISTINCT AddressLine 
FROM Employee;
```

4. From the following table, write a SQL query to return EmployeeID, FirstName, LastName, City and AddressLine.

```javascript
SELECT EmployeeID,
       FirstName,
       LastName,
       City,
       AddressLine
FROM Employee;
```

5. From the following table, write a SQL query to count the number of characters except the spaces for each FirstName. Return FirstName length.

```javascript
SELECT length(trim(FirstName))
FROM Employee;
```

6. From the following table, write a SQL query to count the number of characters except the spaces for each LastName. Return LastName length. 

```javascript
SELECT length(trim(LastName))
FROM Employee;
```

7. From the following table, write a SQL query to find the EmployeeID, FirstName, Email of all the employees.

```javascript
SELECT EmployeeID,
       FirstName,
       Email
FROM Employee;
```

8. From the following table, write a SQL query to find the unique AddressLine with LastName. Return AddressLine and LastName.

```javascript
SELECT DISTINCT AddressLine, LastName
FROM Employee;
```

9. From the following table, write a SQL query to find those employees who do not belong to AddressLine Brazil. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine NOT IN ('Brazil');
```

10. From the following table, write a SQL query to find those employees who do not belong to AddressLine Argentina. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine NOT IN ('Argentina');
```

11. From the following table, write a SQL query to find those employees who EmployeeID's are before 105. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE EmployeeID<('105');
```

12. From the following table, write a SQL query to find those employees who EmployeeID's are after 105. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE EmployeeID>('105');
```

13. From the following table, write a SQL query to find those employees who EmployeeID's are before or equal to 105. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE EmployeeID<=('105');
```

14. From the following table, write a SQL query to find those employees who EmployeeID's are after or equal to 105. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE EmployeeID>=('105');
```

15. From the following table, write a SQL query to find those employees who EmployeeID is equal to 105. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE EmployeeID=('105');
```

16. From the following table, write a SQL query to find the details of the employee ‘Carol’.

```javascript
SELECT *
FROM Employee
WHERE FirstName = 'Carol';
```

17. From the following table, write a SQL query to find the FirstName of the employees whose length is six. Return employee FirstName.

```javascript
SELECT FirstName
FROM Employee
WHERE length(FirstName)=6;
```

18. From the following table, write a SQL query to find the details of the employee LastName ‘Santos’.

```javascript
SELECT *
FROM Employee
WHERE LastName = 'Santos';
```

19. From the following table, write a SQL query to find those employees whose AddressLine is ‘Brazil’. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine = 'Brazil';
```

20. From the following table, write a SQL query to find those employees whose AddressLine is ‘Argentina’. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine = 'Argentina';
```

21. From the following table, write a SQL query to find those employees whose AddressLine are either Brazil or Argentina. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine IN ('Brazil','Argentina');
```

22. From the following table, write a SQL query to find those employees whose AddressLine are either Chile or United States. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine IN ('Chile','United States');
```

23. From the following table, write a SQL query to find those employees whose AddressLine begin's with C. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine LIKE 'C%';
```

24. From the following table, write a SQL query to find those employees whose AddressLine ends with l. Return complete information about the employees. 

```javascript
SELECT *
FROM Employee
WHERE AddressLine LIKE '%l';
```

25. From the following table, write a SQL query to find those employees whose AddressLine values with 'rg' in between. Return complete information about the employees.

```javascript
SELECT *
FROM Employee
WHERE AddressLine LIKE '%rg%';
```

# LICENSE
This assignment is under <a href="https://github.com/ValentineFernandes/MySQL-Assignment/blob/main/LICENSE">MIT</a> license.
