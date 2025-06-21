
## Intro to Databases

- Multiple users, massive data, complex tasks
- Uses in security: login attempts, software and updates, machines and owners
- Relational Databases
  -  Keys: columns that relate two tables
    -  Primary key: column where every row has a unique entry
    -  Foreign key: column that is a primary key in another table
  - Table can have 1 primary key, multiple foreign
  
## Quering Databases (Data Query Language)

- Main Command: SELECT
  -Basic
  `mysql> SELECT employee_id, device_id`
  -To return all columns:
  `mysql> SELECT *`
  
- Clauses include: FROM, ORDER BY, WHERE
- FROM
  `mysql> SELECT employee_id, device_id
  -> FROM employees;`
- ORDER BY (ascending)
  `SELECT customerid, city, country
  FROM customers
  ORDER BY city;`
- ORDER BY; DESC (descending)
  `SELECT customerid, city, country
  FROM customers
  ORDER BY city DESC;`
- Can sort multiple columns
  `SELECT customerid, city, country
  FROM customers
  ORDER BY city,country;`

## Filtering Queries 

- WHERE
  - Return columns with USA entries alone:
    `WHERE country = 'USA'`
  - Comparison operators(>,<,=,>=,<=,<>)
    `WHERE birthdate > '1970-01-01';`
    
- Wildcard filters
  - `a%`: apple123, art, a
  - `a_`: as, an, a7
  - `a__`: ant, add, a1c
  - `%a`: pizza, Z6ra, a
  - `_a`: ma, 1a, Ha
  - `%a%`: Again, back, a
  - `_a_`: Car, ban, ea7
    
  For example, to return entries starting with "US" including "USA":
    `WHERE country LIKE 'US%'`

- LIKE operator
  - Alternate to equal sign
    `WHERE country LIKE 'US%'`

  ## Data Types & Operators 
  - STRING, NUMERIC, DATE AND TIME
  - Numeric in security:
    - login attempts
    - log entries
    - data volume(source/destination)
  - Time:
    - login dates
    - login times
    - patch dates
    - connection duration

  ## Filtering Dates and Numbers
  - BETWEEN, AND
    `WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';`
  - Year: `YYYY-MM-DD`
  - Time: `HH:MM:SS`

  ## Filters with AND,OR, and NOT
  - AND
    `mysql>SELECT *
    FROM machines
    WHERE operating_system='OS 1' AND email_client='Email Client1';`
  - OR
    `SELECT*
    FROM
    WHERE operating_system='OS 1' 0R email_client='Email Client1';`
  - NOT
    `SELECT
    FROM
    WHERE NOT email_client='Email Client1';`
  - AND NOT
    `SELECT firstname, lastname, email, country
    FROM customers
    WHERE NOT country = 'Canada' AND NOT country = 'USA';`

    ## Join Tables
    - INNER JOIN
    - Syntax:
      `SELECT *
      FROM employees
      INNER JOIN machines ON employees.device_id = machines.device_id;`
    - SELECT* returns columnns existing in both tables twice. If you want to return one of matching columns:
      `SELECT username, operating_system, employees.device_id
      FROM  employees
      INNER JOIN machines ON employees.device_id = machines.device_id;`
    
    - OUTER JOINS: LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN
    - LEFT JOIN
      `SELECT *
      FROM employees
      LEFT JOIN machines ON employees.device_id = machines.device_id;`
      
    - RIGHT JOIN
      `SELECT *
      FROM employees
      RIGHT JOIN machines ON employees.device_id = machines.device_id;`
 
    - FULL OUTER JOIN
      `SELECT *
      FROM employees
      FULL OUTER JOIN machines ON employees.device_id = machines.device_id;`
      
    - Difference: Inner joins only return rows that match on a specified column, but outer joins also return rows that don't match on the specified column.
    - 
    


