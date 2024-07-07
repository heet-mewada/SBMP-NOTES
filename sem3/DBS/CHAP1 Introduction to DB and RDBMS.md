
# Source:
[[Resources]] contains Info on EVERYTHING in it’s rawest form that sir himself put in the PPT


# DATA, DB AND MANAGEMENT 
- ## data #DEF
	It is a raw material(information), that exists in any file format.
- ## DB #DEF 
	It is the collection of structured information or data usually in table format.
- ## DBMS #DEF 
	<mark style="background: #D2B3FFA6;">A Database Management System (DBMS) is a software system that is designed to manage and organize data in a structured manner.</mark> It allows users to create, modify, and query a database, as well as manage the security and access controls for that database.
- ## RDBMS #DEF 
	A Relational Database Management System (RDBMS) is a program that allows you to create, update, and administer a relational database. <mark style="background: #FFF3A3A6;">Most RDBMSs use the SQL language to access the database.</mark> A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables.
	<mark style="background: #FFF3A3A6;">It allows users to set up relationship between many tables at once which is not possible in DBMS.</mark>

# DBMS AND RDBMS #DIFF 
|         Points          | DBMS                                     | RDBMS                                             |
| :---------------------: | ---------------------------------------- | ------------------------------------------------- |
| **==Data Integrity==**  | **==does not force integrity==**         | **==forces integrity==**                          |
| **==Data Redundancy==** | **==does not care about redundancy==**   | **==eliminates redundancy using normalization==** |
|    **==Features==**     | **==no specific features==**             | **==SQL, backups, DBA==**                         |
|    **==Relations==**    | **==does not have a relational model==** | **==is built on a relational model==**            |
|      Data Storage       | stores as files                          | stores as tables                                  |
|    Multi-user access    | single user                              | multi-user                                        |
|     Multiple Views      | does not support multiview               | supports multiview                                |

# Features of RDBMS 
- ##  Referential integrity #DEF 
	[[#RDBMS DEF | RDBMS]] ensures that the relationships between the data elements in different tables are maintained, i.e. ensuring data consistency and integrity

- ##  SQL #DEF 
	RDBMS uses structured query language to interpret and execute commands such as UPDATE, INSERT, DELETE, MAKE and ALTER.

- ##  ACID #DEF 
	RDBMS implements the ACID([[#Atomicity DEF| Atomicity]], [[#Consistency DEF|Consistency]], [[#Isolation DEF|Isolation]], [[#Durability DEF|Durability]]) model to ensure data consistency and integrity.

- ##  Indexing #DEF 
	RDBMS provides indexing to improve query performance and data retrieval.

- ## Normalization #DEF 
	RDBMS uses normalization to reduce data redundancy and improve data integrity.

- ##  Keys #DEF 
	RDBMS uses keys in attributes to make it easier to manage the database.
	
- ##  Access control #DEF 
	RDBMS allows the DBA to give certain privileges to people, namely view, edit and manage privileges which allows those users to access the database in the way that privilege intends. 


## ACID #EXP 

- ### Atomicity #DEF
	==Atomicity guarantees that all of the commands that make up a transaction are treated as a single unit and either succeed or fail together.== This is important as in the case of an unwanted event, like a crash or power outage, we can be sure of the state of the database. The transaction would have either completed successfully or been rolled back if any part of the transaction failed.

- ### Consistency #DEF 
	<mark style="background: #FFB8EBA6;">Consistency guarantees that changes made within a transaction are consistent with database constraints.</mark> This includes all rules, constraints, and triggers. If the data gets into an illegal state, the whole transaction fails.

- ### Isolation #DEF 
	<mark style="background: #FF5582A6;">Isolation ensures that all transactions run in an isolated environment.</mark> That enables running transactions concurrently because transactions don’t interfere with each other.

- ### Durability #DEF 
	<mark style="background: #FFF3A3A6;">Durability guarantees that once the transaction completes and changes are written to the database, they are persisted.</mark> This ensures that data within the system will persist even in the case of system failures like crashes or power outages.


## ACID #EXM 
![[ACID EXAMPLE.png | Acid Example]] 

# Abstraction #EXP 

- ## Physical Level #DEF 
	 Describes a how a record is stored.
- ## Logical Level #DEF 
	 Describes data in the data warehouse(collection of DB) and the relationship between that data (view [[#Data Models EXP | Data Models]] for explanation).
- ## View Level #DEF 
	 Describes how data looks to the end user, i.e. hides unnecessary data for the end user that need not be seen by them or other end users for security purposes.

# Abstraction Levels #DIA 
![[Abstraction.png| Data Model]]

# Schema #EXP 
- ## Logical Schema #EXP 
	 - The logical structure of the DB, i.e. how the database is structured logically with programs on the software it is stored in.
	 - Applications depend on the logical schema
- ## Physical Schema #EXP 
	 - The physical structure of the DB, i.e. how the database is stored outside of software, inside the data warehouse.

## Data Independence #DEF 
The ability to change the physical schema without changing the logical schema.

# Instance #DEF 
The content of the DB at a point of time.

# DBA #DEF 
The person with central control of the data and the processes that control it is called the DBA or DataBase Administrator.

## Works of DBA #EXP 
- ### Schema Definition:
	 The DBA creates the original structure of the DB by using a set of defining statements in DDL.
- ### Storage structure and access-method definition.
	  The DBA decides how the data is presented in the DB
- ### Schema and physical-organization  modification.
	 The DBA modifies the schema and physical organization of the DB in accordance to the needs of the DB
- ### Granting of authorization.
	 The DBA decides who gets certain privileges in the DB, i.e. end users cannot access the DB outside of the application while [[#Application Programmers DEF | application programmers]] or [[#Sophisticated Users DEF | sophisticated users]] can access the DB.
- ### Routine maintenance.
	 It is the job of the DBA to maintain the DB.
- ### Assisting AP.
	 DBA helps [[#Application Programmers DEF | application programmers]] to make applications.
- ### Backup and Restore
	 DBA makes backups of the DB so that the data if ever lost can be restored from when the DB was backed up. DBA should routinely make backups.


# Types of Users 
## Naive Users #DEF 
Unsophisticated users(end users) that are not concerned with the DB or its programs. These users interact with the DB through an interface but cannot modify the DB in any way except their own entry.
## Application Programmers #DEF 
Users that interact with the DB using programs through [[#DML DEF]](Data Manipulation Language) and RAD(Rapid development tools). RAD allows application programmers to construct forms and reports with minimal efforts.
## Sophisticated Users #DEF 
Users that interact with the DB using data query languages or by using tools like data analysis tools. They don’t interact using programs like [[#Application Programmers DEF]] but interact using [[#SQL DEF]] queries that directly interact with the query processor.
## Specialized Users #DEF 
Users who write specialized database applications such as computer-aided design systems, knowledge base and expert systems, systems that store data with complex data types.

# Data Models #EXP
A collection of tools that help with describing data, relations between data, data constraints and semantics.
There are multiple data models such as [[#ER Model EXP | ER Model]], Relational Model, there are older models that are still used such as Network Model and Hierarchical Model.

## ER Model #EXP 
This model uses objects known as Entities and the relationship between them to display [[#data DEF  | data]]. 

- ### Entity #DEF 
	An object in the which is distinguishable from other objects.

- ### Relationship #DEF 
	Association between several entities. 

## ER #DIA 

![[Example of ER.png| Example of ER model]]

## Advantages of ER #EXP 
- Easy to develop relations 
- Specific Mapping Capabilities
- Specific Keys like primary key
- Generalization and Specialization
## Disadvantages of ER #EXP 
- Only conceptional and not used in market.
## Attributes of ER #EXP 
Each entity has attributes, the particular properties that describe it. For each attribute, there is a set permitted values called domain or value set of attribute, which can be either strings or numbers. Attributes can be either composite or simple(atomic) attributes & single valued or multi valued attributes & stored or derived attributes.

## Composite vs Atomic Attributes #DIFF 

| Points | Composite Attributes                                                                                                            | Atomic Attributes                                                                                    |
| ------ | ------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Def    | Attributes composed of objects that can be divided into other attributes with independent meanings.                             | Attributes which cannot be divided into smaller attributes with independent meanings.                |
| Exmp   | Name can be a composite attribute as it can be divided into different attributes such as first name, middle name and last name. | Id’s are an atomic attribute as they cannot be divided into different attributes unless designed to. |
## Singled vs Multi valued Attributes #DIFF 
| Points | Singled Valued Attributes                                                         | Multi Valued Attributes                                                          |
| ------ | --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Def    | Attributes with only one possible data value for a singular entry.                | Attributes with multiple possible data value for a singular entry.               |
| Exmp   | Age for a person can only one possible data value for a singular person at a time | College degree can multiple possible data values for a singular person at a time |

## Stored vs Derived Attributes #DIFF 
| Points | Stored Attributes                                     | Derived Attributes                                           |
| ------ | ----------------------------------------------------- | ------------------------------------------------------------ |
| Def    | Attributes from which derived attributes are derived. | Attributes that can be determined by another attribute.      |
| Exmp   | Date of Birth is a stored attribute                   | Age is a derived attribute that can be determined by the DoB |