
## Intro to Databases

- Multiple users, massive data, complex tasks
- Uses in security: login attempts, software and updates, machines and owners
- Relational Databases
  -  Keys: columns that relate two tables
    -  Primary key: column where every row has a unique entry
    -  Foreign key: column that is a primary key in another table
  - Table can have 1 primary key, multiple foreign
  
## Quering Databases

- SELECT/FROM:
  - `mysql> SELECT employee_id, device_id
  -> FROM employees;`
  - `mysql> SELECT *
  -> FROM employees~`
- ORDER BY
- ORDER BY DESC

## Filtering Queries 
- Syntax
- Return columns with USA entries alone: `WHERE country = 'USA'`
- Rerturn entries starting with US including USA `WHERE country LIKE 'US%'`

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
  - BETWEEN, AND
    `WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';`
  - Operators(>,<,=,>=,<=,<>)
    `WHERE birthdate > '1970-01-01';`

## Example wildcard filters

- `a%`: apple123, art, a
- `a_`: as, an, a7
- `a__`: ant, add, a1c
- `%a`: pizza, Z6ra, a
- `_a`: ma, 1a, Ha
- `%a%`: Again, back, a
- `_a_`: Car, ban, ea7
