## Library Management System

## Project Title
Library Management System 

## System Description
The Library Management System is a database-driven application designed to manage the core operations of a library. It keeps track of members, books, staff, and borrowing transactions, ensuring that information is organized, consistent, and easy to query.

## Tables Description
The system allows the library to:

## Users
Store and maintain information about library members including name, email, and phone number.
## Books
Track book details such as title, author, ISBN, and the number of available copies.
## Borrow 
Record which user borrowed which book and when, including the return date.
## Staff
Maintain a record of staff responsible for library operations.

The database supports common SQL operations like SELECT, INSERT, UPDATE, DELETE, JOIN, and SUBQUERY. Indexing is used to improve query performance.

## Features Implemented
## User Management
The system stores and manages user information such as name, email, and contact number. Each user is uniquely identified using a primary key.
## Book Management
Allows storage of book details including title, author, ISBN, and available copies. Ensures accurate tracking of library resources.
## Borrowing System
Records borrowing transactions, linking users and books. Tracks borrow dates and return dates to monitor book circulation.
## Staff Management
Maintains records of library staff responsible for handling operations.
## Relational Database Design
Tables are connected using primary and foreign keys to maintain strong relationships and data integrity.
## Normalization (UNF to 3NF)
The database structure is normalized to eliminate redundancy, avoid anomalies, and ensure efficient data organization.
## SQL Operations (CRUD)
Supports:
SELECT (retrieve data)
INSERT (add records)
UPDATE (modify records)
DELETE (remove records)
## Advanced Queries
Includes JOIN operations to combine tables and SUBQUERIES for more complex data retrieval.
## Indexing
Indexes are applied to improve query performance, especially for search operations.
## Data Integrity and Consistency
Constraints like primary keys and foreign keys ensure that data remains accurate and consistent.

## Reflection
Developing this project allowed me to experience how databases are designed in a practical way. I learned how to organize data into multiple related tables and ensure that each table has a clear purpose.

One of the key things I understood was the importance of normalization. By breaking down data from UNF to 3NF, I was able to remove unnecessary duplication and make the database more efficient and consistent.

I also gained confidence in using SQL. I practiced creating tables and performing different operations such as retrieving records, modifying data, and combining tables using JOINs and subqueries to get more meaningful results.

Another concept I learned was indexing. I observed that adding an index can significantly improve query speed, especially when searching large amounts of data, although it may slightly affect other operations. I learned how to use Git as a tool for managing my project. Keeping my work organized through commits made it easier to track changes and avoid mistakes. This project helped me understand both the technical and practical aspects of database management, which will be useful in future projects.