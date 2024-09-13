# Step-by-Step Guide to Modify the `Persons` Table

## Step : Create the Initial Table

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
 ```sql 
 INSERT INTO Persons (FirstName, LastName, Address, Email)
VALUES 
('John', 'Doe', '123 Main St', 'john.doe@example.com'),
('Jane', 'Smith', '456 Elm St', 'jane.smith@example.com'),
('Alice', 'Johnson', '789 Oak St', 'alice.johnson@example.com'),
('Bob', 'Brown', '101 Pine St', 'bob.brown@example.com');

```
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

## Step 4: Update Existing Records with Sample Phone Numbers

```sql
UPDATE Persons
SET PhoneNumber = CASE ID
    WHEN 1 THEN '555-0001'
    WHEN 2 THEN '555-0002'
    WHEN 3 THEN '555-0003'
    WHEN 4 THEN '555-0004'
    ELSE PhoneNumber
END;
 ```

## col name  change 

```sql 
ALTER TABLE `Persons`
CHANGE `Address` `Permanent_Address` VARCHAR(255);
```
