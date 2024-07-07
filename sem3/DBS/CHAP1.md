# DATA, DB AND MANAGEMENT 
## data #DEF
It is a raw material(information), that exists in any file format.
## DB #DEF 
It is the collection of structured information or data usually in table format.
## DBMS #DEF 
<mark style="background: #D2B3FFA6;">A Database Management System (DBMS) is a software system that is designed to manage and organize data in a structured manner.</mark> It allows users to create, modify, and query a database, as well as manage the security and access controls for that database.
## RDBMS #DEF 
A Relational Database Management System (RDBMS) is a program that allows you to create, update, and administer a relational database. <mark style="background: #FFF3A3A6;">Most RDBMSs use the SQL language to access the database.</mark> A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables.
<mark style="background: #FFF3A3A6;">It allows users to set up relationship between many tables at once which is not possible in DBMS.</mark>

# DBMS AND RDBMS #DIFF 
|       Points        | DBMS                                 | RDBMS                                         |
| :-----------------: | ------------------------------------ | --------------------------------------------- |
| **==Data Integrity==**  | **==does not force integrity==**         | **==forces integrity==**                          |
| **==Data Redundancy==** | **==does not care about redundancy==**   | **==eliminates redundancy using normalization==** |
|    **==Features==**     | **==no specific features==**             | **==SQL, backups, DBA==**                         |
|    **==Relations==**    | **==does not have a relational model==** | **==is built on a relational model==**            |
|    Data Storage     | stores as files                      | stores as tables                              |
|  Multi-user access  | single user                          | multi-user                                    |
|   Multiple Views    | does not support multiview           | supports multiview                            |

# Features of RDBMS 
## Referential integrity #DEF 
RDBMS ensures that the relationships between the data elements in different tables are maintained, i.e. ensuring data consistency and integrity

## SQL #DEF 
RDBMS uses structured query language to interpret and execute commands such as UPDATE, INSERT, DELETE, MAKE and ALTER.

## ACID #DEF 
RDBMS implements the ACID([[#Atomicity DEF]], [[#Consistency DEF]], [[#Isolation DEF]], [[#Durability DEF]]) model to ensure data consistency and integrity.

## Indexing #DEF 
RDBMS provides indexing to improve query performance and data retrieval.

## Normalization #DEF 
RDBMS uses normalization to reduce data redundancy and improve data integrity.

## Keys #DEF 
RDBMS uses keys in attributes to make it easier to manage the database.
## Access control #DEF 
RDBMS allows the DBA to give certain privileges to people, namely view, edit and manage privileges which allows those users to access the database in the way that privilege intends. 


## ACID #DEF
### Atomicity #DEF 
<mark style="background: #ABF7F7A6;">Atomicity guarantees that all of the commands that make up a transaction are treated as a single unit and either succeed or fail together.</mark> This is important as in the case of an unwanted event, like a crash or power outage, we can be sure of the state of the database. The transaction would have either completed successfully or been rolled back if any part of the transaction failed.

### Consistency #DEF 
<mark style="background: #FFB8EBA6;">Consistency guarantees that changes made within a transaction are consistent with database constraints.</mark> This includes all rules, constraints, and triggers. If the data gets into an illegal state, the whole transaction fails.

### Isolation #DEF 
Isolation ensures that all transactions run in an isolated environment. That enables running transactions concurrently because transactions don’t interfere with each other.

### Durability #DEF 
<mark style="background: #FFF3A3A6;">Durability guarantees that once the transaction completes and changes are written to the database, they are persisted.</mark> This ensures that data within the system will persist even in the case of system failures like crashes or power outages.


## ACID #EXM 
![[ACID EXAMPLE.png]] 


# Types of Users 
## Naive Users #DEF 
Unsophisticated users(end users) that are not concerned with the DB or its programs. These users interact with the DB through an interface but cannot modify the DB in any way except their own entry.
## Application Programmers #DEF 
Users that interact with the DB using programs through DML(Data Manipulation Language) and RAD(Rapid development tools). RAD allows application programmers to construct forms and reports with minimal efforts.
## Sophisticated Users #DEF 



