# SQL
Here, you will learn SQL from basic to Advance


# What is SQL(Structured Query Language)?  
It is a Language that is used to Interact with Database.  
  
# Difference between SQL and MYSQL:
| SQL                           | MYSQL                                                     |    
| ----------------------------- | -------------                                             |   
| it is a query language        | itself a RDBMS(Relational Data Base Mangement System      |   
| way to access data            | server where data is accesed                              |   


# Install it in your PC   
u can watch the process of installation above in installation file  

# Datatypes  
Sure, here's how you can document the data types in a README.md file:
  
No need to learn all the Data types:

# Data Types for Database Columns  

1. **CHAR(size)**
   - Description: A fixed-length string that can contain letters, numbers, and special characters.
   - Size Range: 0 to 255 characters.
   - Default Size: 1 character.

2. **VARCHAR(size)**
   - Description: A variable-length string that can contain letters, numbers, and special characters.
   - Size Range: 0 to 65,535 characters.
   - Default Size: 1 character.

3. **BINARY(size)**
   - Description: Similar to CHAR(), but stores binary byte strings.
   - Size Range: 0 to 255 bytes.
   - Default Size: 1 byte.

4. **VARBINARY(size)**
   - Description: Similar to VARCHAR(), but stores binary byte strings.
   - Size Range: 0 to 65,535 bytes.

5. **TINYBLOB**
   - Description: Used for BLOBs (Binary Large Objects) with a maximum length of 255 bytes.

6. **TINYTEXT**
   - Description: Holds a string with a maximum length of 255 characters.

7. **TEXT(size)**
   - Description: Holds a string with a maximum length of 65,535 bytes.

8. **BLOB(size)**
   - Description: Used for BLOBs (Binary Large Objects) with a maximum length of 65,535 bytes.

9. **MEDIUMTEXT**
   - Description: Holds a string with a maximum length of 16,777,215 characters.

10. **MEDIUMBLOB**
    - Description: Used for BLOBs (Binary Large Objects) with a maximum length of 16,777,215 bytes.

11. **LONGTEXT**
    - Description: Holds a string with a maximum length of 4,294,967,295 characters.

12. **LONGBLOB**
    - Description: Used for BLOBs (Binary Large Objects) with a maximum length of 4,294,967,295 bytes.

13. **ENUM(val1, val2, val3, ...)**
    - Description: A string object that can have only one value chosen from a list of possible values.
    - Value Limit: Up to 65,535 values in the ENUM list.

14. **SET(val1, val2, val3, ...)**
    - Description: A string object that can have 0 or more values chosen from a list of possible values.
    - Value Limit: Up to 64 values in the SET list.  

  # Numeric Data Types

1. **BIT(size)**
   - Description: A bit-value type with a specified number of bits per value.
   - Size Range: 1 to 64 bits.
   - Default Size: 1 bit.

2. **TINYINT(size)**
   - Description: A very small integer with both signed and unsigned ranges.
   - Signed Range: -128 to 127.
   - Unsigned Range: 0 to 255.
   - Size Parameter: Maximum display width, up to 255.

3. **BOOL / BOOLEAN**
   - Description: A boolean type where zero is considered false, and nonzero values are considered true.

4. **SMALLINT(size)**
   - Description: A small integer with both signed and unsigned ranges.
   - Signed Range: -32768 to 32767.
   - Unsigned Range: 0 to 65535.
   - Size Parameter: Maximum display width, up to 255.

5. **MEDIUMINT(size)**
   - Description: A medium integer with both signed and unsigned ranges.
   - Signed Range: -8388608 to 8388607.
   - Unsigned Range: 0 to 16777215.
   - Size Parameter: Maximum display width, up to 255.

6. **INT(size) / INTEGER(size)**
   - Description: A medium integer with both signed and unsigned ranges.
   - Signed Range: -2147483648 to 2147483647.
   - Unsigned Range: 0 to 4294967295.
   - Size Parameter: Maximum display width, up to 255.

7. **BIGINT(size)**
   - Description: A large integer with both signed and unsigned ranges.
   - Signed Range: -9223372036854775808 to 9223372036854775807.
   - Unsigned Range: 0 to 18446744073709551615.
   - Size Parameter: Maximum display width, up to 255.

8. **FLOAT(size, d)**
   - Description: A floating-point number with a specified total number of digits and digits after the decimal point. *(Deprecated)*

9. **FLOAT(p)**
   - Description: A floating-point number. MySQL uses p to determine FLOAT or DOUBLE data type.
   - If p is 0 to 24, the data type becomes FLOAT().
   - If p is 25 to 53, the data type becomes DOUBLE().

10. **DOUBLE(size, d)**
    - Description: A normal-size floating-point number with a specified total number of digits and digits after the decimal point.

11. **DOUBLE PRECISION(size, d)** (Equivalent to DOUBLE(size, d))

12. **DECIMAL(size, d) / DEC(size, d)**
    - Description: An exact fixed-point number with a specified total number of digits and digits after the decimal point.
    - Size Range: Up to 65 digits.
    - Decimal Range: Up to 30 digits.
    - Default Size: 10 digits.
    - Default Decimal: 0 digits.

# Date and Time Data Types

1. **DATE**
   - Description: A date in the format YYYY-MM-DD.
   - Supported Range: '1000-01-01' to '9999-12-31'.

2. **DATETIME(fsp)**
   - Description: A date and time combination in the format YYYY-MM-DD hh:mm:ss.
   - Supported Range: '1000-01-01 00:00:00' to '9999-12-31 23:59:59'.
   - Additional Options: DEFAULT and ON UPDATE in the column definition allow automatic initialization and updating to the current date and time.

3. **TIMESTAMP(fsp)**
   - Description: A timestamp, stored as the number of seconds since the Unix epoch ('1970-01-01 00:00:00' UTC).
   - Format: YYYY-MM-DD hh:mm:ss.
   - Supported Range: '1970-01-01 00:00:01' UTC to '2038-01-09 03:14:07' UTC.
   - Additional Options: DEFAULT CURRENT_TIMESTAMP and ON UPDATE CURRENT_TIMESTAMP allow automatic initialization and updating to the current date and time.

4. **TIME(fsp)**
   - Description: A time in the format hh:mm:ss.
   - Supported Range: '-838:59:59' to '838:59:59'.

5. **YEAR**
   - Description: A year in four-digit format.
   - Values Allowed: 1901 to 2155, and 0000.
   - Note: MySQL 8.0 does not support the year in two-digit format.
