#sql #sqlCommands 

SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users to query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

We use SQL for CRUD Operations :
- CREATE - To create databases, tables, insert tuples in tables etc.
- READ - To read data present in the database.
- UPDATE - Modify already inserted data.
- DELETE - Delete database, table or specific data point/tuple/row or multiple rows.

<hr>
## SQL Data Types
In SQL, data types define the kind of data that can be stored in a column or variable.

Some Frequently used Data Types are:

![[SQL DataTypes.png]]

[All data types of MYSQL](https://dev.mysql.com/doc/refman/8.0/en/data-types.html)

>**Note** - CHAR is for fixed length & VARCHAR is for variable length strings. Generally,
  VARCHAR is better as it only occupies necessary memory & works more efficiently.

<hr>

---
## SQL Commands

#### 1.  [[DQL (Data Query Language)]] : Used to retrieve data from databases. (SELECT)

> Although often considered part of DML, the SQL `SELECT` statement is strictly speaking an example of DQL. When adding `FROM` or `WHERE` data manipulators to `SELECT` , the statement is then considered part of the DML.
#### 2. [[DDL (Data Definition Language)]] : Used to create, alter, and delete database objects like tables, indexes, etc. (CREATE, DROP, ALTER, RENAME, TRUNCATE)
#### 3. DML (Data Manipulation Language): Used to modify the database. (INSERT, UPDATE, DELETE)
#### 4. DCL (Data Control Language): Used to grant & revoke permissions. (GRANT, REVOKE)
#### 5. TCL (Transaction Control Language): Used to manage transactions. (COMMIT, ROLLBACK, START TRANSACTIONS, SAVEPOINT)

![[SQL Commands.png]]

> `DESCRIBE` : considered a metadata command used to retrieve information about the structure of database objects, primarily tables.
