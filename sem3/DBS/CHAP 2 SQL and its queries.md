# TAGS
[[README]] 
# Source:
[[DBS Resources|| Slides]] contain everything.


# #IMP 


# SQL #DEF 
Structured query language is the [[CHAP1 Introduction to DB and RDBMS#DATA, DB AND MANAGEMENT || database]] language by which we can perform operations on the database, we can also use SQL to create a database. 

## SQL Commands #EXP 
SQL commands are like instructions to a table, it is used to interact with the table/database. It is used to perform specific tasks such as dropping, altering, etc. it can even be used to modify permissions of specific users.

## Database Languages
- DDL - data definition language
	 deals with database schemas and definitions. 
	 Commands included are 
	 - Create 
	 - Alter
	 - Drop
- DML - data manipulation language
	 Deals with data manipulation, used to store, modify, retrieve and update data in database.
	 Commands included are
	 - Select
	 - Insert
	 - Update
	 - Delete
- DQL - data query language
	 Similar to DML. NOT IN TEST OR PORTION.
- DCL - data control language
	 Deals with the flow of data within a database, mostly concerned with the permissions and controls of users in the database.
	 Commands included are
	 - Grant
	 - Revoke
- TCL - transaction control language
	 Deals with the transactions in a database, i.e. the transfer of data between users.
	 Commands included are
	 - Commit
	 - Rollback
	 - Savepoint

# DDL Commands #DEF 

| Command  | Description                                                                      | Syntax                                                   |
| -------- | -------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CREATE   | creates database or objects                                                      | CREATE object object_name;                               |
| DROP     | Delete objects from the database                                                 | DROP object object_name;                                 |
| ALTER    | Alter the structure of the database                                              | ALTER TABLE table_name ADD column column_name data_type; |
| TRUNCATE | Removes all records from a table, including the spaces allocated for the records | TRUNCATE TABLE table_name;                               |
| RENAME   | Renames an object of the database                                                | RENAME TABLE old_table_name TO new_table_name;           |
# DML Commands #DEF 

| Command | Description                          | Syntax                                                   |
| ------- | ------------------------------------ | -------------------------------------------------------- |
| INSERT  | Insert data into table               | INSERT INTO table_name VALUES;                           |
| UPDATE  | Update the existing data in a table  | UPDATE table_name SET column1= value1, column2 = value2; |
| DELETE  | Delete records from a database table | DELETE FROM table_name;                                  |
# DCL Commands #DEF 

| Command | Description                      | Syntax                                                       |
| ------- | -------------------------------- | ------------------------------------------------------------ |
| GRANT   | Assigns new privileges to a user | GRANT privilege ON object_name TO user \[with grant option]; |
| REVOKE  | Removes a privilege from a user  | REVOKE \[grant option] privilege ON object_name FROM user;   |
# TCL Commands #DEF 

| Command           | Description                                        | Syntax                              |
| ----------------- | -------------------------------------------------- | ----------------------------------- |
| BEGIN TRANSACTION | Starts a new transaction                           | BEGIN TRANSACTION transaction_name; |
| COMMIT            | Saves all changes made during the transaction      | COMMIT;                             |
| ROLLBACK          | Undoes all the changes made during the transaction | ROLLBACK;                           |
| SAVEPOINT         | Creates a savepoint within the current transaction | SAVEPOINT savepoint_name;           |
# DQL Commands #DEF 

| Command | Description                            | Syntax                          |
| ------- | -------------------------------------- | ------------------------------- |
| Select  | It is used to display tables from data | SELECT column1 FROM table_name; |
# Important SQL commands #EXP 

| Command                                                         | Example                                                                                     |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [[CHAP 2 SQL and its queries#DQL Commands DEF \| SELECT]]       | SELECT * FROM table_name;                                                                   |
| [[CHAP 2 SQL and its queries#DML Commands DEF \| INSERT]]       | INSERT INTO table_name VALUES value1, value2;                                               |
| [[CHAP 2 SQL and its queries#DML Commands DEF \| UPDATE]]       | UPDATE employees SET attribute = “value” WHERE attribute = “thisvalue”;                     |
| [[CHAP 2 SQL and its queries#DML Commands DEF \| DELETE]]       | DELETE FROM employees WHERE attribute = “thisvalue”;                                        |
| [[CHAP 2 SQL and its queries#DDL Commands DEF \| CREATE TABLE]] | CREATE TABLE employees ( employee_id INT PRIMARY KEY, first_name VARCHAR(50) );             |
| [[CHAP 2 SQL and its queries#DDL Commands DEF \| ALTER TABLE]]  | ALTER TABLE employees ADD COLUMN phone VARCHAR(20);                                         |
| [[CHAP 2 SQL and its queries#DDL Commands DEF \| DROP TABLE]]   | DROP TABLE employees                                                                        |
| WHERE                                                           | SELECT * FROM table_name WHERE attribute = “value”;                                         |
| ORDER BY                                                        | SELECT * FROM table_name ORDER BY attribute DESC/ASC;                                       |
| JOIN                                                            | SELECT e.first, e.last, d.depart FROM employees e JOIN department d ON e.depart = d.depart; |
# Datatypes in MySQL #EXP 
- Numeric Types
	 - INT (SIZE): Integer type, optional display size;
	 - FLOAT: single precise floating point number;
	 - DOUBLE: double precision floating point number;
- Date and time types
	 - DATE: date value  in ‘YYYY-MM-DD’ format
	 - TIME: in ‘hh:mm’ format
	 - DATETIME: combined format
	 - TIMESTAMP: in DATETIME format
	 - YEAR: 4 digit year format
- String types
	 - CHAR(SIZE): Fixed length character string
	 - VARCHAR(SIZE): Variable length character string
	 - TEXT: Variable length character string (larger)

# Integrity Constraints #EXP 
There are 4 types of integrity constraints.
[[INTEGRITY CONSTRAINTS.canvas|INTEGRITY CONSTRAINTS]] 
## Key Constraints #EXP 
Keys are the entity set that is used to identify an entity within its entry.

An entity set can have multiple keys but out of which one key needs to be primary key, a primary key needs contain a unique value in relational database. 

When  a primary key contains a repeated value, it is not allowed and as such key constraints is implemented.
## Domain Constraints #EXP 
Domain constraints can be defined as the definition of a valid set of values for an attribute.

The data type of domain includes string, characters, integer, etc. the value of the attribute must be available in the corresponding table.

If the value of attribute is not found then domain constraint is implemented.

## Referential Integrity Constraints #EXP 
A referential integrity constraint is specified between two tables.

In referential integrity constraints, if a foreign key in table 1 refers to primary key of table 2 then every value of foreign key needs to be unique, if it is not then referential integrity constraint is implemented.

## Check Constraints #EXP 
The check constraint is used to limit the value range that can be placed in a column.

If you define a check constraint on a column it will allow only certain values for this column.

if you define a check constraint on a table, it can limit the values in certain columns based on values in other columns in the row.
# Procedural Language/Structured Query Language 
PL/SQL is Oracle Corporation’s procedural extension for SQL and the oracle relational database application.

It allows you to write procedural logic such as loops, conditions and exception handling directly within SQL commands.

PL/SQL combines the data manipulating power of SQL with the procedural capabilities of a programming language, making it a powerful tool for managing databases.

## Key concepts of PL/SQL
- Blocks
	 PL/SQL programs are made of blocks, which can be anonymous blocks, procedural blocks, functions. triggers, etc.
- Variables and Constants
	 PL/SQL allows you to declare variables and constants to store data temporarily permanently.
- Control Structures
	 PL/SQL includes standard programming constructs like loops, conditional statements and more.
- Exceptional handling
	 You can handle errors and exceptions using exception blocks.
- Cursors
	 Cursors are used for traversing the records in result set. PL/SQL provides both implicit and explicit cursors.
- Procedures and Functions 
	 These are reusable program units stored in the database. Procedures perform an action, while functions returns a value.
### Example of PL/SQL #EXM 
![[Pasted image 20240822065419.png | Example of PL/SQL function]]
# Functions in PL/SQL #EXP 
There are 2 types of functions in PL/SQL
- User-defined functions
- Ready made functions
[[Functions in PL_SQL.canvas| Hierarchy of Functions in PL_SQL]]

## Single Row Functions #EXP 
Single row or scalar functions return a value for every row that is processed in a query.

### String Functions #EXP 
- Initcap(str): This function is used to convert the first letter of string to capital letter
- Concatenate (Exp, Exp): This function is used to append two or more literal expression with eachother
- Replace: In this function, the 1st set of character is replaced with the 2nd set of characters given in string
- Lower(‘string’): This function is to convert all upper case letters to lower case in given string
- Substring(‘string‘, starting char_no, no. of characters): This function is used to return the part of string from given index to ending index.
- Translate(‘string’, ‘letter’, ‘letter’): This function is used to replace a single character.
- Ltrim and Rtrim: These functions are used to trim out strings from left side and right side respectively
- Upper(‘string’): This function is used to convert all lower case letters to upper case in given string
- CHR(ASCII_VALUE): This function is used to return the character assigned to given ASCII number.
- LPAD(‘string’, index,’replace’): This function is used to pad given symbol for given number of times on the LEFT
- RPAD(‘string’, index,’replace’): This function is used to pad given symbol for given number of times on the RIGHT
### Arithmetic Functions #EXP 

| Function Name | Description                                                                       |
| ------------- | --------------------------------------------------------------------------------- |
| ABS           | This function returns the absolute value of given number                          |
| CEIL          | Ceil function returns the smallest integer greater than or equal to passed number |
| EXP(n)        | Exp returns exponential value of given number                                     |
| FLOOR         | This function returns largest integer equal or less than number passed            |
| LN(a)         | This function returns natural log of a value                                      |
| log(a,b)      | This function returns log of b to the base of a                                   |
| MOD(a,b)      | This function returns reminder of the division between a and b                    |
| POWER(a,b)    | This function returns the value obtained after $$a^b$$                            |
| ROUND(a,b)    | This function returns the rounded value of a to the decimal places.               |
| SIGN(a)       | This function shows negative or positive number                                   |
| SIN(a)        | This function returns value obtained after $$sin(a)$$                             |
| SQRT(a)       | This function returns value obtained after $$\sqrt a$$                            |
| TRUNC(a,b)    | This function returns value obtained after truncated a to b decimal places        |

## Group Functions #EXP 
These functions group the rows of data based on the values returned by the query.

These functions group are used to calculate aggregate values like total or average.

### Date and time functions #EXP 

| Function Name    | Description                                                                             |
| ---------------- | --------------------------------------------------------------------------------------- |
| ADD_MONTHS       | Adds the specified number of months to a date                                           |
| LAST_DAY         | Returns the last day of a specified month                                               |
| MONTHS_INBETWEEN | Calculates the number of months between two dates                                       |
| NEW_TIME         | Returns the date/time value with time shifted as requested                              |
| NEXT_DAY         | Returns the date of the 1st week day specified that is later than the date              |
| ROUND            | Returns the date rounded by specified format unit                                       |
| SYSDATE          | Returns the current date and time in the oracle server                                  |
| TRUNC            | Truncates the specified date of its time portion according to the format unit provided. |
### Aggregate functions #EXP 

| Function Name | Usage                                       |
| ------------- | ------------------------------------------- |
| AVG(EXP)      | Returns average of given expression         |
| COUNT(EXP)    | Counts the row defined by expression        |
| COUNT(\*)     | Counts all rows in table                    |
| MIN(EXP)      | Returns minimal value defined by expression |
| MAX(EXP)      | Returns maximum value defined by expression |
| SUM(EXP)      | Returns sum value of given column           |
# Queries using clauses #EXP 
## Group by clause #EXP 
It is used with the select query, following the where clause but preceeding order by clause.

The group by field generally has repeated values or records

Syntax: select * from table_name where (condition) group by column1, column2, column3;

## Having clause #EXP 
The having clause enables you to specify conditions that filter which group results appear in results.

Syntax: select * from table_name where (condition) group by column1, column2, column3 having condition1, condition2;

## Order by clause #EXP 
The SQL order by clause is used to sort the data in ascending order or descending order, based on the columns.
It sorts in ascending by default.
to sort in descending, DESC keyword must be used.

Syntax: select * from table_name order by column1, column2 ASC;

# Subqueries #EXP 
Subquery is a form of an SQL statement that appears inside another SQL statement. It is also called nested queries.
The statement containing the subquery is called parent statement.
## Example of subquery #EXM 
select cust_no, name from cust_dtls where cust_no in (select cust_no, acc_no, acc_bal from cust_dtls where acc_no < A-4 AND acc_bal < 25000);


