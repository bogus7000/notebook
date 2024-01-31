*Based on course materials by Agnieszka Krasowska - Database Systems*

# Basics of SQL 

## Overview of SQL and Databases
1. What is SQL and what are its primary uses in relational and object-oriented relational databases?
2. How does the relational data model define the structure and manipulation of data?

## Basic Concepts of Databases
3. Describe the difference between data and information within the context of a database system.
4. What is a Database Management System (DBMS) and what are its main functions?

## Relational Data Model
5. Explain the concept of a relation in the relational data model. How is it represented?
6. What are the properties of a table in the relational model?
7. Define the terms 'primary key', 'unique key', and 'foreign key'. Provide examples.

## SQL Language Basics
8. Outline the history and evolution of SQL. How has it become a standard in database management?
9. Describe the basic syntax for creating, modifying, and deleting tables in SQL.

## Data Types and Table Creation
10. What are the standard SQL data types and how do they differ from Oracle's data types?
11. Provide the SQL syntax for creating a table with examples of integrity constraints.

## Data Manipulation in SQL
12. How do you insert, update, and delete data in a SQL table? Provide examples for each operation.
13. What is the purpose of the `COMMIT` and `ROLLBACK` statements in SQL?

## Simple Queries in SQL
14. Construct a simple `SELECT` statement and explain the function of each clause.
15. How does the `WHERE` clause filter the results of a SQL query?

## Expressions and Conditional Logic in SQL
16. Discuss the use of arithmetic, string, comparison, and logical operators in SQL expressions.
17. Explain how the `CASE`, `DECODE`, and `NVL` functions work in SQL with examples.

## Advanced Query Techniques
18. Describe how you can use the `ORDER BY` clause to sort query results.
19. How can the `DISTINCT` keyword be used to filter results in a SQL query?

## Type Conversion and Functions
20. What is the purpose of type conversion functions in SQL, and how do you use them?
21. Explain the difference between `CAST` in standard SQL and Oracle's conversion functions like `TO_CHAR`, `TO_DATE`, and `TO_NUMBER`.

## Review and Practice
22. Reflect on the examples provided in the lecture. How do they illustrate the practical application of SQL commands and functions?

## Applying Knowledge
23. Create a SQL query to display employees earning more than a certain amount and sort the result by hire date. Provide the SQL statement and explain each part of the query.

Based on the lecture content, here's a list of self-check study questions to help understand Lecture 2, formatted in Markdown:

# Continuation of SQL 

## Algebraic Operators on Queries
1. What are the three algebraic operators used in SQL queries and what do they do?
2. How do you use the `UNION` operator in a SQL query, and what is the significance of `UNION ALL`?

## Table Joins
3. Describe how to perform a simple inner join between two tables in SQL.
4. What is a self-join and provide an example where it might be used?

## Aggregate and Grouping Queries
5. List the aggregate functions available in SQL and explain their use.
6. How does the `GROUP BY` clause work in SQL, and how does it differ from using `DISTINCT`?

## Subqueries
7. What are subqueries and how can they be utilized in `SELECT`, `WHERE`, and `FROM` clauses?
8. Explain the difference between correlated and uncorrelated subqueries with examples.

## Outer Joins
9. What are `LEFT JOIN` and `RIGHT JOIN` in SQL, and when would you use them?
10. Provide an example of a SQL query that uses an outer join and explain the result set.

## Advanced Topics
11. Discuss the use of `EXISTS`, `ANY`, `ALL`, and `UNIQUE` operators in SQL queries.
12. How do subqueries enhance the functionality of `UPDATE` and `DELETE` statements in SQL?

## Practical Application
13. Create a SQL query that lists all departments along with the total salaries paid for each, including departments with no employees.
14. Write a SQL query using a subquery to find employees who earn more than the average salary of their department.

## Conceptual Understanding
15. How do the concepts of inner join, outer join, and subqueries contribute to the flexibility and power of SQL in data manipulation and analysis?

Based on the lecture content on advanced SQL constructions, here's a list of self-check study questions formatted in Markdown:

# Advanced SQL 

## Views
1. What is a view in SQL and how is it created?
2. How can views be used to simplify data access for different user groups?
3. Discuss the limitations and capabilities of views regarding data manipulation (INSERT, UPDATE, DELETE).

## Synonyms
4. Explain the purpose of synonyms in SQL and provide an example of their usage.

## Transactions
5. Define a transaction in the context of SQL and explain its importance.
6. What is the difference between `COMMIT` and `ROLLBACK` statements in transaction management?

## Locks and Isolation Levels
7. Describe the purpose of locks in database transactions.
8. Explain the different levels of transaction isolation and their impact on database operations.

## Data Dictionary
9. What is a data dictionary and what kind of information does it typically contain?

## Privileges
10. How are privileges granted and revoked in SQL, and what is the significance of the `WITH GRANT OPTION` clause?

## Schema
11. Define a schema in the context of SQL and describe how it is used.

## Temporary Tables
12. What are temporary tables, and when might they be useful?

## Sequences
13. Explain the purpose of sequences in Oracle and how they are used.

## Clusters
14. What is a cluster in Oracle, and how does it affect data storage and access?

## Applying Concepts
15. Propose a scenario where using a view with a `CHECK OPTION` would be beneficial.
16. Create an example where a transaction involves multiple `UPDATE` statements and requires a `ROLLBACK` due to an error.

Based on the lecture content from the document, here's a detailed list of self-check study questions focusing on advanced database concepts, specifically around integrity constraints, SQL*Plus, and database application programming. These questions are designed to test your understanding and application of the concepts covered in the lecture:

# Declarative Constraints 

## Declarative Integrity Constraints
1. What are declarative integrity constraints, and why are they important in database applications?
2. Differentiate between entity integrity constraints and referential integrity constraints. Provide examples for each.
3. How are primary key and unique key constraints defined within a database schema? What are their implications?
4. Explain the role of `NOT NULL` and `CHECK` constraints in maintaining data integrity.
5. Discuss the syntax differences between defining constraints at the column level and at the table level.

## Referential Actions
6. What are referential actions, and how do they affect database operations like `DELETE` and `UPDATE`?
7. Compare and contrast the effects of `ON DELETE CASCADE` and `ON DELETE SET NULL` options in referential integrity constraints.

## SQL*Plus and Database Applications
8. Describe the purpose and functionalities of SQL*Plus in Oracle database applications.
9. How do bind and substitution variables work in SQL*Plus, and what are their use cases?
10. List some common SQL*Plus commands and their purposes in database management and application development.

## Practical Application and Understanding
11. Given a scenario, how would you design a table with appropriate integrity constraints to ensure data quality?
12. Create a simple SQL*Plus script that demonstrates the use of bind variables in data manipulation.
13. Propose a set of referential actions that would be suitable for a database handling employee and department data, considering various operations like deletions and updates.

Based on the lecture content from the document on PL/SQL, here's a detailed list of self-check study questions formatted in Markdown:

# PL/SQL

## PL/SQL Basics
1. What is PL/SQL and how does it extend SQL?
2. Describe the structure of a PL/SQL block.

## Variables and Constants
3. How do you declare variables and constants in PL/SQL? Provide examples.
4. Discuss the significance of initializing variables and the use of the `DEFAULT` clause.

## Data Types
5. What are the unique data types available in PL/SQL that are not in standard SQL?

## Bind and Substitution Variables
6. Explain the difference between bind variables and substitution variables in PL/SQL.

## SELECT Statement in PL/SQL
7. How does the `SELECT INTO` statement function in PL/SQL and why can't it be used to display results directly on the screen?

## Cursors
8. What is a cursor in PL/SQL and how is it used to handle query result sets?
9. Describe the process of opening, fetching from, and closing a cursor.

## Exception Handling
10. List some common PL/SQL exceptions and explain how exception handling works in PL/SQL blocks.
11. How can custom exceptions be defined and used in PL/SQL?

## Control Structures
12. Describe the control structures available in PL/SQL, such as `IF`, `LOOP`, and `CASE`.

## Cursor Attributes
13. What are cursor attributes and how can they be used to control cursor behavior?

## FOR UPDATE Clause
14. Explain the `FOR UPDATE` clause in cursor declarations and its use cases.

## PL/SQL Records
15. What is a PL/SQL record and how does it differ from a rowtype variable?

# Procedural database objects 

## Procedures and Functions
1. What distinguishes a procedure from a function in PL/SQL?
2. How are parameters passed to procedures and functions in PL/SQL (i.e., IN, OUT, IN OUT)?
3. Provide an example of a PL/SQL procedure and explain the purpose of each component.

## Packages
4. What is a package in PL/SQL, and how does it differ from standalone procedures and functions?
5. Explain the significance of the package specification and package body.
6. How can package variables and constants maintain their state during a session?

## Database Triggers
7. Define a database trigger and describe its typical use cases.
8. Differentiate between row-level and statement-level triggers.
9. What are INSTEAD OF triggers, and when would you use them?
10. Discuss the restrictions associated with triggers, such as the mutating table issue.

## Practical Application
11. Design a trigger to enforce a business rule that is not easily implemented via declarative constraints.
12. How can a package help organize complex PL/SQL code in large applications?

## Advanced Concepts
13. Describe how system triggers differ from regular triggers and provide an example of their use.
14. How can dynamic SQL be utilized within PL/SQL procedures, and what are the potential risks?

# Object-oriented features 

## Object Orientation Basics
1. What is the purpose of introducing object-oriented features into relational databases?
2. How do procedural and data abstraction contribute to object orientation in databases?

## Object Types and Structures
3. Describe the structure of an object type in Oracle. What components does it include?
4. How do you define and implement an object type in Oracle SQL?

## Methods and Inheritance
5. What types of methods can be defined in an object type? Provide examples.
6. Explain the concept of inheritance in Oracle object types with an example.

## Object Tables and Constructors
7. What is an object table, and how is it different from a regular relational table?
8. How are object constructor methods used in PL/SQL and SQL?

## LOB Objects
9. Describe the different types of LOB (Large Object) data types in Oracle.
10. How are LOB objects stored and manipulated in Oracle databases?

## Working with Collections
11. What are collections in Oracle, and what types of collections are available?
12. Provide an example of how to use VARRAY in an Oracle database.

## Practical Application
13. Create an example that demonstrates the use of object types, including their methods and inheritance, in a database application.
14. How would you store and retrieve large objects like images or documents in an Oracle database?

# Physical database level 

## Physical Model of a Database
1. What distinguishes the physical model of a database from the logical model?
2. How does the architecture of computer systems influence the physical model of a database?

## Disks and Files
3. Describe the role of disk IO operations in database systems. Why are they considered high-cost operations?
4. Explain why databases primarily use magnetic disks for data storage despite the volatility and limited storage of RAM.

## Disk Space Management
5. What functions does the disk space manager perform in a database system?
6. How does the concept of pages facilitate data storage and access on disks?

## Data Buffers Management in RAM
7. What is the purpose of data buffers in database systems, and how are they managed?
8. Discuss the strategies for replacing pages in data buffers, such as LRU, MRU, and Clock.

## Record and Page Formats
9. Compare and contrast fixed-length and variable-length record formats. What are the advantages and disadvantages of each?
10. How do record identifiers (rids) work, and how do they facilitate data access?

## Record Files Organization
11. What is the difference between unordered (heap) files and sorted files in a database?
12. How does a hash file organization facilitate data retrieval based on search key values?

# Indexes. External Sorting

## Index Structures and Classification
1. What are the basic functions of index structures in databases, and how do they facilitate data retrieval?
2. Explain the difference between internal and external indexes.

## Data Structures for Indexes
3. Describe the characteristics of static ISAM trees and their use in databases.
4. What are B+ trees, and how do they improve upon the limitations of ISAM trees?

## External Sorting
5. Define external sorting and its importance in database operations.
6. Outline the steps involved in a multi-phase external sort by merging.

## Practical Applications
7. How do clustered and unclustered indexes affect data retrieval and storage efficiency?
8. Discuss the role of hash indexes and their limitations compared to tree-based indexes.

# Executing Queries 

## Relational Operations
1. Describe the basic relational operators used in SQL queries.
2. Explain the concept and implementation of the selection operation in SQL. What methods can be used for its realization?

## Join Methods
3. Compare and contrast different join methods, such as Simple Nested Loops Join, Index Nested Loops Join, Sort Merge Join, and Hash Join. What are their costs and when is each method preferred?
4. How does the concept of a cluster improve the efficiency of join operations?

## Query Optimization
5. What role does the query optimizer play in executing SQL queries?
6. Discuss the factors that the optimizer considers when choosing the best execution plan for a query.
7. How can the use of indexes influence the execution plan of a query?

## General Optimization Strategies
8. What are some general strategies for optimizing query execution in a DBMS?
9. Explain the significance of left-oriented trees in query optimization and how they facilitate running queries "in place."

# Planning of Indexes 

## Physical Database Design
1. What are the main goals of physical schema design and tuning in database systems?
2. How can redundancies in table schemas affect storage and data manipulation?
3. Explain the significance of BCNF (Boyce-Codd Normal Form) in eliminating redundancies related to functional dependencies.
4. Discuss the trade-offs between normal form compliance and query execution speed when designing database schemas.
5. What is horizontal decomposition, and how does it differ from vertical decomposition during normalization?
6. Describe the conditions under which a table might be split into two separate tables, such as "Students" and "Employees".

## Designing Indexes
1. How does one determine the workload of a database application, and why is it important for index planning?
2. What factors should be considered when deciding which tables and columns to index?
3. Discuss the differences between primary, unique, ordinary, clustered-internal, hash-internal, and ordinary indexes.
4. What are the considerations for choosing between hash indexes and tree indexes?
5. Explain the concept of "only-index" strategy and its importance in query optimization.

## Indexes in Oracle DBMS
1. What are the different types of indexes available in Oracle DBMS, and how do they function?
2. Describe the role of B+ tree indexes in Oracle and their suitability for range queries.
3. Explain the concept of index-organized tables and their advantages in Oracle.
4. How do hash indexes work in Oracle, and in what scenarios are they particularly useful?
5. Discuss the implications of creating an index with entries specified through expressions, such as using the `UPPER` function in an index.

## General Questions
1. What are the potential impacts of index creation on query performance and storage requirements?
2. How can materialized views be used in conjunction with indexes to optimize query execution?
3. Discuss the benefits and drawbacks of clustering tables in a database.
4. What are some strategies for optimizing queries and indexes in a database system?
5. How often should indexes be rebuilt, and why is it necessary?
6. Explain the importance of gathering and refreshing statistics used by the query optimizer.

# Transactions. Database recovery 

## Overview and Transactions
1. What is the significance of managing transactions in a database system with multiple users?
2. Define a transaction in the context of a DBMS. What constitutes a transaction in SQL language?
3. Explain the concept of concurrency in database transactions. Why is it important?
4. Describe the ACID properties in the context of database transactions.

## Concurrency Control
5. What problems can arise due to concurrent transactions in a DBMS?
6. How does the DBMS ensure the correctness and consistency of executed transactions amidst concurrency?
7. Explain the Strict Two-Phase Locking (Strict-2PL) protocol and its significance in transaction management.

## Locks and Locking Mechanisms
8. Differentiate between shared locks and exclusive locks in a database system.
9. How does the DBMS use locks to manage concurrent transactions and maintain database integrity?
10. What are the potential downsides or limitations of locking mechanisms in transaction management?

## Deadlocks
11. Define a deadlock in the context of database transactions. How can deadlocks be detected and resolved?
12. Discuss the strategies for deadlock prevention and their implications on database performance.

## Transaction Isolation Levels
13. Describe the four transaction isolation levels defined by the ANSI/ISO standard.
14. How do different isolation levels affect the interactions among concurrently executed transactions?

## Recovery Mechanisms
15. Explain the role of undo and redo logs in database recovery processes.
16. Describe the Write-Ahead Logging (WAL) rule and its importance in database recovery.
17. What is a checkpoint, and how does it facilitate database recovery?

## Advanced Topics
18. Discuss the concept of multi-version concurrency control (MVCC) and its advantages over traditional locking mechanisms.
19. What is optimistic locking, and how does it differ from pessimistic locking in transaction management?
20. Explain the concept of phantom reads and how they can be prevented in a database system.

## Practical Applications
21. How would you apply the knowledge of transaction management and concurrency control in designing a robust database system?
22. Given a scenario with specific transaction requirements, how would you choose the appropriate isolation level and locking mechanism?

# Distributed Databases

## Conceptual Understanding
1. What is a distributed database and how does it differ from a centralized database?
2. Discuss the advantages and disadvantages of distributed databases compared to centralized databases.
3. Explain the concepts of data fragmentation and replication in the context of distributed databases. What are the differences between horizontal and vertical fragmentation?

## Technical Details
4. Describe the role of transparency in distributed databases. What are the three types of transparency mentioned in the lecture?
5. How does a distributed database manage data consistency and integrity across different nodes?
6. What are the challenges associated with query optimization in distributed databases?

## Implementation and Practical Considerations
7. How is Oracle used to implement distributed database concepts? Specifically, discuss the role of database links and snapshot materialized views.
8. Explain the Two-Phase Commit protocol in the context of distributed transactions. What are its main stages and purpose?
9. Discuss the methods of replica synchronization in distributed databases. What are the differences between synchronic and asynchronic replication?

## Advanced Topics
10. How do distributed databases handle distributed joins and what are the methods to optimize them?
11. Describe the challenges and solutions related to data integration from different sources in distributed environments.
12. Given a scenario of an international company with regional offices, how would you design its distributed database in terms of data placement, replication, and updating?

## Reflection and Application
13. Reflect on a situation where a distributed database would be more beneficial than a centralized one. Justify your reasoning based on the lecture content.
14. How would you approach the problem of updating through replicas in a distributed database? What factors need to be considered?
15. Consider the problem of data integration discussed in the lecture. How would you apply the concepts of data warehouses and mediators to solve this problem?

# Data Warehouses 

## Introduction to Data Warehouses
1. What are the primary purposes of operational databases, and how do they support current business activities?
2. Explain the difference between OLTP and OLAP systems. 
3. What are the main characteristics of data warehouses? 
4. How do data warehouses handle data from different sources and over long periods?

## Properties of Data Warehouses
5. Describe the importance of data being subject-oriented in a data warehouse.
6. Why is nonvolatility a critical feature of data warehouses?
7. Explain the concept of time-variance in the context of data warehouses.
8. How is data transformed before being loaded into a data warehouse?

## Schema of Data Warehouse
9. Distinguish between facts and dimensions within a data warehouse schema.
10. What is a star schema, and how does it structure data for analysis?
11. Explain the significance of dimension tables in a star schema.
12. Describe how a multidimensional cube schema represents data differently from a relational schema.

## Operations on Data Warehouses
13. What is pivoting, and how does it reorganize data for analysis?
14. Define the drill-down and roll-up operations and their purposes in data analysis.
15. Explain the slice-and-dice operation and its use in data warehouses.

## Implementation in Oracle
16. What role do histograms play in Oracle's data warehouse implementation?
17. How does parallel processing improve performance in Oracle data warehouses?
18. Describe the purpose of partitioned objects in data management.
19. What are bitmapped indexes, and why are they useful in data warehouses?
20. Explain the STAR transformation and its impact on query performance.
21. What are materialized views, and how do they enhance query efficiency?

## Advanced SQL Features for Data Warehouses
22. Compare and contrast the ROLLUP and CUBE operators in SQL.
23. What are analytic (window) functions, and how do they enhance data analysis?

## Summary and Review
24. Summarize the key differences between data warehouses and operational databases.
25. Reflect on how the tools presented for Oracle's data warehouses facilitate complex data analysis.

*Edited and formatted with the help of ChatGPT*