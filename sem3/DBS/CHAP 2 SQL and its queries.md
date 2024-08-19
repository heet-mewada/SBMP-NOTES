
# Source:
[[Resources || Slides]] contain everything.

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
