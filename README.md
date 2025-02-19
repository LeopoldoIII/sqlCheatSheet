# sqlCheatSheet

## Relational database

A relational database is a type of database that organizes data into tables (relations) with rows and columns. Each table represents an entity (like customers or products), and relationships between tables are managed through keys.

Key Concepts:
* Tables: Store data about entities with rows (records) and columns (attributes).
* Primary Key: A unique identifier for each record in a table.
* Foreign Key: Links records between tables, creating relationships.
* Relationships: One-to-one, one-to-many, and many-to-many connections between tables.
* Normalization: Organizing tables to reduce redundancy and improve data integrity.
* SQL (Structured Query Language): The language used to query, insert, update, and manage data.

### Integrity constraints

Integrity constraints are rules applied to databases tables to ensure the accuracy and consistency of the data. Here are the main types of integfity constraints: 

1 *Primary Key Constraint:* Ensures that each row in a table is unique and not null It uniquely identifies each record in the table

  ```
  CREATE TABLE Emloyees (
    EmployeeID INT PRIMARY KEY,
    Name VARCHAR(100)
  );
  ```

2 *Foreign Key Constraint:* Ensures that the value in one table matches a value in another table, maintaining referential integrity

```
  CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    EmployeeID INT,
    FOREIGN KEY (EmployeeID) REFERENCES
  Employees(EmplyeeID)
  ):
```

3 *Unique Constraint:* Ensures that all values in a column are unique

```
  CREATE TABLE Users (
      UserID INT PRIMARY KEY,
      Email VARCHAR(100) UNIQUE
  );
```

4 *Not Null Constraint:* Ensures that a column cannot have a null value

```
  CREATE TABLE Products (
      ProductID INT PRIMARY KEY,
      ProductName VARCHAR(100) NOT NULL
  );
```

5 *Check Constraint:* Ensures that all values in a column satisfy a specific condition

```
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    Age INT CHECK (Age >= 18)
);
```

