[ReadME](readme.md)  
# Day 2 Notes
 
# MySQL Integrity Constraints: Quick Reference

<ol> 
    <li> Primary Key Constraint</li>
    <li> Foreign Key Constraint</li>
    <li> Unique Constraint </li>
    <li> Not Null Constraint </li>
    <li> Check Constraint </li>
</ol>

 
Lab Code : 

Step 1: Create Database
```sql
CREATE DATABASE LAB2 
```
Step 2: Create `Student` Table
```sql
CREATE TABLE Student (
    StudentID INT UNIQUE,
    FirstName VARCHAR(20) NOT NULL,
    LastName VARCHAR(20),
    Address VARCHAR(50),
    City VARCHAR(20) DEFAULT 'Dhaka'
);

```
Step 3: Insert Data into `Student` Table
 ```sql 
 INSERT INTO `Student`(`StudentID`, `FirstName`, `LastName`, `Address`)
  VALUES
   ('1','[abc]','[ef]','[Bagladesh]')
```

Step 4: Create `Players` Table with Primary Key
``` sql
CREATE TABLE Players(
    player_No INT,
    Players_Name VARCHAR(20) NOT NULL,
    Legue_no INT,
    PRIMARY KEY(player_No)
);
 ```
 Step 5: Create `Team` Table with Foreign Key Constraint
 ``` sql
 CREATE TABLE Team(
    Team_no INT,
    Players_no VARCHAR(20) NOT NULL,
    Division char(15),
    PRIMARY KEY(Team_no),
    FOREIGN KEY (Players_no) REFERENCES Players (player_No)
);
```

Step 6:  
Insert data into `Players` table:
```sql 
INSERT INTO Players (player_No, Players_Name, Legue_no)
VALUES
    (1, 'John Doe', 101),
    (2, 'Jane Smith', 102),
    (3, 'Alice Johnson', 103);
```

Insert data into Team table:
```sql
INSERT INTO Team (Team_no, Players_no, Division)
VALUES
    (1, '1', 'East'),
    (2, '2', 'West'),
    (3, '3', 'North');
```
