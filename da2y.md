
## Types of SQL Commands 

DDL (Data Definition Language) : create, alter, rename, truncate & drop. 

DQL (Data Query Language) 

DML (Data Manipulation Language) : , insert, update & delete 

DCL (Data Control Language) : grant & revoke permission to users 

TCL (Transaction Control Language) : start transaction, commit, rollback €

---
[DAY 1](day1.md) 

### Create Database 
```sql
CREATE DATABASE database_Name;
```
### Delete database 
```sql
DROP DATABESE databes_Name
```
### Create Table

```sql
CREATE TABLE student( id INT PRIMARY KEY, name VARCHAR(50), age INT NOT NULL );

```
### insart data

```sql
INSERT INTO student VALUES(1,'adnan',24)
```

