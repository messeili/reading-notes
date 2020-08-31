## SQL
SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

## Relational databases
A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

## Select queries
By using SELECT statement we can retrieve data from database. A query is a statement that declares what data we are looking for and where to find it in the database(represented as a table). ex:
```
SELECT column1, column2 ;
FROM mytable;
```
To select all the colomns in a database/table use SELECT *

## Constraints/conditions
In order to filter certain results from being returned, we need to use a WHERE clause in the query.

SELECT column;
FROM mytable
WHERE condition
    AND/OR another_condition
operators that are used with WHERE:

=Case sensitive exact string comparison
!= or <>Case sensitive exact string inequality comparison
LIKE Case insensitive exact string comparison
% Used anywhere in a string to match a sequence of zero or more characters(only with LIKE or NOT LIKE)
_ Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)
IN (listitems)String exists in a list