# Step-by-Step Guide to Modify the `Persons` Table

## Step 1: Create the Initial Table

First, create a table named `Persons`:

```sql
CREATE TABLE Persons
(
    ID int NOT NULL AUTO_INCREMENT,
    FirstName varchar(50) NOT NULL,
    LastName varchar(50),
    Address varchar(50),
    Email varchar(50),
    PRIMARY KEY (ID)
);
```

 ## Step : insart 4 data on  Persons table 
 ## Step : Add a New Column
Add a new column named PhoneNumber:
```sql
ALTER TABLE Persons ADD COLUMN PhoneNumber varchar(15);
```
 ## Insert Sample Data
Add sample data to the new column:
```sql
UPDATE Persons SET PhoneNumber = '555-0000';
```
 ## Change the PhoneNumber Data Type
```sql
ALTER TABLE Persons MODIFY COLUMN PhoneNumber varchar(20);
```