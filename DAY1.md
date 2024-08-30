# Day 1 Notes

## 1. Data Definition Language (DDL)
- **Full Form:** Data Definition Language
- **Function:** Defines, modifies, and removes database structures (e.g., tables, indexes).
- **Commands:**
  - `CREATE`: Creates new tables, views, indexes, or databases.
  - `ALTER`: Modifies existing database objects (e.g., adding columns).
  - `DROP`: Deletes tables, views, or databases.
  - `TRUNCATE`: Removes all records from a table, but keeps the structure.

## 2. Data Manipulation Language (DML)
- **Full Form:** Data Manipulation Language
- **Function:** Manages and manipulates data within database tables.
- **Commands:**
  - `SELECT`: Retrieves data.
  - `INSERT`: Adds new records.
  - `UPDATE`: Modifies existing records.
  - `DELETE`: Removes records.

## 3. Data Control Language (DCL)
- **Full Form:** Data Control Language
- **Function:** Controls access to data in the database.
- **Commands:**
  - `GRANT`: Provides privileges to users or roles.
  - `REVOKE`: Removes privileges from users or roles.

## 4. Transaction Control Language (TCL)
- **Full Form:** Transaction Control Language
- **Function:** Manages transactions to ensure data integrity.
- **Commands:**
  - `COMMIT`: Saves changes made during a transaction.
  - `ROLLBACK`: Undoes changes made during a transaction.
  - `SAVEPOINT`: Sets a rollback point within a transaction.
  - `SET TRANSACTION`: Configures transaction properties (e.g., isolation level).

## Summary
- **DDL:** Defines and modifies database structures.
- **DML:** Manages and manipulates data.
- **DCL:** Controls access to data.
- **TCL:** Manages transactions and ensures data integrity.

## Data Types

### Numeric Data Types
- `INT`: Whole numbers. Variants: `SMALLINT`, `BIGINT`.
- `FLOAT`: Approximate floating-point numbers.
- `DOUBLE`: Double-precision floating-point numbers.
- `DECIMAL`: Exact numeric values, useful for financial data.

### Character/String Data Types
- `CHAR(n)`: Fixed-length string, pads with spaces.
- `VARCHAR(n)`: Variable-length string.
- `TEXT`: Large text data. Variants: `TINYTEXT`, `MEDIUMTEXT`, `LONGTEXT`.

### Date and Time Data Types
- `DATE`: YYYY-MM-DD.
- `TIME`: HH:MM:SS.
- `DATETIME`: YYYY-MM-DD HH:MM:SS.
- `TIMESTAMP`: Date and time, often for record creation/modification.
- `YEAR`: Year value.

### Binary Data Types
- `BINARY(n)`: Fixed-length binary data.
- `VARBINARY(n)`: Variable-length binary data.
- `BLOB`: Large binary objects. Variants: `TINYBLOB`, `MEDIUMBLOB`, `LONGBLOB`.

### Boolean Data Type
- `BOOLEAN`: Stores TRUE or FALSE.

### Special Data Types
- `ENUM`: Value from a predefined list.
- `SET`: Multiple values from a predefined list.

### Spatial Data Types
- `GEOMETRY`: Spatial data (e.g., points, lines).

### JSON Data Type
- `JSON`: Stores JSON-formatted data.

### Choosing Data Types
- **Efficiency:** Optimize storage and performance.
- **Accuracy:** Correct data storage and processing.
- **Validation:** Enforce data integrity and rules.

**Examples:**
- Customer ID: `INT` or `BIGINT`.
- Customer Names: `VARCHAR`.
- Order Dates: `DATE` or `DATETIME`.
- Product Descriptions: `TEXT`.

## Workflow

1. **Open and Run XAMPP:** Start XAMPP to work with databases locally.

2. **Create a Database**

   ```sql
   CREATE TABLE Teacher (
       TeacherID INT NOT NULL AUTO_INCREMENT,
       Name VARCHAR(100) NOT NULL,
       Designation VARCHAR(50),
       Address TEXT,
       Email VARCHAR(100),
       PRIMARY KEY (TeacherID)
   );

3. **Insert Data**
   ```sql
   INSERT INTO Teacher (Name, Designation, Address, Email)
   VALUES 
   ('John Doe', 'Professor', '123 Elm St, Springfield', 'johndoe@example.com'),
   ('Jane Smith', 'Lecturer', '456 Oak St, Springfield', 'janesmith@example.com');


4. **Update Data** 
   ```sql
   UPDATE Teacher
   SET joinDate = '2024-01-15'
   WHERE TeacherID = 1;
   UPDATE Teacher
   SET joinDate = '2024-02-20'WHERE TeacherID = 2;
