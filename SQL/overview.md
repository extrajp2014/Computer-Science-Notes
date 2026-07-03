## **SQL Command Categories**

---

### **Data Definition Language (DDL)**

| Command | Description |
|---------|-------------|
| **CREATE TABLE** | Creates a new table with specified columns and constraints |
| **ALTER TABLE** | Modifies an existing table (add/drop/alter columns, add/drop constraints) |
| **DROP TABLE** | Removes a table and its data permanently |
| **TRUNCATE TABLE** | Removes all rows from a table without logging individual row deletions |
| **RENAME TABLE** | Renames an existing table |
| **COMMENT ON TABLE** | Adds a comment to a table |
| **CREATE INDEX** | Creates an index on one or more columns of a table |
| **DROP INDEX** | Removes an index from a table |
| **REINDEX** | Rebuilds an index |
| **CREATE UNIQUE INDEX** | Creates a unique index that enforces uniqueness on the indexed columns |
| **CREATE FULLTEXT INDEX** | Creates a full-text index for text search |
| **CREATE SPATIAL INDEX** | Creates a spatial index for geographic data |
| **CREATE VIEW** | Creates a virtual table based on a SQL query |
| **ALTER VIEW** | Modifies an existing view |
| **DROP VIEW** | Removes a view |
| **CREATE MATERIALIZED VIEW** | Creates a materialized view that stores query results physically |
| **DROP MATERIALIZED VIEW** | Removes a materialized view |
| **REFRESH MATERIALIZED VIEW** | Updates the data in a materialized view |
| **CREATE SCHEMA** | Creates a new schema (namespace) |
| **ALTER SCHEMA** | Modifies an existing schema |
| **DROP SCHEMA** | Removes a schema |
| **RENAME SCHEMA** | Renames an existing schema |
| **CREATE DATABASE** | Creates a new database |
| **ALTER DATABASE** | Modifies database properties |
| **DROP DATABASE** | Removes a database and all its objects |
| **RENAME DATABASE** | Renames an existing database |
| **ADD COLUMN** | Adds a new column to an existing table |
| **DROP COLUMN** | Removes a column from a table |
| **ALTER COLUMN** | Modifies the data type or constraints of a column |
| **RENAME COLUMN** | Renames a column in a table |
| **MODIFY COLUMN** | Changes the definition of a column |
| **CHANGE COLUMN** | Changes the name and definition of a column |
| **ADD CONSTRAINT** | Adds a constraint to a table |
| **DROP CONSTRAINT** | Removes a constraint from a table |
| **ALTER CONSTRAINT** | Modifies a constraint |
| **ENABLE CONSTRAINT** | Enables a disabled constraint |
| **DISABLE CONSTRAINT** | Disables a constraint |
| **CREATE SEQUENCE** | Creates a sequence generator |
| **ALTER SEQUENCE** | Modifies a sequence |
| **DROP SEQUENCE** | Removes a sequence |
| **SET SEQUENCE** | Sets the current value of a sequence |
| **CREATE SYNONYM** | Creates an alias for a table, view, or other object |
| **DROP SYNONYM** | Removes a synonym |
| **CREATE TYPE** | Creates a new user-defined data type |
| **DROP TYPE** | Removes a user-defined data type |
| **ALTER TYPE** | Modifies a user-defined data type |
| **CREATE PROCEDURE** | Creates a stored procedure |
| **ALTER PROCEDURE** | Modifies an existing stored procedure |
| **DROP PROCEDURE** | Removes a stored procedure |
| **CREATE FUNCTION** | Creates a user-defined function |
| **ALTER FUNCTION** | Modifies an existing user-defined function |
| **DROP FUNCTION** | Removes a user-defined function |
| **CREATE PACKAGE** | Creates a package of related procedures and functions |
| **DROP PACKAGE** | Removes a package |
| **CREATE TRIGGER** | Creates a trigger that executes in response to specified events |
| **ALTER TRIGGER** | Modifies an existing trigger |
| **DROP TRIGGER** | Removes a trigger |
| **ENABLE TRIGGER** | Enables a disabled trigger |
| **DISABLE TRIGGER** | Disables a trigger |
| **CREATE EVENT** | Creates a scheduled event |
| **ALTER EVENT** | Modifies an existing event |
| **DROP EVENT** | Removes an event |
| **PARTITION BY** | Defines how a table is partitioned |
| **CREATE TABLESPACE** | Creates a new tablespace for storing data |
| **ALTER TABLESPACE** | Modifies an existing tablespace |
| **DROP TABLESPACE** | Removes a tablespace |
| **CREATE EXTENSION** | Installs an extension in the database |
| **ALTER EXTENSION** | Modifies an installed extension |
| **DROP EXTENSION** | Removes an extension |

---

### **Data Manipulation Language (DML)**

| Command | Description |
|---------|-------------|
| **SELECT** | Retrieves data from one or more tables |
| **SELECT INTO** | Copies data from a query into a new table |
| **INSERT** | Adds new rows to a table |
| **INSERT INTO ... VALUES** | Inserts one or more rows with specified values |
| **INSERT INTO ... SELECT** | Inserts rows from a query result |
| **INSERT ALL** | Inserts multiple rows in a single statement |
| **REPLACE** | Replaces existing rows or inserts new rows |
| **COPY** | Copies data between tables or files |
| **BULK INSERT** | Inserts multiple rows from a file |
| **UPDATE** | Modifies existing rows in a table |
| **MERGE** | Performs INSERT, UPDATE, or DELETE operations conditionally (UPSERT) |
| **ON DUPLICATE KEY UPDATE** | Updates existing rows if a duplicate key is found during INSERT |
| **DELETE** | Removes rows from a table |
| **TRUNCATE** | Removes all rows from a table without logging individual row deletions |
| **LOAD DATA INFILE** | Loads data from a file into a table |
| **SELECT INTO OUTFILE** | Writes query results to a file |
| **COPY FROM** | Copies data from a file into a table |
| **COPY TO** | Copies data from a table to a file |
| **EXPORT** | Exports data from a table to a file |
| **IMPORT** | Imports data from a file into a table |

---

### **Data Control Language (DCL)**

| Command | Description |
|---------|-------------|
| **GRANT** | Grants privileges to users or roles |
| **REVOKE** | Revokes previously granted privileges |
| **DENY** | Explicitly denies privileges to users or roles |
| **GRANT OPTION FOR** | Allows a user to grant privileges to other users |

---

### **Transaction Control Language (TCL)**

| Command | Description |
|---------|-------------|
| **BEGIN TRANSACTION** | Starts a new transaction |
| **START TRANSACTION** | Starts a new transaction (synonym for BEGIN) |
| **COMMIT** | Commits the current transaction, making changes permanent |
| **ROLLBACK** | Rolls back the current transaction, undoing all changes |
| **SAVEPOINT** | Creates a savepoint within the current transaction |
| **RELEASE SAVEPOINT** | Removes a savepoint without rolling back |
| **ROLLBACK TO SAVEPOINT** | Rolls back to a specified savepoint |
| **SET TRANSACTION** | Sets transaction properties (isolation level, access mode) |
| **SET AUTOCOMMIT** | Enables or disables autocommit mode |
| **SET SESSION CHARACTERISTICS** | Sets session-level transaction characteristics |

---

### **Data Query Language (DQL)**

| Command | Description |
|---------|-------------|
| **SELECT** | Retrieves data from one or more tables |
| **WITH** | Defines a Common Table Expression (CTE) |
| **WITH RECURSIVE** | Defines a recursive Common Table Expression |

---

---
---
## **SQL Clauses**

---

### **SELECT Clauses**

| Clause | Description |
|--------|-------------|
| **FROM** | Specifies the tables to query and how they are joined |
| **WHERE** | Filters rows based on specified conditions |
| **GROUP BY** | Groups rows by specified columns for aggregate functions |
| **HAVING** | Filters groups created by GROUP BY |
| **ORDER BY** | Sorts the result set by specified columns |
| **LIMIT** | Limits the number of rows returned |
| **OFFSET** | Skips a specified number of rows before returning results |
| **FETCH FIRST n ROWS ONLY** | Returns only the first n rows of the result set |
| **FETCH NEXT n ROWS ONLY** | Returns the next n rows after the first set |
| **FOR UPDATE** | Locks the selected rows for update |
| **LOCK IN SHARE MODE** | Locks the selected rows for shared access |

---

### **JOIN Clauses**

| Clause | Description |
|--------|-------------|
| **INNER JOIN** | Returns rows when there is a match in both tables |
| **LEFT JOIN / LEFT OUTER JOIN** | Returns all rows from the left table, and matched rows from the right table (NULL if no match) |
| **RIGHT JOIN / RIGHT OUTER JOIN** | Returns all rows from the right table, and matched rows from the left table (NULL if no match) |
| **FULL JOIN / FULL OUTER JOIN** | Returns all rows when there is a match in either left or right table |
| **CROSS JOIN** | Returns the Cartesian product of both tables |
| **NATURAL JOIN** | Joins tables on columns with the same name |
| **SELF JOIN** | Joins a table to itself |
| **LATERAL JOIN** | Allows a subquery in the FROM clause to reference columns from preceding tables |
| **CROSS LATERAL JOIN** | Cross join with LATERAL subquery |
| **LEFT LATERAL JOIN** | Left join with LATERAL subquery |
| **RIGHT LATERAL JOIN** | Right join with LATERAL subquery |

---

### **Subquery Clauses**

| Clause | Description |
|--------|-------------|
| **EXISTS** | Tests for the existence of rows in a subquery |
| **NOT EXISTS** | Tests for the non-existence of rows in a subquery |
| **IN** | Tests if a value is contained in the results of a subquery |
| **NOT IN** | Tests if a value is not contained in the results of a subquery |
| **ANY** | Tests if a value satisfies any condition in a subquery |
| **ALL** | Tests if a value satisfies all conditions in a subquery |
| **SOME** | Synonym for ANY |

---
### **Set Operation Clauses**

| Clause | Description |
|--------|-------------|
| **UNION** | Combines the result sets of two or more SELECT statements (removes duplicates) |
| **UNION ALL** | Combines the result sets of two or more SELECT statements (includes duplicates) |
| **INTERSECT** | Returns only rows that appear in both result sets |
| **EXCEPT** | Returns rows from the first query that are not in the second query |
| **MINUS** | Synonym for EXCEPT (Oracle, PostgreSQL) |
| **CORRESPONDING** | Matches columns by name in set operations |

---
### **Other Clauses**

| Clause | Description |
|--------|-------------|
| **USING** | Specifies columns to join on when tables have columns with the same name |
| **ON** | Specifies the join condition for explicit joins |
| **PARTITION BY** | Defines partitions for window functions |
| **WINDOW** | Defines a named window specification for reuse |
| **OVER** | Defines the window for window functions |
| **FILTER** | Filters the rows used in an aggregate function |
| **QUALIFY** | Filters the results of window functions |

---
### **Window Function Clauses**

| Clause | Description |
|--------|-------------|
| **OVER** | Defines the window for window functions |
| **PARTITION BY** | Divides the result set into partitions |
| **ORDER BY** | Orders rows within each partition |
| **ROWS BETWEEN** | Defines the frame for window functions using row counts |
| **RANGE BETWEEN** | Defines the frame for window functions using value ranges |
| **UNBOUNDED PRECEDING** | Specifies the start of the frame as the first row of the partition |
| **UNBOUNDED FOLLOWING** | Specifies the end of the frame as the last row of the partition |
| **CURRENT ROW** | Specifies the current row as the start or end of the frame |
| **n PRECEDING** | Specifies the start of the frame as n rows before the current row |
| **n FOLLOWING** | Specifies the end of the frame as n rows after the current row |

---
### **Table Clauses**

| Clause | Description |
|--------|-------------|
| **TABLE** | Specifies a table or derived table in the FROM clause |
| **TABLESAMPLE** | Returns a random sample of rows from a table |
| **SYSTEM** | Uses a system-defined sampling method |
| **BERNOULLI** | Uses Bernoulli sampling (each row is selected with equal probability) |
| **RESERVOIR** | Uses reservoir sampling (random sample of n rows or n percent) |
| **BUCKET n OUT OF m** | Samples from n out of m buckets |
| **SAMPLE n ROWS** | Returns a sample of n rows |
| **SAMPLE n PERCENT** | Returns a sample of n percent of rows |

---
### **INSERT Clauses**

| Clause | Description |
|--------|-------------|
| **INTO** | Specifies the target table for an INSERT statement |
| **VALUES** | Specifies the values to insert |
| **DEFAULT VALUES** | Inserts a row with default values for all columns |
| **SET** | Specifies column-value pairs for an INSERT or UPDATE statement |
| **ON DUPLICATE KEY UPDATE** | Updates existing rows if a duplicate key is found during INSERT |
| **ON CONFLICT** | Specifies what to do when a conflict occurs (PostgreSQL) |
| **DO NOTHING** | Does nothing if a conflict occurs |
| **DO UPDATE SET** | Updates the row if a conflict occurs |

---
### **UPDATE Clauses**

| Clause | Description |
|--------|-------------|
| **SET** | Specifies the columns to update and their new values |
| **WHERE** | Filters the rows to update |
| **FROM** | Specifies additional tables for the update (PostgreSQL, SQL Server) |
| **RETURNING** | Returns the rows affected by the update |

---
### **DELETE Clauses**

| Clause | Description |
|--------|-------------|
| **FROM** | Specifies the table to delete rows from |
| **WHERE** | Filters the rows to delete |
| **RETURNING** | Returns the rows affected by the delete |

---
---
---
## **SQL Functions**

---
### **Aggregate Functions**

| Function | Description |
|----------|-------------|
| **COUNT** | Counts the number of rows or non-NULL values |
| **SUM** | Calculates the sum of values |
| **AVG** | Calculates the average of values |
| **MIN** | Returns the minimum value |
| **MAX** | Returns the maximum value |
| **STDDEV** | Calculates the standard deviation of values |
| **STDDEV_POP** | Calculates the population standard deviation |
| **STDDEV_SAMP** | Calculates the sample standard deviation |
| **VARIANCE** | Calculates the variance of values |
| **VAR_POP** | Calculates the population variance |
| **VAR_SAMP** | Calculates the sample variance |
| **MEDIAN** | Calculates the median value |
| **FIRST_VALUE** | Returns the first value in an ordered set |
| **LAST_VALUE** | Returns the last value in an ordered set |
| **NTH_VALUE** | Returns the nth value in an ordered set |
| **STRING_AGG** | Concatenates values from multiple rows into a single string |
| **LISTAGG** | Oracle's version of STRING_AGG |
| **ARRAY_AGG** | Aggregates values into an array |
| **JSON_AGG** | Aggregates values into a JSON array |
| **JSON_OBJECTAGG** | Aggregates key-value pairs into a JSON object |
| **BIT_AND** | Performs a bitwise AND on all values |
| **BIT_OR** | Performs a bitwise OR on all values |
| **BIT_XOR** | Performs a bitwise XOR on all values |
| **PERCENTILE_CONT** | Calculates a continuous percentile |
| **PERCENTILE_DISC** | Calculates a discrete percentile |
| **APPROX_COUNT_DISTINCT** | Estimates the count of distinct values |
| **COLLECT** | Collects all values into a nested table (Oracle) |
| **INTERSECTION** | Returns the intersection of all values (Oracle) |
| **UNION_AGG** | Returns the union of all values (Oracle) |

---
---
### **Window Functions**

| Function | Description |
|----------|-------------|
| **ROW_NUMBER** | Assigns a unique sequential integer to rows within a partition |
| **RANK** | Assigns a rank to each row within a partition (gaps in ranking) |
| **DENSE_RANK** | Assigns a rank to each row within a partition (no gaps in ranking) |
| **PERCENT_RANK** | Calculates the relative rank of each row within a partition |
| **CUME_DIST** | Calculates the cumulative distribution of a value within a partition |
| **NTILE** | Divides the rows in a partition into approximately equal groups |
| **LEAD** | Accesses data from a subsequent row in the same result set |
| **LAG** | Accesses data from a previous row in the same result set |
| **FIRST_VALUE** | Returns the first value in an ordered set of values |
| **LAST_VALUE** | Returns the last value in an ordered set of values |
| **NTH_VALUE** | Returns the nth value in an ordered set of values |
| **SUM OVER** | Calculates the sum of values over a window |
| **AVG OVER** | Calculates the average of values over a window |
| **COUNT OVER** | Counts the number of rows over a window |
| **MIN OVER** | Returns the minimum value over a window |
| **MAX OVER** | Returns the maximum value over a window |
| **STDDEV OVER** | Calculates the standard deviation over a window |
| **VARIANCE OVER** | Calculates the variance over a window |

---
---
### **Scalar Functions**

---
#### **String Functions**

| Function | Description |
|----------|-------------|
| **UPPER** | Converts a string to uppercase |
| **LOWER** | Converts a string to lowercase |
| **INITCAP** | Converts the first letter of each word to uppercase |
| **TO_UPPER** | Synonym for UPPER |
| **TO_LOWER** | Synonym for LOWER |
| **CONCAT** | Concatenates two or more strings |
| **CONCAT_WS** | Concatenates strings with a specified separator |
| **SUBSTRING / SUBSTR** | Extracts a substring from a string |
| **LEFT** | Extracts the leftmost n characters from a string |
| **RIGHT** | Extracts the rightmost n characters from a string |
| **MID** | Extracts a substring starting at a specified position |
| **REVERSE** | Reverses a string |
| **REPEAT** | Repeats a string a specified number of times |
| **SPACE** | Returns a string of n spaces |
| **LPAD** | Pads a string on the left with a specified character |
| **RPAD** | Pads a string on the right with a specified character |
| **LTRIM** | Removes leading characters from a string |
| **RTRIM** | Removes trailing characters from a string |
| **TRIM** | Removes leading and trailing characters from a string |
| **REGEXP_REPLACE** | Replaces substrings matching a regular expression |
| **REGEXP_SUBSTR** | Extracts a substring matching a regular expression |
| **REGEXP_INSTR** | Returns the position of a substring matching a regular expression |
| **SOUNDEX** | Returns a phonetic representation of a string |
| **DIFFERENCE** | Compares the SOUNDEX values of two strings |
| **STR_CMP** | Compares two strings |
| **LOCATE** | Returns the position of a substring within a string |
| **POSITION** | Returns the position of a substring within a string |
| **INSTR** | Returns the position of a substring within a string |
| **CHARINDEX** | Returns the position of a substring within a string |
| **PATINDEX** | Returns the position of a pattern within a string |
| **EXTRACT** | Extracts a substring using a regular expression |
| **SPLIT_PART** | Splits a string into parts based on a delimiter |
| **PARSE_URL** | Parses a URL and extracts components |
| **PARSE_JSON** | Parses a JSON string |
| **FORMAT** | Formats a value as a string with a specified format |
| **TO_CHAR** | Converts a value to a string with a specified format |
| **TO_VARCHAR** | Synonym for TO_CHAR |
| **PRINTF** | Formats a string using printf-style formatting |
| **BIN_TO_TEXT** | Converts binary data to a text representation |
| **HEX_TO_TEXT** | Converts hexadecimal data to a text representation |

---
#### **String Information Functions**

| Function | Description |
|----------|-------------|
| **LENGTH** | Returns the length of a string in bytes |
| **CHAR_LENGTH** | Returns the length of a string in characters |
| **OCTET_LENGTH** | Returns the length of a string in bytes (synonym for LENGTH) |
| **BIT_LENGTH** | Returns the length of a string in bits |
| **ASCII** | Returns the ASCII code of the first character in a string |
| **CHAR** | Returns the character corresponding to an ASCII code |
| **UNICODE** | Returns the Unicode code point of the first character in a string |
| **NCHAR** | Returns the character corresponding to a Unicode code point |

---
#### **String Comparison Functions**

| Function | Description |
|----------|-------------|
| **SOUNDEX** | Returns a phonetic representation of a string |
| **DIFFERENCE** | Compares the SOUNDEX values of two strings |
| **STR_CMP** | Compares two strings lexicographically |
| **LOCATE** | Returns the position of a substring within a string |
| **POSITION** | Returns the position of a substring within a string |

---
---
#### **Numeric Functions**

| Function | Description |
|----------|-------------|
| **ABS** | Returns the absolute value of a number |
| **SIGN** | Returns the sign of a number (-1, 0, or 1) |
| **CEIL / CEILING** | Returns the smallest integer greater than or equal to a number |
| **FLOOR** | Returns the largest integer less than or equal to a number |
| **ROUND** | Rounds a number to a specified number of decimal places |
| **TRUNC / TRUNCATE** | Truncates a number to a specified number of decimal places |
| **MOD** | Returns the remainder of a division operation |
| **POWER / POW** | Raises a number to the power of another number |
| **EXP** | Returns e raised to the power of a number |
| **LN / LOG** | Returns the natural logarithm of a number |
| **LOG10** | Returns the base-10 logarithm of a number |
| **LOG2** | Returns the base-2 logarithm of a number |
| **SQRT** | Returns the square root of a number |
| **CBRT** | Returns the cube root of a number |
| **DIV** | Performs integer division |
| **GREATEST** | Returns the largest value from a list of values |
| **LEAST** | Returns the smallest value from a list of values |

---
#### **Trigonometric Functions**

| Function | Description |
|----------|-------------|
| **SIN** | Returns the sine of an angle in radians |
| **COS** | Returns the cosine of an angle in radians |
| **TAN** | Returns the tangent of an angle in radians |
| **ASIN** | Returns the arcsine of a value in radians |
| **ACOS** | Returns the arccosine of a value in radians |
| **ATAN** | Returns the arctangent of a value in radians |
| **ATAN2** | Returns the arctangent of y/x in radians |
| **COT** | Returns the cotangent of an angle in radians |
| **SEC** | Returns the secant of an angle in radians |
| **CSC** | Returns the cosecant of an angle in radians |
| **SINH** | Returns the hyperbolic sine of a value |
| **COSH** | Returns the hyperbolic cosine of a value |
| **TANH** | Returns the hyperbolic tangent of a value |
| **ASINH** | Returns the inverse hyperbolic sine of a value |
| **ACOSH** | Returns the inverse hyperbolic cosine of a value |
| **ATANH** | Returns the inverse hyperbolic tangent of a value |

---
#### **Angle Conversion Functions**

| Function | Description |
|----------|-------------|
| **DEGREES** | Converts radians to degrees |
| **RADIANS** | Converts degrees to radians |
| **PI** | Returns the value of pi (3.14159...) |

---
#### **Random Number Functions**

| Function | Description |
|----------|-------------|
| **RAND** | Returns a random float between 0 and 1 |
| **RANDOM** | Returns a random float between 0 and 1 |
| **RANDOMBLOB** | Returns a random blob of a specified length |
| **RANDOMTEXT** | Returns a random text string of a specified length |

---
#### **Bitwise Functions**

| Function | Description |
|----------|-------------|
| **BIT_AND** | Performs a bitwise AND on all values in a group |
| **BIT_OR** | Performs a bitwise OR on all values in a group |
| **BIT_XOR** | Performs a bitwise XOR on all values in a group |
| **BIT_NOT** | Performs a bitwise NOT on a value |
| **BIT_COUNT** | Counts the number of bits set to 1 in a value |
| **BIT_LENGTH** | Returns the number of bits in a value |
| **BIT_POSITION** | Returns the position of the first bit set to 1 in a value |
| **BIT_TO_NUM** | Converts a bit string to a number |
| **NUM_TO_BIT** | Converts a number to a bit string |

---
---
#### **Date and Time Functions**

| Function | Description |
|----------|-------------|
| **CURRENT_DATE** | Returns the current date |
| **CURRENT_TIME** | Returns the current time |
| **CURRENT_TIMESTAMP** | Returns the current date and time |
| **LOCALTIME** | Returns the current local date and time |
| **LOCALTIMESTAMP** | Returns the current local date and time |
| **NOW** | Returns the current date and time |
| **SYSDATE** | Returns the current date and time (Oracle, MySQL) |
| **CURRENT_TIMEZONE** | Returns the current time zone |
| **LOCALTIMEZONE** | Returns the local time zone |
| **EXTRACT** | Extracts a part (year, month, day, etc.) from a date or timestamp |
| **DATE_PART** | Returns a part (year, month, day, etc.) from a date or timestamp |
| **DATE_TRUNC** | Truncates a date or timestamp to a specified precision |
| **DATEADD / ADD_MONTHS / ADD_DAYS / ADD_HOURS** | Adds a time interval to a date or timestamp |
| **DATEDIFF / DATE_DIFF** | Returns the difference between two dates |
| **DATE_FORMAT** | Formats a date or timestamp as a string |
| **TO_CHAR** | Converts a date, timestamp, or number to a string |
| **TO_DATE** | Converts a string to a date |
| **TO_TIMESTAMP** | Converts a string to a timestamp |
| **MAKEDATE** | Creates a date from year, month, and day values |
| **MAKETIME** | Creates a time from hour, minute, and second values |
| **MAKETIMESTAMP** | Creates a timestamp from date and time components |
| **YEAR** | Returns the year part of a date or timestamp |
| **MONTH** | Returns the month part of a date or timestamp |
| **DAY** | Returns the day part of a date or timestamp |
| **HOUR** | Returns the hour part of a time or timestamp |
| **MINUTE** | Returns the minute part of a time or timestamp |
| **SECOND** | Returns the second part of a time or timestamp |
| **MILLISECOND** | Returns the millisecond part of a time or timestamp |
| **MICROSECOND** | Returns the microsecond part of a time or timestamp |
| **QUARTER** | Returns the quarter (1-4) of a date |
| **WEEK** | Returns the week of the year |
| **DAYOFWEEK** | Returns the day of the week (1-7) |
| **DAYOFYEAR** | Returns the day of the year (1-366) |
| **DAYOFMONTH** | Returns the day of the month (1-31) |
| **WEEKDAY** | Returns the day of the week (0-6) |
| **ISODOW** | Returns the ISO day of the week (1-7, Monday=1) |
| **DOW** | Returns the day of the week (0-6, Sunday=0) |
| **LAST_DAY** | Returns the last day of the month |
| **NEXT_DAY** | Returns the first specified day of the week after a given date |
| **AGE** | Calculates the difference between two timestamps |

---
#### **Date/Time Arithmetic Functions**

| Function | Description |
|----------|-------------|
| **INTERVAL** | Creates an interval value |
| **DATETIME** | Creates a datetime value |
| **TIMESTAMPADD** | Adds an interval to a timestamp |
| **TIMESTAMPDIFF** | Returns the difference between two timestamps as an interval |

---
#### **Date/Time Formatting Functions**

| Function | Description |
|----------|-------------|
| **STRFTIME** | Formats a date or timestamp as a string using format specifiers |
| **STRPTIME** | Parses a string into a date or timestamp using format specifiers |
| **FORMATDATETIME** | Formats a date or timestamp as a string |
| **FORMATTIMESTAMP** | Formats a timestamp as a string |

---
#### **Time Zone Functions**

| Function | Description |
|----------|-------------|
| **CONVERT_TZ** | Converts a timestamp from one time zone to another |
| **AT TIME ZONE** | Converts a timestamp to a specified time zone |
| **UTC_TIMESTAMP** | Returns the current UTC timestamp |
| **GMT_TIMESTAMP** | Returns the current GMT timestamp |

---
---
#### **Type Conversion Functions**

| Function | Description |
|----------|-------------|
| **CAST** | Converts a value from one data type to another |
| **CONVERT** | Converts a value from one data type or character set to another |
| **TRY_CAST** | Attempts to convert a value and returns NULL if the conversion fails |
| **TRY_CONVERT** | Attempts to convert a value and returns NULL if the conversion fails |
| **SAFE_CAST** | Attempts to convert a value and returns NULL if the conversion fails |
| **TO_NUMBER** | Converts a string to a number |
| **TO_DATE** | Converts a string to a date |
| **TO_TIMESTAMP** | Converts a string to a timestamp |
| **TO_CHAR** | Converts a date, timestamp, or number to a string |
| **TO_VARCHAR** | Converts a value to a string |
| **TO_BLOB** | Converts a value to a binary large object |
| **TO_CLOB** | Converts a value to a character large object |

---
---
#### **JSON Functions**

| Function | Description |
|----------|-------------|
| **JSON_VALUE** | Extracts a scalar value from a JSON string |
| **JSON_QUERY** | Extracts an object or array from a JSON string |
| **JSON_MODIFY** | Modifies a JSON string |
| **JSON_ARRAY** | Creates a JSON array from values |
| **JSON_ARRAYAGG** | Aggregates values into a JSON array |
| **JSON_OBJECT** | Creates a JSON object from key-value pairs |
| **JSON_OBJECTAGG** | Aggregates key-value pairs into a JSON object |
| **JSON_TABLE** | Converts JSON data into a relational table |
| **JSON_CONTAINS** | Checks if a JSON string contains a specified path |
| **JSON_CONTAINS_PATH** | Checks if a JSON string contains a specified path |
| **JSON_EXTRACT** | Extracts a value from a JSON string |
| **JSON_KEYS** | Returns the keys of a JSON object |
| **JSON_LENGTH** | Returns the length of a JSON array or the number of keys in a JSON object |
| **JSON_TYPE** | Returns the type of a JSON value |
| **JSON_VALID** | Checks if a string is valid JSON |
| **JSON_PRETTY** | Formats a JSON string with indentation |
| **JSON_STORAGE_SIZE** | Returns the storage size of a JSON document |

---
---
#### **XML Functions**

| Function | Description |
|----------|-------------|
| **XMLAGG** | Aggregates values into an XML document |
| **XMLCONCAT** | Concatenates XML values |
| **XMLELEMENT** | Creates an XML element |
| **XMLFOREST** | Creates an XML forest (multiple elements) |
| **XMLPARSE** | Parses a string into an XML value |
| **XMLPI** | Creates an XML processing instruction |
| **XMLROOT** | Creates an XML root element |
| **XMLSERIALIZE** | Serializes an XML value to a string |
| **XMLTABLE** | Converts XML data into a relational table |
| **XMLCAST** | Casts a value to an XML type |
| **XMLTYPE** | Creates an XML type value |

---
---
#### **Other Scalar Functions**

| Function | Description |
|----------|-------------|
| **COALESCE** | Returns the first non-NULL value from a list of values |
| **NULLIF** | Returns NULL if two values are equal, otherwise returns the first value |
| **ISNULL** | Returns the first argument if it is not NULL, otherwise returns the second argument |
| **IFNULL** | Returns the first argument if it is not NULL, otherwise returns the second argument |
| **NVL** | Returns the first argument if it is not NULL, otherwise returns the second argument |
| **NVL2** | Returns the second argument if the first argument is not NULL, otherwise returns the third argument |
| **DECODE** | Oracle-specific function for conditional logic |
| **CASE** | Provides conditional logic |
| **IIF** | Returns one value if a condition is true, another value if false |
| **GREATEST** | Returns the largest value from a list of values |
| **LEAST** | Returns the smallest value from a list of values |
| **INET_ATON** | Converts an IPv4 address from dotted-quad notation to an integer |
| **INET_NTOA** | Converts an integer to an IPv4 address in dotted-quad notation |
| **INET_PTON** | Converts an IP address from text to binary |
| **INET_NTOP** | Converts an IP address from binary to text |
| **UUID** | Generates a universally unique identifier |
| **UUID_TO_BIN** | Converts a UUID string to binary |
| **BIN_TO_UUID** | Converts binary UUID data to a string |
| **VERSION** | Returns the version of the database server |
| **DATABASE** | Returns the name of the current database |
| **USER** | Returns the current user name |
| **CURRENT_USER** | Returns the current user name |
| **SESSION_USER** | Returns the current session user name |
| **SYSTEM_USER** | Returns the system user name |
| **CONNECTION_ID** | Returns the connection ID |
| **LAST_INSERT_ID** | Returns the first auto-increment value generated in the current session |
| **ROW_COUNT** | Returns the number of rows affected by the last statement |
| **FOUND_ROWS** | Returns the number of rows found by the last SELECT statement |
| **IDENTITY** | Returns the last identity value generated in the current session |
| **SCOPE_IDENTITY** | Returns the last identity value generated in the current scope |
| **CURRENT_IDENTITY** | Returns the last identity value generated in the current session for a specified table |

---
---
---
## **SQL Operators**

---
### **Arithmetic Operators**

| Operator | Description |
|----------|-------------|
| **+** | Addition |
| **- ** | Subtraction |
| *** | Multiplication |
| **/** | Division |
| **%** | Modulo (remainder) |
| **DIV** | Integer division |
| **MOD** | Modulo (synonym for %) |

---
### **Comparison Operators**

| Operator | Description |
|----------|-------------|
| **=** | Equal to |
| **<** | Less than |
| **>** | Greater than |
| **<=** | Less than or equal to |
| **>=** | Greater than or equal to |
| **<>** | Not equal to |
| **!=** | Not equal to |
| **!** | Not equal to (alternative) |
| **IS** | Tests if a value is NULL |
| **IS NOT** | Tests if a value is not NULL |
| **LIKE** | Pattern matching (case-sensitive) |
| **NOT LIKE** | Negation of LIKE |
| **ILIKE** | Pattern matching (case-insensitive, PostgreSQL) |
| **NOT ILIKE** | Negation of ILIKE |
| **SIMILAR TO** | Regular expression pattern matching |
| **NOT SIMILAR TO** | Negation of SIMILAR TO |
| **BETWEEN** | Tests if a value is within a range |
| **NOT BETWEEN** | Tests if a value is not within a range |
| **IN** | Tests if a value is contained in a list or subquery |
| **NOT IN** | Tests if a value is not contained in a list or subquery |
| **EXISTS** | Tests if a subquery returns any rows |
| **NOT EXISTS** | Tests if a subquery returns no rows |
| **ANY** | Tests if a value satisfies any condition in a list or subquery |
| **ALL** | Tests if a value satisfies all conditions in a list or subquery |
| **SOME** | Synonym for ANY |
| **IS DISTINCT FROM** | Tests if two values are different (handles NULLs) |
| **IS NOT DISTINCT FROM** | Tests if two values are the same (handles NULLs) |

---
### **Logical Operators**

| Operator | Description |
|----------|-------------|
| **AND** | Logical AND |
| **OR** | Logical OR |
| **NOT** | Logical NOT |
| **XOR** | Logical XOR (exclusive OR) |

---
### **Bitwise Operators**

| Operator | Description |
|----------|-------------|
| **&** | Bitwise AND |
| **\|** | Bitwise OR |
| **^** | Bitwise XOR |
| **~** | Bitwise NOT |
| **<<** | Bitwise left shift |
| **>>** | Bitwise right shift |
| **>>>` | Bitwise right shift with zero fill (Java, not SQL) |

---
### **Set Operators**

| Operator | Description |
|----------|-------------|
| **UNION** | Combines the result sets of two or more SELECT statements (removes duplicates) |
| **UNION ALL** | Combines the result sets of two or more SELECT statements (includes duplicates) |
| **INTERSECT** | Returns only rows that appear in both result sets |
| **EXCEPT** | Returns rows from the first query that are not in the second query |
| **MINUS** | Synonym for EXCEPT (Oracle, PostgreSQL) |

---
### **String Operators**

| Operator | Description |
|----------|-------------|
| **\|\|** | String concatenation |
| **CONCAT** | String concatenation function |

---
### **JSON Operators**

| Operator | Description |
|----------|-------------|
| **->** | Extracts a JSON object field or array element |
| **->>** | Extracts a JSON object field or array element as text |
| **#>>** | Extracts a nested JSON object field or array element as text (PostgreSQL) |
| **@>** | Contains operator (JSON path contains value) |
| **<@** | Contained by operator |
| **? ** | Contains key operator (JSON object contains key) |
| **?\|** | Contains any key operator (JSON object contains any of the specified keys) |
| **?&** | Contains all keys operator (JSON object contains all of the specified keys) |

---
### **Other Operators**

| Operator | Description |
|----------|-------------|
| **::** | Type cast operator (PostgreSQL) |
| **@>** | Contains operator (PostgreSQL) |
| **<@** | Contained by operator (PostgreSQL) |
| **&&** | Overlaps operator (PostgreSQL) |
| **\~\~** | Regular expression match (PostgreSQL) |
| **!\~\~** | Regular expression does not match (PostgreSQL) |
| **\~\*\ ** | Case-insensitive regular expression match (PostgreSQL) |
| **!\~\*\ ** | Case-insensitive regular expression does not match (PostgreSQL) |

---
---
---
## **SQL Data Types**

---
### **Numeric Types**

| Data Type | Description |
|-----------|-------------|
| **BIT** | Bit-string type |
| **TINYINT** | 1-byte integer (signed: -128 to 127, unsigned: 0 to 255) |
| **SMALLINT** | 2-byte integer (signed: -32,768 to 32,767, unsigned: 0 to 65,535) |
| **INT / INTEGER** | 4-byte integer (signed: -2,147,483,648 to 2,147,483,647, unsigned: 0 to 4,294,967,295) |
| **BIGINT** | 8-byte integer (signed: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807, unsigned: 0 to 18,446,744,073,709,551,615) |
| **SERIAL** | Auto-incrementing 4-byte integer (PostgreSQL) |
| **SMALLSERIAL** | Auto-incrementing 2-byte integer (PostgreSQL) |
| **BIGSERIAL** | Auto-incrementing 8-byte integer (PostgreSQL) |
| **DECIMAL / DEC / NUMERIC** | Fixed-point number with user-specified precision and scale |
| **FLOAT** | Single-precision floating-point number (4 bytes) |
| **REAL** | Single-precision floating-point number (4 bytes, synonym for FLOAT) |
| **DOUBLE** | Double-precision floating-point number (8 bytes) |
| **DOUBLE PRECISION** | Double-precision floating-point number (8 bytes) |
| **HALF_FLOAT** | Half-precision floating-point number (2 bytes) |
| **MONEY** | Currency amount (8 bytes, PostgreSQL) |
| **SMALLMONEY** | Currency amount (4 bytes, SQL Server) |

---
### **Fixed-Point Types**

| Data Type | Description |
|-----------|-------------|
| **DECIMAL** | Fixed-point number with user-specified precision and scale |
| **DEC** | Synonym for DECIMAL |
| **NUMERIC** | Synonym for DECIMAL |
| **FIXED** | Synonym for DECIMAL |

---
### **String Types**

| Data Type | Description |
|-----------|-------------|
| **CHAR / CHARACTER** | Fixed-length character string |
| **VARCHAR / CHARACTER VARYING** | Variable-length character string |
| **NCHAR** | Fixed-length Unicode string |
| **NVARCHAR** | Variable-length Unicode string |
| **NVARCHAR2** | Variable-length Unicode string (Oracle) |
| **TEXT** | Variable-length character string (unlimited length) |
| **CLOB** | Character large object (for storing large text) |
| **NTEXT** | Unicode text (SQL Server) |
| **NCLOB** | Unicode character large object |

---
### **Binary Types**

| Data Type | Description |
|-----------|-------------|
| **BINARY** | Fixed-length binary string |
| **VARBINARY** | Variable-length binary string |
| **BLOB** | Binary large object (for storing large binary data) |
| **LONG VARBINARY** | Variable-length binary string (unlimited length) |
| **BYTEA** | Binary string (PostgreSQL) |

---
### **Date and Time Types**

| Data Type | Description |
|-----------|-------------|
| **DATE** | Date (year, month, day) |
| **TIME** | Time of day (hour, minute, second) |
| **TIME WITH TIME ZONE** | Time of day with time zone |
| **TIME WITHOUT TIME ZONE** | Time of day without time zone |
| **TIMESTAMP** | Date and time (year, month, day, hour, minute, second) |
| **TIMESTAMP WITH TIME ZONE** | Date and time with time zone |
| **TIMESTAMP WITHOUT TIME ZONE** | Date and time without time zone |
| **TIMESTAMPTZ** | Timestamp with time zone (PostgreSQL) |
| **TIMESTAMPLTZ** | Timestamp with local time zone (Oracle) |
| **INTERVAL** | Time interval |
| **DATERANGE** | Range of dates (PostgreSQL) |
| **TSRANGE** | Range of timestamps (PostgreSQL) |
| **TSTZRANGE** | Range of timestamps with time zone (PostgreSQL) |
| **DATETIMETZRANGE** | Range of date and time with time zone (PostgreSQL) |

---
### **Date and Time Components**

| Data Type | Description |
|-----------|-------------|
| **YEAR** | Year (1-4 digits) |
| **MONTH** | Month (1-12) |
| **DAY** | Day of the month (1-31) |
| **HOUR** | Hour (0-23) |
| **MINUTE** | Minute (0-59) |
| **SECOND** | Second (0-59) |

---
### **Boolean Type**

| Data Type | Description |
|-----------|-------------|
| **BOOLEAN / BOOL** | Boolean value (TRUE or FALSE) |

---
### **JSON Types**

| Data Type | Description |
|-----------|-------------|
| **JSON** | JSON document |
| **JSONB** | Binary JSON (PostgreSQL) |

---
### **XML Type**

| Data Type | Description |
|-----------|-------------|
| **XML** | XML document |

---
### **Array Type**

| Data Type | Description |
|-----------|-------------|
| **ARRAY** | Array of values (PostgreSQL) |

---
### **Composite Types**

| Data Type | Description |
|-----------|-------------|
| **COMPOSITE** | Composite type (PostgreSQL) |
| **RECORD** | Record type (PostgreSQL) |
| **ROW** | Row type |

---
### **Range Types**

| Data Type | Description |
|-----------|-------------|
| **INT4RANGE** | Range of 4-byte integers (PostgreSQL) |
| **INT8RANGE** | Range of 8-byte integers (PostgreSQL) |
| **NUMRANGE** | Range of numeric values (PostgreSQL) |
| **DATERANGE** | Range of dates (PostgreSQL) |
| **TSRANGE** | Range of timestamps (PostgreSQL) |
| **TSTZRANGE** | Range of timestamps with time zone (PostgreSQL) |

---
### **Network Address Types**

| Data Type | Description |
|-----------|-------------|
| **INET** | IPv4 or IPv6 address (PostgreSQL) |
| **CIDR** | IPv4 or IPv6 network address (PostgreSQL) |
| **MACADDR** | MAC address (PostgreSQL) |
| **MACADDR8** | EUI-64 MAC address (PostgreSQL) |

---
### **Geometric and Geographic Types**

| Data Type | Description |
|-----------|-------------|
| **POINT** | Geometric point (PostgreSQL) |
| **LINE** | Infinite line (PostgreSQL) |
| **LSEG** | Line segment (PostgreSQL) |
| **BOX** | Rectangular box (PostgreSQL) |
| **PATH** | Geometric path (PostgreSQL) |
| **POLYGON** | Polygon (PostgreSQL) |
| **CIRCLE** | Circle (PostgreSQL) |
| **GEOMETRY** | Geometry type (PostGIS) |
| **GEOGRAPHY** | Geography type (PostGIS) |

---
### **Full-Text Search Types**

| Data Type | Description |
|-----------|-------------|
| **TSVECTOR** | Text search vector (PostgreSQL) |
| **TSQUERY** | Text search query (PostgreSQL) |

---
### **UUID Type**

| Data Type | Description |
|-----------|-------------|
| **UUID** | Universally Unique Identifier |

---
### **Other Special Types**

| Data Type | Description |
|-----------|-------------|
| **OID** | Object identifier (PostgreSQL) |
| **XID** | Transaction identifier (PostgreSQL) |
| **CID** | Command identifier (PostgreSQL) |
| **REGCONFIG** | Text search configuration (PostgreSQL) |
| **REGDICTIONARY** | Text search dictionary (PostgreSQL) |
| **REGNAMESPACE** | Namespace (PostgreSQL) |
| **REGPROCEDURE** | Procedure (PostgreSQL) |
| **REGOPER** | Operator (PostgreSQL) |
| **REGOPERATOR** | Operator (PostgreSQL) |
| **REGROLE** | Role (PostgreSQL) |
| **REGTYPE** | Type (PostgreSQL) |
| **REGTYPEARRAY** | Type array (PostgreSQL) |

---
---
---
## **SQL Constraints**

---
### **Column Constraints**

| Constraint | Description |
|------------|-------------|
| **PRIMARY KEY** | Uniquely identifies each row in a table (cannot contain NULL values) |
| **FOREIGN KEY** | Ensures referential integrity by linking to a primary key in another table |
| **UNIQUE** | Ensures all values in a column are unique (can contain NULL values) |
| **CHECK** | Ensures values in a column satisfy a specified condition |
| **NOT NULL** | Ensures a column cannot contain NULL values |
| **NULL** | Allows a column to contain NULL values (default) |
| **DEFAULT** | Specifies a default value for a column |
| **GENERATED ALWAYS AS** | Specifies a generated column (computed from other columns) |
| **IDENTITY** | Specifies an auto-incrementing column (SQL Server, PostgreSQL) |
| **SEQUENCE** | Specifies a column that uses a sequence for default values |

---
### **Table Constraints**

| Constraint | Description |
|------------|-------------|
| **PRIMARY KEY** | Uniquely identifies each row in a table using one or more columns |
| **FOREIGN KEY** | Ensures referential integrity between tables |
| **UNIQUE** | Ensures all values in one or more columns are unique |
| **CHECK** | Ensures values in one or more columns satisfy a specified condition |
| **EXCLUDE** | Ensures that if any two rows are compared, at least one specified column must differ (PostgreSQL) |

---
### **Foreign Key Actions**

| Action | Description |
|--------|-------------|
| **ON DELETE CASCADE** | Automatically deletes referencing rows when the referenced row is deleted |
| **ON DELETE SET NULL** | Sets the foreign key column to NULL when the referenced row is deleted |
| **ON DELETE SET DEFAULT** | Sets the foreign key column to its default value when the referenced row is deleted |
| **ON DELETE RESTRICT** | Prevents deletion of the referenced row if referencing rows exist |
| **ON DELETE NO ACTION** | Same as RESTRICT (default in most databases) |
| **ON UPDATE CASCADE** | Automatically updates referencing rows when the referenced row is updated |
| **ON UPDATE SET NULL** | Sets the foreign key column to NULL when the referenced row is updated |
| **ON UPDATE SET DEFAULT** | Sets the foreign key column to its default value when the referenced row is updated |
| **ON UPDATE RESTRICT** | Prevents update of the referenced row if referencing rows exist |
| **ON UPDATE NO ACTION** | Same as RESTRICT (default in most databases) |

---
### **Constraint Naming**

| Syntax | Description |
|--------|-------------|
| **CONSTRAINT constraint_name** | Specifies a name for a constraint |

---
---
---
## **SQL Joins**

| Join Type | Description |
|-----------|-------------|
| **INNER JOIN** | Returns rows when there is a match in both tables |
| **LEFT JOIN / LEFT OUTER JOIN** | Returns all rows from the left table, and matched rows from the right table (NULL if no match) |
| **RIGHT JOIN / RIGHT OUTER JOIN** | Returns all rows from the right table, and matched rows from the left table (NULL if no match) |
| **FULL JOIN / FULL OUTER JOIN** | Returns all rows when there is a match in either left or right table |
| **CROSS JOIN** | Returns the Cartesian product of both tables (all possible combinations) |
| **NATURAL JOIN** | Joins tables on columns with the same name |
| **SELF JOIN** | Joins a table to itself |
| **LATERAL JOIN** | Allows a subquery in the FROM clause to reference columns from preceding tables |
| **CROSS LATERAL JOIN** | Cross join with LATERAL subquery |
| **LEFT LATERAL JOIN** | Left join with LATERAL subquery |
| **RIGHT LATERAL JOIN** | Right join with LATERAL subquery |

---
---
---
## **SQL Index Types**

| Index Type | Description |
|------------|-------------|
| **B-TREE** | Balanced tree index (default for most databases) |
| **HASH** | Hash index (fast for equality comparisons) |
| **GIN (Generalized Inverted Index)** | Inverted index for composite values (PostgreSQL) |
| **GIST (Generalized Search Tree)** | Index for geometric data and full-text search (PostgreSQL) |
| **SP-GIST (Space-Partitioned GiST)** | Index for non-balanced data (PostgreSQL) |
| **BRIN (Block Range Index)** | Index for large tables with ordered data (PostgreSQL) |
| **BITMAP** | Bitmap index (Oracle) |
| **FULL TEXT** | Full-text search index |
| **PARTIAL** | Index on a subset of a table |
| **FUNCTION-BASED** | Index on the result of a function or expression |
| **CLUSTERED** | Index that determines the physical order of data (SQL Server) |
| **NONCLUSTERED** | Index that does not affect the physical order of data |
| **UNIQUE** | Index that enforces uniqueness on the indexed columns |
| **NON-UNIQUE** | Index that allows duplicate values |

---
---
---
## **SQL Advanced Features**

---
### **Common Table Expressions (CTEs)**

| Feature | Description |
|---------|-------------|
| **WITH** | Defines a Common Table Expression (CTE) for use in a query |
| **WITH RECURSIVE** | Defines a recursive CTE for hierarchical or graph queries |
| **SEARCH DEPTH FIRST BY** | Specifies depth-first search order for recursive CTEs |
| **SEARCH BREADTH FIRST BY** | Specifies breadth-first search order for recursive CTEs |
| **CYCLE** | Detects cycles in recursive CTEs and handles them |

---
### **PIVOT and UNPIVOT**

| Feature | Description |
|---------|-------------|
| **PIVOT** | Transforms rows into columns (cross-tabulation) |
| **UNPIVOT** | Transforms columns into rows (reverse of PIVOT) |

---
### **Materialized Views**

| Command | Description |
|---------|-------------|
| **CREATE MATERIALIZED VIEW** | Creates a materialized view that stores query results physically |
| **REFRESH MATERIALIZED VIEW** | Updates the data in a materialized view |
| **REFRESH MATERIALIZED VIEW WITH DATA** | Updates the data in a materialized view with data |
| **REFRESH MATERIALIZED VIEW WITH NO DATA** | Updates the data in a materialized view without data |
| **DROP MATERIALIZED VIEW** | Removes a materialized view |

---
### **Partitions**

| Feature | Description |
|---------|-------------|
| **PARTITION BY** | Defines how a table is partitioned |
| **PARTITION BY RANGE** | Partitions a table by ranges of values |
| **PARTITION BY LIST** | Partitions a table by discrete values |
| **PARTITION BY HASH** | Partitions a table by hash values |
| **PARTITION BY COMPOSITE** | Partitions a table using multiple partitioning strategies |
| **SUBPARTITION BY** | Defines subpartitions within partitions |
| **PARTITION FOR** | Specifies the partition for a specific value |
| **PARTITION pn VALUES LESS THAN** | Defines a range partition with an upper bound |
| **PARTITION pn VALUES IN** | Defines a list partition with discrete values |
| **PARTITION pn VALUES DEFAULT** | Defines a default partition for values that do not match other partitions |

---
### **Table Inheritance**

| Feature | Description |
|---------|-------------|
| **INHERITS** | Specifies that a table inherits from another table (PostgreSQL) |

---
### **Table Sampling**

| Feature | Description |
|---------|-------------|
| **TABLESAMPLE SYSTEM(n)** | Returns a system-defined sample of n percent of rows |
| **TABLESAMPLE BERNOULLI(n)** | Returns a Bernoulli sample of n percent of rows |
| **TABLESAMPLE RESERVOIR(n ROWS)** | Returns a reservoir sample of n rows |
| **TABLESAMPLE RESERVOIR(n PERCENT)** | Returns a reservoir sample of n percent of rows |
| **TABLESAMPLE SYSTEM_TIME** | Returns a sample based on system time |
| **TABLESAMPLE BLOCK** | Returns a sample based on data blocks |

---
### **Query Hints**

| Hint | Description |
|------|-------------|
| **/*+ INDEX(table, index) */** | Suggests using a specific index |
| **/*+ FULL(table) */** | Suggests using a full table scan |
| **/*+ LEADING(table1 table2) */** | Suggests the join order |
| **/*+ USE_NL(table) */** | Suggests using a nested loops join |
| **/*+ USE_MERGE(table) */** | Suggests using a merge join |
| **/*+ USE_HASH(table) */** | Suggests using a hash join |
| **/*+ NO_INDEX(table, index) */** | Suggests not using a specific index |
| **/*+ FIRST_ROWS(n) */** | Optimizes for returning the first n rows quickly |
| **/*+ ALL_ROWS */** | Optimizes for returning all rows |

---
---
---
## **SQL Procedural Extensions**

---
### **Variables**

| Statement | Description |
|-----------|-------------|
| **DECLARE** | Declares a variable, cursor, or other objects |
| **SET** | Assigns a value to a variable |
| **SELECT INTO** | Assigns query results to variables |

---
### **Cursors**

| Statement | Description |
|-----------|-------------|
| **DECLARE CURSOR** | Declares a cursor for iterating over query results |
| **OPEN** | Opens a cursor |
| **FETCH** | Retrieves rows from a cursor |
| **CLOSE** | Closes a cursor |
| **DEALLOCATE** | Deallocates a cursor |
| **FETCH FIRST** | Retrieves the first row from a cursor |
| **FETCH NEXT** | Retrieves the next row from a cursor |
| **FETCH PRIOR** | Retrieves the previous row from a cursor |
| **FETCH LAST** | Retrieves the last row from a cursor |
| **FETCH ABSOLUTE** | Retrieves a row at a specified absolute position |
| **FETCH RELATIVE** | Retrieves a row at a specified relative position |
| **FETCH n** | Retrieves n rows from a cursor |
| **FOR** | Specifies the query for a cursor |
| **AS** | Specifies the name of a cursor |
| **OF** | Specifies the row type for a cursor |
| **ISOLATION LEVEL** | Specifies the transaction isolation level for a cursor |

---
### **Stored Procedures**

| Statement | Description |
|-----------|-------------|
| **CREATE PROCEDURE** | Creates a new stored procedure |
| **ALTER PROCEDURE** | Modifies an existing stored procedure |
| **DROP PROCEDURE** | Removes a stored procedure |
| **EXECUTE** | Executes a stored procedure |
| **CALL** | Calls a stored procedure |
| **BEGIN ... END** | Defines a block of statements |
| **IF ... THEN ... ELSE ... END IF** | Conditional execution |
| **CASE ... WHEN ... THEN ... ELSE ... END CASE** | Multi-way conditional |
| **LOOP ... END LOOP** | Infinite loop |
| **WHILE ... DO ... END WHILE** | Conditional loop |
| **REPEAT ... UNTIL ... END REPEAT** | Post-test loop |
| **FOR ... IN ... DO ... END FOR** | Iterates over a query result |
| **CONTINUE** | Skips to the next iteration of a loop |
| **LEAVE** | Exits a loop |
| **ITERATE** | Synonym for CONTINUE |
| **RETURN** | Returns from a procedure or function |
| **SIGNAL** | Raises an error or warning |
| **RESIGNAL** | Re-raises an error or warning |
| **DECLARE ... HANDLER FOR** | Defines an error handler |

---
### **Functions**

| Statement | Description |
|-----------|-------------|
| **CREATE FUNCTION** | Creates a new user-defined function |
| **ALTER FUNCTION** | Modifies an existing user-defined function |
| **DROP FUNCTION** | Removes a user-defined function |
| **RETURNS** | Specifies the return type of a function |
| **LANGUAGE** | Specifies the language of a function (SQL, PLpgSQL, etc.) |
| **SQL** | Specifies that the function is written in SQL |
| **AS** | Specifies the body of a function |
| **BEGIN ATOMIC ... END** | Defines an atomic block in a function |

---
### **Triggers**

| Statement | Description |
|-----------|-------------|
| **CREATE TRIGGER** | Creates a new trigger |
| **ALTER TRIGGER** | Modifies an existing trigger |
| **DROP TRIGGER** | Removes a trigger |
| **BEFORE** | Specifies that the trigger fires before the event |
| **AFTER** | Specifies that the trigger fires after the event |
| **INSTEAD OF** | Specifies that the trigger fires instead of the event |
| **FOR EACH ROW** | Specifies that the trigger fires for each affected row |
| **FOR EACH STATEMENT** | Specifies that the trigger fires once per statement |
| **EXECUTE PROCEDURE** | Specifies the procedure to execute for the trigger |
| **WHEN** | Specifies a condition for the trigger |
| **REFERENCING** | Specifies the old and new values for the trigger |
| **OLD** | Refers to the old values in a trigger |
| **NEW** | Refers to the new values in a trigger |
| **OLD TABLE** | Refers to the old table in a trigger |
| **NEW TABLE** | Refers to the new table in a trigger |

---
### **Events**

| Statement | Description |
|-----------|-------------|
| **CREATE EVENT** | Creates a new scheduled event |
| **ALTER EVENT** | Modifies an existing event |
| **DROP EVENT** | Removes an event |
| **ON SCHEDULE** | Specifies the schedule for an event |
| **AT** | Specifies a one-time schedule for an event |
| **EVERY** | Specifies a recurring schedule for an event |
| **STARTS** | Specifies the start time for an event |
| **ENDS** | Specifies the end time for an event |
| **DO** | Specifies the SQL statement to execute for an event |
| **ENABLE** | Enables an event |
| **DISABLE** | Disables an event |
| **ALTER DEFINER** | Changes the definer of an event |

---
---
---
## **SQL System Information**

---
### **Information Schema Views**

| View | Description |
|------|-------------|
| **INFORMATION_SCHEMA.CATALOGS** | Lists all catalogs (databases) in the instance |
| **INFORMATION_SCHEMA.SCHEMATA** | Lists all schemas in the current catalog |
| **INFORMATION_SCHEMA.TABLES** | Lists all tables and views in the current catalog |
| **INFORMATION_SCHEMA.VIEWS** | Lists all views in the current catalog |
| **INFORMATION_SCHEMA.COLUMNS** | Lists all columns in all tables and views |
| **INFORMATION_SCHEMA.TABLE_CONSTRAINTS** | Lists all table constraints |
| **INFORMATION_SCHEMA.KEY_COLUMN_USAGE** | Lists all key column usages |
| **INFORMATION_SCHEMA.REFERENTIAL_CONSTRAINTS** | Lists all referential constraints |
| **INFORMATION_SCHEMA.CHECK_CONSTRAINTS** | Lists all check constraints |
| **INFORMATION_SCHEMA.COLUMN_DOMAIN_USAGE** | Lists all column domain usages |
| **INFORMATION_SCHEMA.DOMAIN_CONSTRAINTS** | Lists all domain constraints |
| **INFORMATION_SCHEMA.DOMAINS** | Lists all domains |
| **INFORMATION_SCHEMA.CHARACTER_SETS** | Lists all character sets |
| **INFORMATION_SCHEMA.COLLATIONS** | Lists all collations |
| **INFORMATION_SCHEMA.COLLATION_CHARACTER_SET_APPLICABILITY** | Lists all collation and character set applicability |
| **INFORMATION_SCHEMA.ROUTINES** | Lists all routines (procedures and functions) |
| **INFORMATION_SCHEMA.PARAMETERS** | Lists all parameters for routines |
| **INFORMATION_SCHEMA.FUNCTIONS** | Lists all functions |
| **INFORMATION_SCHEMA.PROCEDURES** | Lists all procedures |
| **INFORMATION_SCHEMA.TABLE_PRIVILEGES** | Lists all table privileges |
| **INFORMATION_SCHEMA.COLUMN_PRIVILEGES** | Lists all column privileges |
| **INFORMATION_SCHEMA.USAGE_PRIVILEGES** | Lists all usage privileges |
| **INFORMATION_SCHEMA.VIEW_TABLE_USAGE** | Lists all table usages by views |
| **INFORMATION_SCHEMA.VIEW_COLUMN_USAGE** | Lists all column usages by views |
| **INFORMATION_SCHEMA.ELEMENT_TYPES** | Lists all element types |
| **INFORMATION_SCHEMA.ASSERTIONS** | Lists all assertions |
| **INFORMATION_SCHEMA.SQL_FEATURES** | Lists all supported SQL features |
| **INFORMATION_SCHEMA.SQL_IMPLEMENTATION_INFO** | Provides information about the SQL implementation |
| **INFORMATION_SCHEMA.SQL_LANGUAGES** | Lists all supported SQL languages |
| **INFORMATION_SCHEMA.SQL_PACKAGES** | Lists all SQL packages |
| **INFORMATION_SCHEMA.SQL_PARTS** | Lists all SQL parts |
| **INFORMATION_SCHEMA.SQL_SIZING** | Provides information about sizing limits |
| **INFORMATION_SCHEMA.SQL_TYPE_INFO** | Provides information about data types |

---
---
### **System Catalog Tables**

---
#### **PostgreSQL System Catalogs**

| Table | Description |
|-------|-------------|
| **pg_class** | Stores information about tables, indexes, views, sequences, etc. |
| **pg_attribute** | Stores information about table columns |
| **pg_type** | Stores information about data types |
| **pg_namespace** | Stores information about schemas |
| **pg_tables** | Lists all tables in the database |
| **pg_indexes** | Lists all indexes in the database |
| **pg_proc** | Stores information about functions and procedures |
| **pg_operator** | Stores information about operators |
| **pg_am** | Stores information about access methods |
| **pg_amop** | Stores information about access method operators |
| **pg_amproc** | Stores information about access method procedures |
| **pg_language** | Stores information about procedural languages |
| **pg_trigger** | Stores information about triggers |
| **pg_constraint** | Stores information about constraints |
| **pg_inherits** | Stores information about table inheritance |
| **pg_depend** | Stores information about dependencies between objects |
| **pg_description** | Stores descriptions for database objects |
| **pg_statistic** | Stores statistics used by the query planner |
| **pg_rewrite** | Stores information about query rewriting rules |
| **pg_rules** | Stores information about rules |
| **pg_views** | Stores information about views |
| **pg_matviews** | Stores information about materialized views |
| **pg_sequences** | Stores information about sequences |
| **pg_settings** | Stores database configuration parameters |
| **pg_database** | Stores information about databases |
| **pg_tablespace** | Stores information about tablespaces |
| **pg_role** | Stores information about database roles |
| **pg_authid** | Stores information about authentication identifiers |
| **pg_group** | Stores information about role membership |
| **pg_user** | Stores information about database users |
| **pg_shadow** | Stores information about user passwords |

---
#### **SQL Server System Catalogs**

| Table | Description |
|-------|-------------|
| **sys.tables** | Lists all user-defined tables |
| **sys.views** | Lists all user-defined views |
| **sys.columns** | Lists all columns in all tables and views |
| **sys.types** | Lists all data types |
| **sys.objects** | Lists all database objects |
| **sys.indexes** | Lists all indexes |
| **sys.index_columns** | Lists all columns used in indexes |
| **sys.constraints** | Lists all constraints |
| **sys.foreign_keys** | Lists all foreign key constraints |
| **sys.check_constraints** | Lists all check constraints |
| **sys.default_constraints** | Lists all default constraints |
| **sys.key_constraints** | Lists all primary and unique key constraints |
| **sys.databases** | Lists all databases |
| **sys.schemas** | Lists all schemas |
| **sys.sql_modules** | Lists all SQL modules (procedures, functions, etc.) |
| **sys.parameters** | Lists all parameters for SQL modules |
| **sys.procedures** | Lists all stored procedures |
| **sys.functions** | Lists all user-defined functions |
| **sys.triggers** | Lists all triggers |
| **sys.partitions** | Lists all partitions |
| **sys.partition_functions** | Lists all partition functions |
| **sys.partition_schemes** | Lists all partition schemes |
| **sys.partition_range_values** | Lists all partition range values |
| **sys.filegroups** | Lists all filegroups |
| **sys.files** | Lists all database files |
| **sys.dm_exec_requests** | Lists all active execution requests |
| **sys.dm_exec_sessions** | Lists all active sessions |
| **sys.dm_tran_active_transactions** | Lists all active transactions |
| **sys.dm_tran_session_transactions** | Lists all active session transactions |

---
#### **MySQL System Catalogs**

| Table | Description |
|-------|-------------|
| **information_schema.TABLES** | Lists all tables in all databases |
| **information_schema.COLUMNS** | Lists all columns in all tables |
| **information_schema.STATISTICS** | Lists all table index statistics |
| **information_schema.KEY_COLUMN_USAGE** | Lists all key column usages |
| **information_schema.REFERENTIAL_CONSTRAINTS** | Lists all referential constraints |
| **information_schema.TABLE_CONSTRAINTS** | Lists all table constraints |
| **information_schema.CHECK_CONSTRAINTS** | Lists all check constraints |
| **information_schema.ROUTINES** | Lists all stored routines (procedures and functions) |
| **information_schema.PARAMETERS** | Lists all parameters for routines |
| **information_schema.VIEWS** | Lists all views |
| **information_schema.TRIGGERS** | Lists all triggers |
| **information_schema.EVENTS** | Lists all scheduled events |
| **information_schema.PROCESSLIST** | Lists all active processes |
| **information_schema.SCHEMATA** | Lists all schemas (databases) |
| **information_schema.ENGINES** | Lists all storage engines |
| **information_schema.PLUGINS** | Lists all plugins |
| **information_schema.CHARACTER_SETS** | Lists all character sets |
| **information_schema.COLLATIONS** | Lists all collations |
| **information_schema.COLLATION_CHARACTER_SET_APPLICABILITY** | Lists all collation and character set applicability |

---
#### **Oracle System Catalogs**

| Table | Description |
|-------|-------------|
| **ALL_TABLES** | Lists all tables accessible to the current user |
| **ALL_COLUMNS** | Lists all columns in tables accessible to the current user |
| **ALL_INDEXES** | Lists all indexes on tables accessible to the current user |
| **ALL_CONSTRAINTS** | Lists all constraints on tables accessible to the current user |
| **ALL_CONS_COLUMNS** | Lists all columns used in constraints accessible to the current user |
| **ALL_OBJECTS** | Lists all objects accessible to the current user |
| **ALL_SOURCE** | Lists the source code of all objects accessible to the current user |
| **ALL_PROCEDURES** | Lists all procedures accessible to the current user |
| **ALL_FUNCTIONS** | Lists all functions accessible to the current user |
| **ALL_PACKAGES** | Lists all packages accessible to the current user |
| **ALL_TRIGGERS** | Lists all triggers accessible to the current user |
| **ALL_SEQUENCES** | Lists all sequences accessible to the current user |
| **ALL_SYNONYMS** | Lists all synonyms accessible to the current user |
| **ALL_VIEWS** | Lists all views accessible to the current user |
| **ALL_MVIEWS** | Lists all materialized views accessible to the current user |
| **USER_TABLES** | Lists all tables owned by the current user |
| **USER_COLUMNS** | Lists all columns in tables owned by the current user |
| **USER_INDEXES** | Lists all indexes on tables owned by the current user |
| **USER_CONSTRAINTS** | Lists all constraints on tables owned by the current user |
| **USER_CONS_COLUMNS** | Lists all columns used in constraints owned by the current user |
| **USER_OBJECTS** | Lists all objects owned by the current user |
| **USER_SOURCE** | Lists the source code of all objects owned by the current user |
| **USER_PROCEDURES** | Lists all procedures owned by the current user |
| **USER_FUNCTIONS** | Lists all functions owned by the current user |
| **USER_PACKAGES** | Lists all packages owned by the current user |
| **USER_TRIGGERS** | Lists all triggers owned by the current user |
| **USER_SEQUENCES** | Lists all sequences owned by the current user |
| **USER_SYNONYMS** | Lists all synonyms owned by the current user |
| **USER_VIEWS** | Lists all views owned by the current user |
| **USER_MVIEWS** | Lists all materialized views owned by the current user |
| **DBA_TABLES** | Lists all tables in the database |
| **DBA_COLUMNS** | Lists all columns in all tables |
| **DBA_INDEXES** | Lists all indexes in the database |
| **DBA_CONSTRAINTS** | Lists all constraints in the database |
| **DBA_CONS_COLUMNS** | Lists all columns used in constraints in the database |
| **DBA_OBJECTS** | Lists all objects in the database |
| **DBA_SOURCE** | Lists the source code of all objects in the database |
| **DBA_PROCEDURES** | Lists all procedures in the database |
| **DBA_FUNCTIONS** | Lists all functions in the database |
| **DBA_PACKAGES** | Lists all packages in the database |
| **DBA_TRIGGERS** | Lists all triggers in the database |
| **DBA_SEQUENCES** | Lists all sequences in the database |
| **DBA_SYNONYMS** | Lists all synonyms in the database |
| **DBA_VIEWS** | Lists all views in the database |
| **DBA_MVIEWS** | Lists all materialized views in the database |
| **DBA_USERS** | Lists all users in the database |
| **DBA_TAB_PRIVS** | Lists all table privileges in the database |
| **DBA_COL_PRIVS** | Lists all column privileges in the database |
| **DBA_SEQ_PRIVS** | Lists all sequence privileges in the database |

---
---
---
### **System Functions**

| Function | Description |
|----------|-------------|
| **CURRENT_DATE** | Returns the current date |
| **CURRENT_TIME** | Returns the current time |
| **CURRENT_TIMESTAMP** | Returns the current date and time |
| **LOCALTIME** | Returns the current local date and time |
| **LOCALTIMESTAMP** | Returns the current local date and time |
| **NOW** | Returns the current date and time |
| **SYSDATE** | Returns the current date and time (Oracle, MySQL) |
| **CURRENT_USER** | Returns the current user name |
| **SESSION_USER** | Returns the current session user name |
| **SYSTEM_USER** | Returns the system user name |
| **USER** | Returns the current user name |
| **DATABASE** | Returns the name of the current database |
| **VERSION** | Returns the version of the database server |

---
### **System Variables**

---
#### **MySQL System Variables**

| Variable | Description |
|----------|-------------|
| **@@auto_increment_increment** | Auto-increment increment value |
| **@@auto_increment_offset** | Auto-increment offset value |
| **@@autocommit** | Autocommit mode (0 or 1) |
| **@@character_set_client** | Character set for the client |
| **@@character_set_connection** | Character set for the connection |
| **@@character_set_database** | Character set for the database |
| **@@character_set_filesystem** | Character set for the filesystem |
| **@@character_set_results** | Character set for result sets |
| **@@character_set_server** | Character set for the server |
| **@@collation_connection** | Collation for the connection |
| **@@collation_database** | Collation for the database |
| **@@collation_server** | Collation for the server |
| **@@default_storage_engine** | Default storage engine |
| **@@default_week_format** | Default week format |
| **@@have_ssl** | Whether SSL support is available |
| **@@hostname** | Server hostname |
| **@@interactive_timeout** | Timeout for interactive connections |
| **@@max_connections** | Maximum number of connections |
| **@@port** | Server port |
| **@@server_id** | Server ID |
| **@@time_zone** | Server time zone |
| **@@tmpdir** | Temporary directory |
| **@@version** | Server version |
| **@@wait_timeout** | Timeout for non-interactive connections |

---
---
---
## **SQL Comments and Delimiters**

---
### **Comments**

| Syntax | Description |
|--------|-------------|
| **-- comment** | Single-line comment |
| **/* comment */** | Multi-line comment |
| **# comment** | Single-line comment (MySQL) |
| **--! comment** | Special comment (MySQL) |

---
### **Delimiters**

| Delimiter | Description |
|-----------|-------------|
| **;** | Statement terminator |
| **,** | Comma separator |
| **.** | Dot separator (e.g., schema.table) |
| **( )** | Parentheses for grouping expressions |
| **[ ]** | Square brackets for identifiers (SQL Server) |
| **{ }** | Curly braces for compound statements |
| **' '** | Single quotes for string literals |
| **" "** | Double quotes for identifiers |
| **` `** | Backticks for identifiers (MySQL) |
| **$** | Dollar sign for tagged templates (PostgreSQL) |

---
---
---
## **SQL Escape Sequences**

| Escape Sequence | Description |
|-----------------|-------------|
| **\'** | Single quote |
| **\"** | Double quote |
| **\\** | Backslash |
| **\0** | Null character |
| **\b** | Backspace |
| **\n** | Newline |
| **\r** | Carriage return |
| **\t** | Tab |
| **\Z** | PostgreSQL string terminator |
| **\xHH** | Hexadecimal character (PostgreSQL) |

---
---
---
## **SQL Reserved Keywords**

| Keyword | Description |
|---------|-------------|
| **ALL** | Quantifier for predicates and set operations |
| **ALTER** | Modifies a database object |
| **AND** | Logical AND operator |
| **ANY** | Quantifier for predicates |
| **AS** | Renames a column or table with an alias |
| **ASC** | Ascending order in ORDER BY |
| **BETWEEN** | Range condition |
| **BY** | Specifies the grouping or ordering criteria |
| **CASE** | Conditional expression |
| **CAST** | Converts a value to a specified data type |
| **CHECK** | Defines a check constraint |
| **COLLATE** | Specifies a collation for string comparison |
| **COLUMN** | Specifies a column in a table |
| **COMMIT** | Commits a transaction |
| **CONSTRAINT** | Defines a constraint |
| **CREATE** | Creates a new database object |
| **CROSS** | Specifies a cross join |
| **CURRENT** | Specifies the current value |
| **CURRENT_DATE** | Returns the current date |
| **CURRENT_TIME** | Returns the current time |
| **CURRENT_TIMESTAMP** | Returns the current timestamp |
| **CURRENT_USER** | Returns the current user |
| **DATABASE** | Specifies a database |
| **DAY** | Specifies the day part of a date |
| **DECLARE** | Declares a variable or cursor |
| **DEFAULT** | Specifies a default value |
| **DELETE** | Deletes rows from a table |
| **DESC** | Descending order in ORDER BY |
| **DISTINCT** | Removes duplicate rows from a result set |
| **DROP** | Removes a database object |
| **ELSE** | Alternative branch in a CASE expression |
| **END** | Ends a block of statements |
| **ESCAPE** | Specifies an escape character for LIKE patterns |
| **EXCEPT** | Set operation (difference) |
| **EXISTS** | Tests for the existence of rows |
| **FALSE** | Boolean false value |
| **FETCH** | Specifies the number of rows to return |
| **FOR** | Specifies the target of a cursor or trigger |
| **FOREIGN** | Specifies a foreign key constraint |
| **FROM** | Specifies the source tables for a query |
| **FULL** | Specifies a full outer join |
| **FUNCTION** | Specifies a user-defined function |
| **GENERATED** | Specifies a generated column |
| **GROUP** | Groups rows for aggregation |
| **HAVING** | Filters groups after aggregation |
| **HOUR** | Specifies the hour part of a time |
| **IDENTITY** | Specifies an identity column |
| **IMMEDIATE** | Specifies immediate execution |
| **IN** | Tests for membership in a set |
| **INDEX** | Specifies an index |
| **INNER** | Specifies an inner join |
| **INSERT** | Inserts rows into a table |
| **INTERSECT** | Set operation (intersection) |
| **INTERVAL** | Specifies a time interval |
| **INTO** | Specifies the target of an INSERT or SELECT INTO |
| **IS** | Tests for NULL or boolean conditions |
| **JOIN** | Specifies a join operation |
| **LANGUAGE** | Specifies the language for a function |
| **LATERAL** | Specifies a lateral join |
| **LEADING** | Specifies the leading table in a join |
| **LEFT** | Specifies a left outer join |
| **LIKE** | Pattern matching |
| **LIMIT** | Limits the number of rows returned |
| **LOCAL** | Specifies a local variable or transaction |
| **MINUTE** | Specifies the minute part of a time |
| **MONTH** | Specifies the month part of a date |
| **NATURAL** | Specifies a natural join |
| **NO** | Negates a condition |
| **NOT** | Logical NOT operator |
| **NULL** | Specifies a NULL value |
| **OF** | Specifies the source of a cursor or trigger |
| **OFFSET** | Skips a specified number of rows |
| **ON** | Specifies the join condition |
| **OR** | Logical OR operator |
| **ORDER** | Specifies the sorting criteria |
| **OUTER** | Specifies an outer join |
| **OVER** | Defines a window for window functions |
| **PARTITION** | Divides a result set into partitions |
| **PERCENT** | Specifies a percentage |
| **PIVOT** | Transforms rows into columns |
| **PRECISION** | Specifies the precision for numeric types |
| **PRIMARY** | Specifies a primary key constraint |
| **PROCEDURE** | Specifies a stored procedure |
| **RANGE** | Specifies a range for window functions |
| **RECURSIVE** | Specifies a recursive CTE |
| **REFERENCES** | Specifies a foreign key constraint |
| **REGEXP** | Regular expression pattern matching |
| **RIGHT** | Specifies a right outer join |
| **ROLLBACK** | Rolls back a transaction |
| **ROW** | Specifies a row in a window function |
| **ROWS** | Specifies rows in a window frame |
| **SAVEPOINT** | Creates a savepoint in a transaction |
| **SCHEMA** | Specifies a schema |
| **SECOND** | Specifies the second part of a time |
| **SELECT** | Retrieves data from a table |
| **SEQUENCE** | Specifies a sequence |
| **SESSION** | Specifies a session variable or setting |
| **SET** | Assigns a value to a variable or specifies a set operation |
| **SIMPLE** | Specifies a simple data type |
| **SIZE** | Specifies the size of a data type |
| **SOME** | Quantifier for predicates (synonym for ANY) |
| **START** | Starts a transaction |
| **TABLE** | Specifies a table |
| **TABLESAMPLE** | Specifies a table sampling method |
| **THEN** | Specifies the result of a WHEN clause in a CASE expression |
| **TIME** | Specifies a time value |
| **TIMESTAMP** | Specifies a timestamp value |
| **TIMEZONE_HOUR** | Specifies the time zone hour |
| **TIMEZONE_MINUTE** | Specifies the time zone minute |
| **TO** | Specifies the target of a CAST or the end of a range |
| **TRAILING** | Specifies the trailing table in a join |
| **TRANSACTION** | Specifies a transaction |
| **TRIGGER** | Specifies a trigger |
| **TRUE** | Boolean true value |
| **TRUNCATE** | Truncates a table |
| **UNBOUNDED** | Specifies an unbounded window frame |
| **UNION** | Set operation (union) |
| **UNIQUE** | Specifies a unique constraint |
| **UNKNOWN** | Specifies an unknown value |
| **UNPIVOT** | Transforms columns into rows |
| **UPDATE** | Updates rows in a table |
| **USER** | Specifies a user |
| **USING** | Specifies the columns to join on |
| **VALUES** | Specifies values for an INSERT statement |
| **VIEW** | Specifies a view |
| **WHEN** | Specifies a condition in a CASE expression |
| **WHERE** | Filters rows in a query |
| **WINDOW** | Specifies a named window |
| **WITH** | Defines a Common Table Expression (CTE) |
| **WITHIN** | Specifies a time window |
| **YEAR** | Specifies the year part of a date |
| **ZONE** | Specifies a time zone |