## Creating Tables

- Define these datatypes in PostgreSQL:

  - NULL - no data
  - INTEGER - number
  - DECIMAL -  variable length after decimal
  - FLOAT - number with a decimal of undefined length
  - TEXT - a string
  - VARCHAR(n) - variable length

- What does SERIAL do in Postgres? (Note: in chinook.ml this will be INTEGER PRIMARY KEY AUTOINCREMENT)

adds autoincrement to the table

- What is the syntax for creating a new table?
  
  CREATE TABLE table_name (constraints)

- On <http://postgres.devmountain.com> , create a student table with this schema:
  - id - integer - primary key autoincrement
  - first_name - varchar(255)
  - hometown - varchar(255)
  - fun_fact - text

## Inserting Data (Section 9)

- What is the syntax for inserting values into a table?

- Insert the following data into the student table from above:
  
  ```
  first_name: 'Eric'
  hometown: 'Dallas'
  fun_fact: NULL
  ```
  
  ```
  first_name: 'James'
  hometown: 'Dallas'
  fun_fact: 'Postgres is progress.'
  ```

## Updating Data (Section 9)

- What is the syntax for updating existing values in a table?

- Update Eric's fun_fact to be 'I love SQL' using his id.

## Querying Data (Section 2 and 3)

### Syntax

- How do you select all columns from a table?

SELECT * FROM table_name

- How do you select 2 specific columns from a table?

SELECT column1 AND column2 FROM table_name

- What does DISTINCT do?

removes duplicate rows resulting from a query

- What does ORDER BY do?

state the display order for the results

- Practice: Get all the information we currently have in the student table, sorted by id, with the highest id first.

### WHERE clauses

- What are 4 comparison operators in PostgreSQL? (Hint: Look in the WHERE section)

=, >, <, !=

- What do AND, OR and IN do?

it's the logical operatior for && and ||, check if a value is in a list of values

- How do you check for NULL values? (Hint: it's not = NULL or != NULL)

value IS NULL

- What does LIMIT do?

limits the number of rows returned

- What do each of these aggregate functions do?

  - min() – return the minimum value.
  - max() – return the maximum value.
  - sum() – return the sum of all or distinct values.
  - avg() - return the average value.
  - count()– return the number of values.
  

- How does LIKE work?

returns data matching that value 

- What's the difference between % and \_ with LIKE?
