#sqlCommands #cmdCommands

These are MYSQL CMD Commands list only.
## 🚀 Starting MySQL in cmd:
```
mysql -u root -p
```

## 🧹 To clear whole screen:
```
system cls
```
OR
```
system clear
```
OR
```
\! cls
```

## 👁️ To see all the databases in mysql:
```
SHOW DATABASES;
```
## 🖋️ To create a database:
```
CREATE DATABASE db_name;
```

> After creating database we have to use `use db_name;` command in order to "use" the database to perform CRUD (CREATE, READ, UPDATE, DELETE) operations on.

## 🧑‍💻 To use a database:
```
use db_name;
```

## 👁️ To see all the tables in the database:
```
show tables;
```
## 🖋️ To create a table:
```
CREATE TABLE table_name (
col_name1 INT PRIMARY KEY,
col_name2 VARCHAR(20),
);
```

> You can write the whole query in single line , it's just to increase readability.
## 📝 To insert values in the table:
```
INSERT INTO table_name 
(rollNo,name) VALUES 
(1,"John Doe"),
(2, "Anything");
```
## ❌ To drop a database:
```
DROP DATABASE db_name;
```

## 🖋️ To Create Foreign Key:

``` 
CREATE TABLE Orders (  
    OrderID int NOT NULL,  
    OrderNumber int NOT NULL,  
    PersonID int,  
    PRIMARY KEY (OrderID),  
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)  
);
```

## 📝 To Update a value in table:
```
UPDATE _table_name_  
SET _column1_ = _value1_, _column2_ = _value2_, ...  
WHERE _condition_;
```
For Example , if you want to change subject name from Bio to Biology: 
```
UPDATE student
SET subject = "Biology"
WERE subject = "Bio"; 
```

##  ❌ To Delete records from a Table:
```
DELETE FROM Table_Name WHERE condition;
```

To delete every record in the Table :
```
DELETE FROM Table_Name;
```

## 🤏 To Select records from column in a Table:
Show / Select records of all columns 
```
SELECT * FROM table_name;
```
---
Show / Select records of specific columns only ( you can add (n) number of cols)  :
```
SELECT col1_name, col2_name FROM table_name;
```
---
Show / Select columns from different tables together:
```
SELECT table1.col_name, table2.col_name FROM table1, table2;
```
---
Show / Select records in order:
Ascending Order:
```
SELECT col_name FROM table_name ORDER BY col_name ASC;
```
Descending Order:
```
SELECT col_name FROM table_name ORDER BY col_name DESC;
```
---
Show / Select limited number of records only: 
```
SELECT col_name FROM table_name LIMIT 2;
```
