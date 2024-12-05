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
          **Syntax:**  
          ```sql
          SELECT AVG(column_name) FROM table_name;
          ```
        - `COUNT()`: Returns the number of rows that match a specified criterion.
        - `MAX()`: Returns the maximum value in a column.
        - `MIN()`: Returns the minimum value in a column.
        - `SUM()`: Returns the total sum of a numeric column.

    - **Mathematical Functions**: Perform a mathematical operation and return a single value.
        - `ABS()`: Returns the absolute value of a number.  
          **Syntax:**  
          ```sql
          SELECT ABS(column_name) FROM table_name;
          ```
        - `CEIL()`: Returns the smallest integer value greater than or equal to a number.
        - `FLOOR()`: Returns the largest integer value less than or equal to a number.
        - `ROUND()`: Rounds a number to a specified number of decimal places.  
          **Syntax:**  
          ```sql
          SELECT ROUND(column_name, decimal_places) FROM table_name;
          ```
        - `MOD()`: Returns the remainder of a division.  
          **Syntax:**  
          ```sql
          SELECT MOD(column_name, divisor) FROM table_name;
          ```
        - `RAND()`: Generates a random number.
        - `TRUNCATE()`: Truncates a number to a specified number of decimal places.

2. **String Functions**: Perform operations on a string and return a string value.
    - `CONCAT()`: Concatenates two or more strings.  
      **Syntax:**  
      ```sql
      SELECT CONCAT(column1, column2) FROM table_name;
      ```
    - `LENGTH()`: Returns the length of a string.  
      **Syntax:**  
      ```sql
      SELECT LENGTH(column_name) FROM table_name;
      ```
    - `LOWER()`: Converts a string to lowercase.  
      **Syntax:**  
      ```sql
      SELECT LOWER(column_name) FROM table_name;
      ```
    - `UPPER()`: Converts a string to uppercase.  
      **Syntax:**  
      ```sql
      SELECT UPPER(column_name) FROM table_name;
      ```
    - `REPLACE()`: Replaces a substring within a string with another substring.  
      **Syntax:**  
      ```sql
      SELECT REPLACE(column_name, 'old_string', 'new_string') FROM table_name;
      ```
    - `SUBSTRING()`: Extracts a substring from a string.  
      **Syntax:**  
      ```sql
      SELECT SUBSTRING(column_name, start_position, length) FROM table_name;
      ```

3. **Date Functions**: Date functions in MySQL are used to extract and format date and time values in various formats.
    - `CURDATE()`: Returns the current date.
        ```sql 
        SELECT CURDATE();
        ```
    - `CURTIME()`: Returns the current time.
       ```sql 
       SELECT CURTIME(); 
       ```
    - `NOW()`: Returns the current date and time.
    - `DATE()`: Extracts the date part of a date or datetime expression.
    - `TIME()`: Extracts the time part of a date or datetime expression.
    - `DAYNAME()`: Returns the name of the weekday.
    - `MONTHNAME()`: Returns the name of the month.
    - `DAY()`: Returns the day of the month.
    - `MONTH()`: Returns the month of the year.
    - `YEAR()`: Returns the year.
    - `HOUR()`: Returns the hour.
    - `MINUTE()`: Returns the minute.
    - `SECOND()`: Returns the second.
    - `TIMESTAMP()`: Converts a date or datetime expression to a timestamp.
4. **Control Flow Functions**
5. **Comparison Functions**

## Advanced MySQL Topics
### Functions and Trigers