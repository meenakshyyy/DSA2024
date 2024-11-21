# Introduction to Databases
## Why Databases?
  **Alternatives:** CSV file, text file, excel file are all flat files
  **Databases** make our life simpler, easier, faster, reliable, and secure
        * E.g finding rows where value of a particular column>10 is time consuming in flat files. Databases
          use a technique called indexing with simple and easy to use langauge called SQL
          to achieve the result faster.
        * This is done without much programming background, instead it uses the quering language.
        * Databases backup the data at multiple places to increase reliability

        * Example Databases
          Oracle, MySQL, SQLServer

## -Relational and Non-relational Databases
*	-Relational Db stores data in a structured tables with rows and columns, using a predefined schema 
to clearly define relationships between data points.
MySQL, Postgre SQ , Oracle, MySQL server.

## -Non relational Database
* 	-MongoDB, (NoSQL),Non-relational database (often called NoSQL) offers more flexibility by storing 
            data in various formats like documents, key-value pairs, or graphs, allowing for less structured 
            and more dynamic data sets; essentially.

* Relational databases are ideal for highly structured data with complex queries, while non-relational 
    databases excel in handling large volumes of diverse data with rapid scalability needs.


## Tables
* In a relational database all our data is stored across multiple tables to avoid duplication.
* Primary keys are unique. It is associated with each tables.

## SQL-Structured Query Language
* Operations-CRUD Create Read Update Delete
* It is called Declarative programming language and domanin specific lang
* C/C++, Python are procedural language, step by step instructions are provided
* gen purpose lang allows web dev gaming operating sys,db etc.

## SQL execution stmts:
* SQL->Parser, compiler
* -> Parser: tries to understand the query 
* ->compiler: query optimizer and generated code.
* ->query executer->DB->results

## USE, DESCRIBE, SHOW Tables
    - mysql -u root -p root
    - CNTRL+L to clear the screen
    - CREATE DATABASE imdb;
    - USE <DB NAME>;
        - USE imdb;
    - SHOW tables;
    - DESCRIBE <table_name>;
        - shows the schema of a particular table
        - DESCRIBE actors;
## SELECT
    - Suppose if i want to list all the movies, i can use select clause 

## LIMIT, OFFSET
    -  view information like a page by page fashion
        - e.g. flipkart view gadgets by price/review

    - SELECT name, rankscore FROM movies LIMIT 20;
    - SELECT name, rankscore FROM movies LIMIT 20 OFFSET 40;


## ORDER BY
    - SELECT name, year FROM movies ORDER BY year DESC LIMIT 10;
    - default sorting order in ascending
    - The output row order maynot be same as the one in the table due to
    query optimizer and internal data-structures/indices.


## DISTINCT
    - Can be used to find distinct values with in a columns
    - SELECT DISTINCT genre FROM movie_genres;
    - SELECT DISTINCT first_name. last_name FROM directors ORDER BY first_name;
## Logical Operators
* AND, OR, NOT, ANY, ALL, LIKE, SOME, IN, BETWEEN, EXISTS
* All these operators are clubed with WHERE clause

## Aggregate functions
* COUNT MAX MIN SUM
* GROUP BY often used with Aggregate functions.
* HAVING conditions on groups.

## Order of execution
* GROUP BY to creat groups
* apply the Aggregate functions
* apply HAVING conditions on groups

## SELECT * FROM WHERE G-H-O-L
* *- ALL 
* G-Group BY
* H-HAVING
* O-Order BY
* L-Limit(has OFFSET)

# JOIN and natural join
* JOIN combine data in multiple tables having same column names
* type of inner join where we dont have to specific coloumns, it performs 
natural join.

# table aliases
* eg TableA a, TableB be

# Left join
* Join the tables on the right with left with columns of right with respect 
to left, it can be null if a particular val for right doesnt exist.

# OUTER JOIN
* join all values in the table

# Nested Query
* first inner query is executed then the outer query.
* ANY operator return True if any subquery value meets the conditions
* ALL operator return True if all of the subquery value meet the conditions
* IN,EXISTS,NOT IN, NOT EXISTS, ANY, ALL , Comparison Operators 

# CREATE 
* CREATE TABLE table_name(
    col1 data-type,
    col2 data_type
);

# INSERT
* INSERT INTO table_name(col1,col2)
values('val1','val2'),(....);

# UPDATE 
* UPDATE table_name
SET col='val'
WHERE condition;

# ALTER 
* alter the structure of the table
* ALTER TABLE table_name
ADD col_name col_dtype();
* ALTER TABLE table_name
 RENAME old_name,new_name;

* Adding new columns
        - ALTER TABLE students 
          ADD email VARCHAR(100);
* Rename column
        - ALTER TABLE students 
         RENAME COLUMN grade TO final_grade;

# TRUNCATE
* Delete the contents of the table not the table
* TRUNCATE TABLE table_name;
# DROP
* Delete the whole table including the schema
* Deletes both tableand all of the data permanently
    - DROP TABLE Tablename;
    - DROP TABLE tablename IF EXISTS;
# DELETE 
* Delete the selected values of the table
 
