# SQL Basics - Episode 01 Summary

## Database Fundamentals
- Tables are fundamental structures in databases
- Data is organized in rows and columns
- Each table represents a specific entity or concept

## MySQL Setup in WSL
1. Installation Steps:
   ```bash
   sudo apt update
   sudo apt install mysql-server
   sudo mysql
   ```

## Basic Database Operations
### Database Management
- Create database: `CREATE DATABASE database_name;`
- View all databases: `SHOW DATABASES;`
- Select database: `USE database_name;`
- Delete database: `DROP DATABASE database_name;`

### Table Operations
1. Creating Tables
   - Basic syntax: `CREATE TABLE table_name (column1 datatype, column2 datatype, ...);`
   - View tables: `SHOW TABLES;`
   - View table structure: `DESCRIBE table_name;`

2. Data Types Learned
   - VARCHAR: For variable-length strings
     - Requires length specification
   - DECIMAL: For precise decimal numbers
     - First argument: Total digits
     - Second argument: Decimal places

3. Data Manipulation
   - Insert data: `INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);`
   - View data: `SELECT * FROM table_name;`
   - Delete table: `DROP TABLE table_name;`
   - Clear table data: `DELETE FROM table_name;`

## Data Retrieval
### SELECT Statements
- Select all columns: `SELECT * FROM table_name;`
- Select specific columns: `SELECT column1, column2, ... FROM table_name;`
- Column order is flexible in SELECT statements

### Data Limiting
- Limit results: `SELECT * FROM table_name LIMIT n;`
- Example: `SELECT * FROM customers LIMIT 2;`

### Data Sorting
- Ascending order: `ORDER BY column_name ASC;`
- Descending order: `ORDER BY column_name DESC;`
- Multiple column sorting: `ORDER BY column1 ASC, column2 DESC;`

## SQL Command Categories
1. DDL (Data Definition Language)
   - Used for defining database structures
2. DML (Data Manipulation Language)
   - Used for manipulating data
3. DCL (Data Control Language)
   - Used for controlling access to data

## Key Takeaways
- Learned basic database and table creation
- Understood fundamental data types
- Mastered basic data insertion and retrieval
- Explored sorting and limiting results
- Gained knowledge of different SQL command types