## Meta Database Engineer Professional Certificate

### Table of Contents
- [Database Structures and Management with MySQL](#database-structures-and-management-with-mysql)
  - [Module 1](#module-1)
  - [Module 2](#module-2)
      - [Subqueries](#subqueries)
  - [Module 3](#module-3)
      - [Functions in MySQL](#functions-in-mysql)
  - [Module 4](#module-4)

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


## Advanced MySQL Topics
### Functions and Trigers

