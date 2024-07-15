# DBMS Quick Notes
## Properties of database
1. **Reduces redundancy/Integrated:** A database can be a collection of data from different files and when any redundancy among those files are removed from database is said to be integrated data.
2. **Atomicity:**  Atomicity is a property of database transactions that ensures that a set of database operations **either all occur, or none occur**.Eg, Transaction Process. 
3. **Consistency:** Value should remain preserved always.
4. **Isolation:** Isolation is the property of a database where **no data should affect the other one and may occur concurrently**.Eg, in the case of transactions, when two or more transactions occur simultaneously, the consistency should remain maintained. 
5. **Durabilty:** In DBMS, the term durability ensures that the data after the successful execution of the operation becomes **permanent** in the database.
6. **Sharing Data:** The data stored in the database can be shared by multiple users simultaneously without affecting the correctness of data.
7. **Persitent:** If data is removed from database due to some explicit request from user to remove.
8. **Secure**
9. **Concurrent Access**
10. **Data Independence:** Data independence is usually considered from two points of views; **physically data independence**
and **logical data independence**.
    - **Physical data independence:** Changes in conceptual level doesn't affect in physical level.
    - **Logical data independence:** Changes in external level doesn't affect in conceptual level.
11. **Abstraction:** Data Abstraction is a process of hiding unwanted or irrelevant details from the end user.
- **ACID:** Atomicity,Consistency,Isolation,Durability
## Database Basics
1. **Data/Item:** Eg: “e101”, ”sumit”
2. **Entities/Table:** An entity is a thing or object in the real world that is distinguishable from all other objects.\
Eg: Bank, employee, student
3. **Attribute/Columns:** Attributes are properties are properties of an entity.\
Eg: Empcode, ename, rolno, name
4. **Logical data:** Logical data are the data for the table created by user in primary memory.
5. **Physical data:** Physical data refers to the data stored in the secondary memory.
6. **Schema:** A schema is a logical data base description and is drawn as a chart of the types of data that are used.
It gives the names of the entities and attributes and specify the relationships between them.
7. **Sub-schema:** A subschema is derived schema derived from existing schema as per the user requirement
8. **Degree:** total number of columns.
9. **Cardinality:** Total number of rows.
10. **Data integrity:** There are three categories of data integrity
    - **Entity integrity:** 
        - It specifies that there should be **no duplicate rows** in a table.
        - key contrainsts
    - **Domain integrity:** 
        - It enforces valid entries for a given column by restricting the type, the format, or the range of values.
        - Data types
    - **Referential integrity:** specifies that rows cannot be deleted, which are used by other records.
    - **User-defined integrity:** It enforces some specific business rules defined by users.
11. **Database users:** 
    - **Naive Users:** Users who need not be aware of the presence of the database system or any other system supporting their usage are considered naïve users . A user of an automatic teller machine falls on this category.
    - **Online Users :** These are users who may communicate with the database directly via an online terminal or indirectly via a user interface and application program. These users are aware of the database system and also know the data manipulation language system.
    - **Application Programmers :** Professional programmers who are responsible for developing application programs or user interfaces utilized by the naïve and online user falls into this category.
12. **Metadata:** 
    - Metadata means "data about data".
    - Metadata in a database is information that describes the database itself, rather than its contents.
    - It can include things like column names, database names, user names, schema,etc.
    - Helps users to find and understand data, and makes it reusable. 
13. **Data utilities:** A DBMS also provides a set of utilities for managing and controlling database activities. Examples of database utilities include reorganization, RUNSTATS, backup and copy, recover, integrity check, load data, unload data and repair database.
## Datababe Languages
1. **Data Definition Language (DDL):**
    - It is used to **define** database structure or pattern.
    - It is used to **create schema, tables, indexes, constraints**, etc. in the database.
    - Eg, Create, Alter,Drop,Truncate,Rename,Comment
2. **Data Manipulation Language (DML):**
    - accessing and manipulating data in a database.
    - handles user requests.
    - Eg, Select,Insert,Update,Delete,join
3. **Data Control Language (DCL):**
   - It is used to retrieve the stored or saved data.
   - It is used to control permissions over database.
   - Eg, Grant, Revoke
## DBMS vs RDBMS
|Slno|DBMS|RDBMS|
|-|-|-|
|1.|Satisfies atleast 5-6 codd rules|Satisfies all codd rules|
|2.|It is used for small organization and deal with small data.|It is used to handle large amount of data.|
|3.|Data redundancy is common in this model.|Keys and indexes do not allow Data redundancy.|
|4.|Relationship between data is not specified.|Data is stored in the form of tables which are related to each other.|
|5.|Security is less|There exists multiple levels of data security in a RDBMS.|
|6.|Low software and hardware necessities.|Higher software and hardware necessities.|
|7.|Examples: XML, Window Registry, Forxpro, dbaseIIIplus etc.|Examples: MySQL, PostgreSQL, SQL Server, Oracle, Microsoft Access etc.|
## ER Concepts
- **Recursive Relationships:** When the same entity type participates more than once in a relationship type in different roles, the
relationship types are called recursive relationships.
- **Weak Entity:** 
    - Entity types that do not contain any key attribute, and hence can not be identified independently are called weak entity types.
    - A weak entity can be identified by uniquely only by considering some of its attributes in conjunction with the primary key attribute of another entity, which is called the identifying owner entity.
    - Relationship between owner entity and weak entity is one to many.
    - Weak entity has full contribution in it's relation with owner entity
## TRC
- **Unsafe Expression**: 
$\{t|NOT(EMPLOYEE(t))\}$ is unsafe because it yields all tuples in the universe that are not EMPLOYEE tuples, which are
 infinitely numerous. 
## Domain and data dependency
- Domain and data dependency in Database Management Systems (DBMS) refers to the relationship between the domain (tables, columns, relationships) and the data (records) that is stored in the system. Domain dependency is the relationship between two or more tables in the database, while data dependency is the relationship between the data stored in the tables. Domain dependency is important because it helps to maintain integrity, consistency, and accuracy of the data stored in the database. Data dependency is important because it ensures that any changes to the data in one table do not affect the data in the other tables.
- **Normalization:** Technique to remove and reduce redundancy from table.
