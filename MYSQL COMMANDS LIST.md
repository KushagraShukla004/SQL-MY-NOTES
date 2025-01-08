#sqlCommands #cmdCommands

These are MYSQL CMD Commands list only.
## Starting MySQL in cmd:
```
mysql -u root -p
```

## To clear whole screen:
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

## To see all the databases in mysql:
```
SHOW DATABASES;
```
## To create a database:
```
CREATE DATABASE db_name;
```

> After creating database we have to use `use db_name;` command in order to "use" the database to perform CRUD (CREATE, READ, UPDATE, DELETE) operations on.

## To use a database:
```
use db_name;
```

## To see all the tables in the database:
```
show tables;
```
## To create a table:
```
CREATE TABLE table_name (
col_name1 INT PRIMARY KEY,
col_name2 VARCHAR(20),
);
```

> You can write the whole query in single line , it's just to increase readability.
## To insert values in the table:
```
INSERT INTO table_name 
(rollNo,name) VALUES 
(1,"John Doe"),
(2, "Anything");
```
## To drop a database:
```
DROP DATABASE db_name;
```

## To Create Foreign Key:

``` 
CREATE TABLE Orders (  
    OrderID int NOT NULL,  
    OrderNumber int NOT NULL,  
    PersonID int,  
    PRIMARY KEY (OrderID),  
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)  
);
```

## To Update a value in table:
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