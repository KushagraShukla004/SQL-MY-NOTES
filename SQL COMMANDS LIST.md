#sqlCommands #cmdCommands

#### Starting MySQL in cmd:
```
mysql -u root -p
```

#### To clear whole screen:
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

#### To see all the databases in mysql:
```
SHOW DATABASES;
```

#### To use a database:
```
use db_name;
```

#### To create a database:
```
CREATE DATABASE db_name;
```

> After creating database we have to use `use db_name;` command in order to "use" the database to perform CRUD (CREATE, READ, UPDATE, DELETE) operations on.
#### To create a table:
```
CREATE TABLE table_name (
col_name1 INT PRIMARY KEY,
col_name2 VARCHAR(20),
);
```

> You can write the whole query in single line , it's just to increase readability.
#### To insert values in the table:
```
INSERT INTO table_name 
(rollNo,name) VALUES 
(1,"John Doe")
(2, "Anything")
```

> Writing column name helps remembering order of values to put in because if the order changes then the column it will be put into will change as well which could lead to datatype errors and misplaced information. 
> For Example:

Output of Above Query:

| rollNo | Name     |
| ------ | -------- |
| 1      | JohnDoe  |
| 2      | Anything |
> Hence, we can understand which value comes first and which column datatype is INT and which is VARCHAR (String).

#### To drop a database:
```
DROP DATABASE db_name;
```