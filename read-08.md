# Read 08: SQL

* SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database
* To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries
* In order to filter certain results from being returned, we need to use a WHERE clause in the query
* More complex clauses can be constructed by joining numerous AND or OR logical keywords (ie. num_wheels >= 4 AND doors <= 2)
* writing clauses to constrain the set of rows returned also allows the query to run faster due to the reduction in unnecessary data being returned
* WHERE clauses with columns containing text data, SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching
* while most database implementations are quite efficient when using these operators, full-text search is best left to dedicated libraries like Apache Lucene or Sphinx. These libraries are designed specifically to do full text search, and as a result are more efficient and can support a wider variety of search features including internationalization and advanced queries
* the DISTINCT keyword will blindly remove duplicate rows, we will learn in a future lesson how to discard duplicates based on specific columns using grouping and the GROUP BY clause
* ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. In some databases, you can also specify a collation to better sort data containing international text
* LIMIT and OFFSET clauses, which are a useful optimization to indicate to the database the subset of the results you care about
* LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from
* In SQL, the database schema is what describes the structure of each table, and the datatypes that each column of the table can contain
* we need to use an INSERT statement, which declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert
* accidentally leaving out the WHERE clause (which causes the update to apply to all rows), you need to be extra careful when constructing UPDATE statements
* When you need to delete data from a table in the database, you can use a DELETE statement, which describes the table to act on, and the rows of the table to delete through the WHERE clause
* You can create a new database table using the CREATE TABLE statement
* SQL provides a way for you to update your corresponding tables and database schemas by using the ALTER TABLE statement to add, remove, or modify columns and table constraints
* In some databases like MySQL, you can even specify where to insert the new column using the FIRST or AFTER clauses, though this is not a standard feature
* you can use the DROP TABLE statement, which differs from the DELETE statement in that it also removes the table schema from the database entirely