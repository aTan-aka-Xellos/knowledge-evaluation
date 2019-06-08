# Qualified
Database objects understanding. Perform simple data manipulation select/insert/delete. Limited understanding of complex data transformations.  

## Tables, relationships, keys, constraints understanding

## DDL, DML, DCL understanding

https://www.geeksforgeeks.org/sql-ddl-dml-dcl-tcl-commands/

![types_of_req](https://kdiv.files.wordpress.com/2015/04/sql-lang.jpg)

### DDL(Data Definition Language)
* CREATE
* DROP
* ALTER
* TRUNCATE

### DML(Data Manipulation Language)
* SELECT
* INSERT
* UPDATE
* DELETE

### TCL(transaction Control Language)
* COMMIT
* ROLLBACK
* SAVEPOINT
* SET TRANSACTION

### DCL(Data Control Language)
* GRANT
* REVOKE

## SQL data types
![types](https://cdn.journaldev.com/wp-content/uploads/2017/11/sql-data-types.png)

## SQL operators, functions

## Data manipulation (insert, update, delete)

## Retrieving data (simple select statement)

## Interview

## Joins understanding

https://www.w3schools.com/sql/sql_syntax.asp

![join](http://i.imgur.com/1m55Wqo.jpg)

# Competent
Ability to create database objects. Creating complex data transformations, creating stored procedures any complexity. Understanding sessions, locks and transactions.  

## Creating, modifying, removing database objects

## Aggregations (ORDER BY, GROUP BY, HAVING, SUM, COUNT, AVG, etc)

http://code.mu/sql/having.html
https://www.w3schools.com/sql/sql_syntax.asp

## Combining the results of multiple queries (union, except, intersect, minus, subqueries)

## Sessions, transactions, locks

https://codingsight.com/main-concept-of-sql-server-locking/

Connection represents connection to the server over a network or locally through shared memory.  
A session represents a user process within SQL Server.  

Exclusive (X)
Shared (S)
Update (U)
Intent (I)
Schema (Sch)
Bulk update (BU)

![lock_lvl](https://www.sqlshack.com/wp-content/uploads/2017/06/word-image-161.png)

## Isolation levels understanding

https://medium.com/pseudo-blog/%D1%83%D1%80%D0%BE%D0%B2%D0%BD%D0%B8-%D0%B8%D0%B7%D0%BE%D0%BB%D1%8F%D1%86%D0%B8%D0%B8-%D1%82%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D0%B9-87cd2b129de1

![isolations](https://cdn-images-1.medium.com/max/1200/1*aVUjZGDsABi9ajwxLggKlQ.jpeg)

* READ UNCOMMITTED
* READ COMMITTED
* REPEATABLE READ
* SNAPSHOT
* SERIALIZABLE
    
Side effects: LOST UPDATE, DIRTY READ, NON-REPEATABLE READ, PHANTOM READ.  
Isolation levels: Read Uncommitted < Read Committed (Snapshot) < Repeatable Read < Serializable / Snapshot.  

## Implementing stored procedures, user-defined functions, triggers

https://www.w3schools.com/sql/sql_stored_procedures.asp  
A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again.  
```
CREATE PROCEDURE procedure_name
AS
sql_statement
GO;
```

SQL Server triggers are special stored procedures that are executed automatically in response to the database object, database, and server events. SQL Server provides three type of triggers:  
* Data manipulation language (DML) triggers which are invoked automatically in response to INSERT, UPDATE, and DELETE events against tables.
* Data definition language (DDL) triggers which fire in response to CREATE, ALTER, and DROP statements. 
* Logon triggers which fire in response to LOGON events


User-defined functions cannot be used to perform actions that modify the database state.  
1. Scalar
2. Inline Table-Valued
3. Multi-statement Table-Valued


## Cursors
