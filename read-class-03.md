# inside a computer
* The motherboard is the computer's main circuit board
* The central processing unit (CPU), also called a processor, is located inside the computer case on the motherboard.
* A processor's speed is measured in megahertz (MHz), or millions of instructions per second; and gigahertz (GHz), or billions of instructions per second.
* RAM is your system's short-term memory. Whenever your computer performs calculations, it temporarily stores the data in the RAM until it is needed.
* When you save a file, the data is written to the hard drive, which acts as long-term storage.
* The power supply unit in a computer converts the power from the wall outlet to the type of power needed by the computer


# Postgres Insert
* The PostgreSQL INSERT statement allows you to insert a new row into a table.
* First, specify the name of the table (table_name) that you want to insert data after the INSERT INTO keywords and a list of comma-separated columns (colum1, column2, ....)
* Second, supply a list of comma-separated values in a parentheses (value1, value2, ...) after the VALUES keyword. The columns and values in the column and value lists must be in the same order
* OID is an object identifier. PostgreSQL used the OID internally as a primary key for its system tables. Typically, the INSERT statement returns OID with value 0. The count is the number of rows that the INSERT statement inserted successfully
* INSERT statement also has an optional RETURNING clause that returns the information of the inserted row

# Postgres Select
* SELECT statement is one of the most complex statements in PostgreSQL. It has many clauses that you can use to form a flexible query
* Select distinct rows using DISTINCT operator.
* Sort rows usingORDER BY clause
* Filter rows using WHERE clause.
* Select a subset of rows from a table using LIMIT or FETCH clause.
* Group rows into groups using GROUP BY clause.
* Filter groups using HAVING clause.
* Join with other tables using joins such as INNER JOIN, LEFT JOIN, FULL OUTER JOIN, CROSS JOIN clauses

# Postgres Update
* The PostgreSQL UPDATE statement allows you to modify data in a table.
* First, specify the name of the table that you want to update data after the UPDATE keyword
* Second, specify columns and their new values after SET keyword. The columns that do not appear in the SET clause retain their original values.
* Third, determine which rows to update in the condition of the WHERE clause
* The WHERE clause is optional. If you omit the WHERE clause, the UPDATE statement will update all rows in the table
* When the UPDATE statement is executed successfully, it returns the following command tag count
* count is the number of rows updated including rows whose values did not change

# Postgres Delete
* The PostgreSQL DELETE statement allows you to delete one or more rows from a table
* First, specify the name of the table from which you want to delete data after the DELETE FROM keywords
* Second, use a condition in the WHERE clause to specify which rows from the table to delete
* WHERE clause is optional. If you omit the WHERE clause, the DELETE statement will delete all rows in the table
* DELETE statement returns the number of rows deleted. It returns zero if the DELETE statement did not delete any row
* asterisk (*) allows you to return all columns of the deleted row from the table_name