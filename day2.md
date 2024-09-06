[ReadME](readme.md)  
# Day 2 Notes
 
# MySQL Integrity Constraints: Quick Reference

### 1. Primary Key Constraint
### 2. Foreign Key Constraint
### 3. Unique Constraint 
### 4.Not Null Constraint 
### 5. Check Constraint
Lab COde : 

step1: create Database
```sql
CREATE DATABASE LAB2 
```
Step 2:
```sql
CREATE TABLE Student (
    StudentID INT UNIQUE,
    FirstName VARCHAR(20) NOT NULL,
    LastName VARCHAR(20),
    Address VARCHAR(50),
    City VARCHAR(20) DEFAULT 'Dhaka'
);

```
Step 3:Insart data in table 
 ```sql 
 INSERT INTO `Student`(`StudentID`, `FirstName`, `LastName`, `Address`)
  VALUES
   ('1','[abc]','[ef]','[Bagladesh]')
```