## Database Structures and Management with MySQL

### Module 3
- Functions in MySQL
1. Numeric functions
    - Aggrigate functions: Perform a calculation on a set of values and return a single value.
        - `AVG()`: Returns the average value of a numeric column.
                Syntax: SELECT AVG(column_name) FROM table_name;
        - `COUNT()`: Returns the number of rows that matches a specified criteria.
        - `MAX()`
        - `MIN()`
        - `SUM()`
    - `Mathematical functions`: Perform a mathematical operation and return a single value.
        - `ABS()`: Returns the absolute value of a number.
          Syntax: 
        - `CEIL()`: Returns the smallest integer value that is greater than or equal to a number.
        - `FLOOR()`: Returns the largest integer value that is less than or equal to a number.
        - `ROUND()`: Rounds a number to a specified number of decimal places.
          Syntax: SELECT column_name, ROUND(column_name, decimal_places) FROM table_name;
        - `MOD()`: Returns the remainder of a division.
            Syntax: SELECT column_name, MOD(column/value, divided by value) FROM table_name;
        - `RAND()`
        - `TRUNCATE()`



2. String functions: Perform an operation on a string and return a string value.
    - `CONCAT()`: Concatenates two or more strings.
        Syntax: SELECT CONCAT(column1, column2) FROM table_name;
    - `LENGTH()`: Returns the length of a string.
        Syntax: SELECT LENGTH(column_name) FROM table_name;
    - `LOWER()`: Converts a string to lower-case.
        Syntax: SELECT LOWER(column_name) FROM table_name;
    - `UPPER()`: Converts a string to upper-case.
        Syntax: SELECT UPPER(column_name) FROM table_name;
    - `REPLACE()`: Replaces a substring within a string with another substring.
        Syntax: SELECT REPLACE(column_name, old_string, new_string) FROM table_name;
    - `SUBSTRING()`: Extracts a substring from a string.
        Syntax: SELECT SUBSTRING (column_name, start_position, length) FROM table_name;
3. Date functions
4. Control flow functions
5. Comparison functions
