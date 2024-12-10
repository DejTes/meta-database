## Meta Database Engineer Professional Certificate

### Table of Contents
- [Database Structures and Management with MySQL](#database-structures-and-management-with-mysql)
  - [Module 1](#module-1)
  - [Module 2](#module-2)
      - [Subqueries](#subqueries)
  - [Module 3](#module-3)
      - [Functions in MySQL](#functions-in-mysql)
      - [Procuders](#Procudeures)
  - [Module 4](#module-4)
- [Advanced MySQL Topics](#advanced-mysql-topics)
  - [Functions and Trigers](#functions-and-trigers)

---

## Database Structures and Management with MySQL
#### database-structures-and-management-with-mysql
### module 2
#### Subqueries
 - A subquery is a query nested within another query, where the inner query (child) executes first and its results are used by the outer query (parent).
 - Subqueries must be enclosed in parentheses and can return various results, such as a single value, row, column, or multiple rows.
 Syntax: 
  ```sql
  SELECT column_name(s)
  FROM table_name
  WHERE column_name operator
  (SELECT column_name(s)
  FROM table_name
  WHERE condition);
  ```
  - Subqueries and Comparison Operators
    - **Comparison Operators**: Used to compare values in a subquery with values in the main query.
    - **IN Operator**: Used to compare a value with a list of values.
    - **ANY Operator**: Used to compare a value with any value in a list.
    - **ALL Operator**: Used to compare a value with all values in a list.
    - **EXISTS Operator**: Used to check the existence of rows in a subquery.
    - **SOME Operator**: Used to compare a value with some values in a list.

### Module 3
#### Functions in MySQL
1. **Numeric Functions**
    - **Aggregate Functions**: Perform a calculation on a set of values and return a single value.
        - `AVG()`: Returns the average value of a numeric column.  
            
          ```sql
          SELECT AVG(column_name) FROM table_name;
          ```
        - `COUNT()`: Returns the number of rows that match a specified criterion.
        - `MAX()`: Returns the maximum value in a column.
        - `MIN()`: Returns the minimum value in a column.
        - `SUM()`: Returns the total sum of a numeric column.

    - **Mathematical Functions**: Perform a mathematical operation and return a single value.
        - `ABS()`: Returns the absolute value of a number.  
            
          ```sql
          SELECT ABS(column_name) FROM table_name;
          ```
        - `CEIL()`: Returns the smallest integer value greater than or equal to a number.
        - `FLOOR()`: Returns the largest integer value less than or equal to a number.
        - `ROUND()`: Rounds a number to a specified number of decimal places.  
            
          ```sql
          SELECT ROUND(column_name, decimal_places) FROM table_name;
          ```
        - `MOD()`: Returns the remainder of a division.  
            
          ```sql
          SELECT MOD(column_name, divisor) FROM table_name;
          ```
        - `RAND()`: Generates a random number.
        - `TRUNCATE()`: Truncates a number to a specified number of decimal places.

2. **String Functions**: Perform operations on a string and return a string value.
    - `CONCAT()`: Concatenates two or more strings.  
        
      ```sql
      SELECT CONCAT(column1, column2) FROM table_name;
      ```
    - `LENGTH()`: Returns the length of a string.  
        
      ```sql
      SELECT LENGTH(column_name) FROM table_name;
      ```
    - `LOWER()`: Converts a string to lowercase.  
        
      ```sql
      SELECT LOWER(column_name) FROM table_name;
      ```
    - `UPPER()`: Converts a string to uppercase.  
        
      ```sql
      SELECT UPPER(column_name) FROM table_name;
      ```
    - `REPLACE()`: Replaces a substring within a string with another substring.  
        
      ```sql
      SELECT REPLACE(column_name, 'old_string', 'new_string') FROM table_name;
      ```
    - `SUBSTRING()`: Extracts a substring from a string.  
        
      ```sql
      SELECT SUBSTRING(column_name, start_position, length) FROM table_name;
      ```

3. **Date Functions**: Date functions in MySQL are used to extract and format date and time values in various formats.
    - `CURDATE()`: Returns the current date.
        ```sql 
        SELECT CURDATE();   // Output: 2021-09-01
        ``` 
         
    - `CURTIME()`: Returns the current time.
       ```sql 
       SELECT CURTIME();    // Output: 12:00:00
       ```
    - `NOW()`: Returns the current date and time. 
        ```sql 
        SELECT NOW();    // Output: 2021-09-01 12:00:00
        ```
    - `DATE()`: Extracts the date part of a date or datetime expression.
        ```sql
        SELECT DATE(column_name) FROM table_name;  
        ```
    - `TIME()`: Extracts the time part of a date or datetime expression.
    - `DATEDIFF()` : Returns the number of days between two dates.
        ```sql
        SELECT DATEDIFF(date1, date2) FROM table_name;
        ```
    - `DAYNAME()`: Returns the name of the weekday.
    - `MONTHNAME()`: Returns the name of the month.
    - `DAY()`: Returns the day of the month.
  

4. **Control Flow Functions**: Control flow functions in MySQL are used to control the flow of execution in a stored procedure or function.
    - `CASE`: Evaluates a list of conditions and returns one of multiple possible results.
      ```sql
      SELECT column_name,
        CASE
          WHEN condition1 THEN result1
          WHEN condition2 THEN result2
          ELSE result3
        END
      FROM table_name;
      ```
    - `IF()`: Returns one value if a condition is true and another value if the condition is false.
    - `IFNULL()`: Returns a specified value if a column is NULL.
    - `NULLIF()`: Returns NULL if two expressions are equal.

5. **Comparison Functions**: Comparison functions in MySQL are used to compare values and return a result based on the comparison.
    - `COALESCE()`: Returns the first non-NULL value in a list.
      ```sql
      SELECT COALESCE(column1, column2, column3) FROM table_name;
      ```
    - `GREATEST()`: Returns the greatest value in a list.
        ```sql
        SELECT GREATEST(column1, column2, column3) FROM table_name;
        ```

    - `LEAST()`: Returns the smallest value in a list.
        ```sql
        SELECT LEAST(column1, column2, column3) FROM table_name;
        ```

## Procedures
#### Procedures
-  Stored Procuders are a set of SQL statements that are stored in the database and can be executed on demand. They are used to encapsulate a set of operations or queries that need to be performed repeatedly.
- The stored procedure in MySQL is a set of SQL instructions wrapped within the CREATE PROCEDURE statement to achieve a particular objective. 
- Benefits include code consistency, reusability, and easier maintenance, reducing the need to rewrite the same SQL statements.
- To create a stored procedure, use the CREATE PROCEDURE command followed by the procedure name and parameters (if any), then write the procedure logic.
- To invoke a stored procedure, use the CALL command followed by the procedure name and parentheses.
- If a stored procedure is no longer needed, it can be removed using the DROP PROCEDURE command followed by the procedure name, without parentheses.
- The main idea behind creating stored procedures is to create reusable code that can be invoked and executed efficiently

Syntax:
```sql
CREATE PROCEDURE procedure_name(parameter_value INT)
SELECT column_name
FROM table_name
WHERE value = parameter_value;
```


## Advanced MySQL Topics
### Functions and Trigers

- Differences between functions and stored procedures

- Functions and procedures are used to encapsulate code that can be executed to implement repetitive tasks such as equations, formulas or business rules.

- In addition, functions and stored procedures make your code more consistent, reusable and easier to use and maintain. 

```sql
 SELECT * FROM Clinets;

 You can wrap this statement in a stored procedure as follows:

 DELIMITER //
CREATE PROCEDURE GetAllClients()
BEGIN
SELECT * FROM Clients;
END //
DELIMITER;

```
  Functions (Stored functions)                    |             STORED PROCEDURES   
--------------------------------------------------|---------------------------------
1. Created using CREATE FUNCTION command          | Created using CREATE PROCEDURE command
2. Invoked using the SELECT statement             | Invoked using the CALL statement
3. Returns a single value                         | Can return multiple values
4. Takes IN parameters only                       | Can take IN, OUT, and INOUT parameters
5. Typically encapsulates common formulas or generic business rules | Typically used to process, manipulate and modify data in the database
6. Must specify the data type of the return value | User must specify the OUT parameter type

## MySQL Triggers and events


- What is a MySQL Trigger?
 - A MySQL trigger is a stored program that automatically executes a set of actions when specific events occur, such as inserting, updating, or deleting data from a table.
 - Triggers help avoid the need to rewrite code for recurring actions, making database management more efficient.

- Creating and Dropping Triggers

  - To create a trigger, use the CREATE TRIGGER statement, followed by a unique trigger name, trigger type (insert, update, delete), and the table it applies to.

  - To drop a trigger, use the DROP TRIGGER command with the IF EXISTS clause to prevent errors if the trigger does not exist.

  ### Types of Triggers
  There are two main types of triggers: 
  - Row-level triggers, which are invoked for each row affected by an action, and 
  - Statement-level triggers, which are invoked once per action regardless of the number of rows.

- MySQL supports only row-level triggers, which are essential for performing actions like inserting, updating, or deleting data in a table.