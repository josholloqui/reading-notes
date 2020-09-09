# PostgreSQL Joins
*  inner join, left join, right join, and full outer join.
* inner join examines each row in the first table (basket_a). It compares the value in the fruit_a column with the value in the fruit_b column of each row in the second table (basket_b)
* If these values are equal, the inner join creates a new row that contains columns from both tables and adds this new row the result set
* In the left join context, the first table is called the left table and the second table is called the right table.
* The left join starts selecting data from the left table. It compares values in the fruit_a column with the values in the fruit_b column in the basket_b table
* If these values are equal, the left join creates a new row that contains columns of both tables and adds this new row to the result set
* In case the values do not equal, the left join also creates a new row that contains columns from both tables and adds it to the result set. However, it fills the columns of the right table (basket_b) with null
* The right join is a reversed version of the left join
* The full outer join or full join returns a result set that contains all rows from both left and right tables, with the matching rows from both sides if available. In case there is no match, the columns of the table will be filled with NULL

# one-to-one
*  a one-to-one relationship is a type of cardinality that refers to the relationship between two entities
* A and B in which one element of A may only be linked to one element of B, and vice versa. In mathematical terms, there exists a bijective function from A to B
* a one-to-one relationship exists when one row in a table may be linked with only one row in another table and vice versa. It is important to note that a one-to-one relationship is not a property of the data, but rather of the relationship itself

# One-to-many
* A and B in which an element of A may be linked to many elements of B, but a member of B is linked to only one element of A
* a one-to-many relationship exists when one row in table A may be linked with many rows in table B, but one row in table B is linked to only one row in table A. It is important to note that a one-to-many relationship is not a property of the data, but rather of the relationship itself

# Many-to-many
* A and B in which A may contain a parent instance for which there are many children in B and vice versa.
* such relationships are usually implemented by means of an associative table (also known as join table, junction table or cross-reference table), say, AB with two one-to-many relationships A -> AB and B -> AB. In this case the logical primary key for AB is formed from the two foreign keys
* In web application frameworks such as CakePHP and Ruby on Rails, a many-to-many relationship between entity types represented by logical model database tables is sometimes referred to as a HasAndBelongsToMany (HABTM) relationship