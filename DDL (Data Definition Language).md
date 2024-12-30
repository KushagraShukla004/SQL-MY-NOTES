#sqlCommands

It is a subset of [[SQL (Structured Query Language)]]
responsible for defining and managing the structure of databases and their objects.
DDL commands enable you to create, modify, and delete database objects like tables,
indexes, constraints, and more.

> - All the command of DDL are #auto-committed that means it permanently save all the changes in the database.

![[SS/DDL Commands.png]]
## Commands:

## Database related Queries:

#databaseQuery
### CREATE DATABASE:

CREATE Command is used to create databases, tables, triggers and other database objects.

SYNTAX-1:

```
CREATE DATABASE db_name;
```

![[SS/Create.png]]

---
#### Things to REMEMBER:

##### General Naming Conventions

1. **Descriptive Names**: Use full English words that clearly describe the purpose of the database or table. Avoid abbreviations unless they are widely recognized (e.g., "emp" for "employee")
2. **Lowercase Letters**: It is advisable to use lowercase letters for all identifiers, including database names, table names, and column names. This practice helps avoid confusion and potential errors when referencing these names in queries

> SQL will always convert database_name or table_name into **Lowercase** .i.e.  :
> ![[SS/CreateQueryLowerCase.png]]
> 

3. **Underscore Separation**: When separating words in identifiers, use underscores (e.g., `first_name`) instead of spaces or CamelCase (e.g., `FirstName`)
4. **Avoid Special Characters**: Refrain from using special characters (like `$`, `#`, etc.) in names unless necessary, as they can complicate queries and require quoting.

> Although using `$` and `#` doesn't particularly "break" the query but there are reasons as to not to use them.
> 
> Technically, you can only `CREATE` using `$` because the `#` is used for ***inline comment***.
> Example:
> 
>SQL `$` validity: 
>    
   ***Use Cases:*** The dollar sign is often used in naming conventions to signify special types of tables or databases. For example, it may indicate that a database is temporary or system-generated. In some contexts, such as when importing data from Excel, table names may automatically receive a trailing dollar sign to denote their origin.
>    
   ***Deprecation Warnings:*** While the dollar sign can be used as the first character in unquoted identifiers, it is important to note that this practice is deprecated in some SQL versions. This means that while it works, it may trigger warnings about future compatibility.
>    
>  ![[SS/CREATE with $.png]]
>  ---
>  
> When using `#`: 
> SQL ignore everything written after `#` and if we press `ENTER` it will simply move to next line for completing the SQL QUERY. 
> ![[SS/inlineComment.png]]


### DROP DATABASE: 

It is used to delete both the structure and record stored in the table. or database
#### SYNTAX for Database:

```
DROP DATABASE db_name; 
```

![[SS/Create,Drop.png]]


---
####  SYNTAX for table:

```
DROP TABLE table_name [cascade constraint];
```

The cascade constraint is an optional parameter which is used for tables which have foreign keys that reference the table being dropped. If cascade constraint is not specified and used attempt to drop a table that has records in a child table, then an error will occur. So by using cascade constraints, all child table foreign keys are dropped.


---

### CREATE DATABASE using `IF NOT EXISTS` :

SYNTAX:
```
CREATE DATABASE IF NOT EXISTS db_name;
```

Gives us extra security feature , i.e. If our backend doesn't contain database with the specified `db_name` then only create the database with that name otherwise do nothing and move on!. 

It helps in error handling without crashing the query.

Example:

> ![[SS/IF NOT EXISTS.png]]

As you can see , if the same DB exists it doesn't show any error or the query doesn't crashes , instead , It just doesn't create the database.

### DROP DATABASE using `IF EXISTS` : 

Syntax:
```
DROP DATABASE IF EXISTS db_name;
```

Works the same way like `IF NOT EXISTS` while CREATE-ing but instead finds if the DB or table exists . If it does exists then DROP the DB or table. 
If doesn't exists then do nothing and move on!.
No errors shown.

Example:
> ![[SS/IF EXISTS.png]]

As you can see it doesn't show any error even if the DB name doesn't exists.


---

## Table related Queries:

#tableQuery
### CREATE TABLE:

SYNTAX:
```
CREATE TABLE table_name (
column_name1 datatype constraint,
column_name2 datatype constraint,
);
```

Example:
> ![[SS/TableQueries.png]]

> DESCRIBE Command is a metadata command.
> 
> mainly comes under DQL Commands in SQL.
> for more info refer to :  [[DQL (Data Query Language)]]

### DROP Table:
Syntax:
```
DROP TABLE table_name;
```

### ALTER:

The `ALTER TABLE` statement in SQL is used to add, remove, or modify columns in an existing table. The ALTER TABLE statement is also used to add and remove various constraints on existing tables.

It allows for structural changes like adding new columns, modifying existing ones, deleting columns, and renaming columns within a table.

SYNTAX:
```
ALTER TABLE table_name
clause [column_name] [datatype];
```
`

