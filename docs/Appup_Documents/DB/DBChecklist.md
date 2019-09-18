# Section 1 - Server Setup

## 1

```
Root User - For security reasons, the root MYSQL user must be setup with a secure password, and should only have
access from localhost. It is a bad idea to allow outside access to the root account. Create additional users if you need to
access the database remotely!
For security reasons, the root MYSQL user must be setup with a secure password, and should only have access from
localhost. It is a bad idea to allow outside access to the root account. Create additional users if you need to access the
database remotely! Y
```
## 2

```
Backup and Restore - Before allowing a database to be used in a production environment, there should be a usable backup
and restore process. I use the phrase “in case the database server is completely destroyed” because the backup location
and method needs to be completely independent from the database server. Note: Even a weekly database backup is better
than no backup at all. YY
```
## 3

```
Benchmarking - There’s no easy way to determine bottlenecks and trouble unless a method to benchmark performance is in
place. The slow query log should always be enabled, and it’s a good idea to install a benchmarking program. Monyog is an
external program that provides a number of real-time reports useful for monitoring and performance tuning. Y
```
## 4

## DNS

```
If you do not allow outside access, or you can access your server from known IP addresses, disabling DNS look-ups can
speed up server operations. Additionally, if the MySQL server loses it’s DNS look-up service, the usability of the entire
Database can all but halt. Y
```
## 5

```
Privileges
When adding users to a database, only give them the permissions that are absolutely required, and be specific in where
they can access from. “GRANT ALL ON EVERYTHING TO USER@ANYWHERE” is a really bad idea. If you do need to
give users full permissions for installations or another purpose, it’s a good practice to change them back to the minimum
once complete. Y
Docker for MySQL?
```
# Section 2 – Schema Design

## 1

```
Naming
A standardized naming scheme should always be used. The best practice is to use lowercase letters with an underscore
connecting names, such as `my_personal_database`. Tables, and individual column names should carry the same naming
convention. Use descriptive names for every column including id columns. `id` is not descriptive whereas `contact_id` is.
The columns should be refered in singular
```
```
Example
Table or View - contact, helptor_group
column - address, phone_number, note_description
constraints - pk_tablename for primary key constraints
fk_tablename_referencedtablename[_n] for foreign key constraints
uq_tablename_columnname[_columnname2...] or (uq_tablename_n) for unique constraints
ck_tablename_columnname[_columnname2...] (or ck_tablename_n) for check constraints
index - ix_tablename_n for non unique indexes
store procedures - sp_actionname Will not be redundant to have contact_id under contact table
```
## 2

```
Include a shortened version (3 letters) of the business domain or module name to start each table name so that it’s easier to
understand to which domain this data relates.
```
## 3

```
Collation vs Internalization
Use the same collation for all parts of the database, and avoid using UTF-8 or multi-byte formats unless you specifically
need them. Keeping the same format on all tables and columns can help prevent data corruption and conversion problems.
UTF-8 requires significantly more disk space and overhead which can reduce performance. If you need UTF-8, use it , but
don’t make your entire database UTF-8 because you’re lazy.
```
## 4

```
Foregin Keys Vs Plain Tables. Handle the relationship via programming. This will help DB engine to avoid one additional
step to ensure the constraints in place.
```
## 5

```
Logically Segmented Data in Tables
Tables should be segmented logically by the data they contain and their association with other tables. In this manner, there
may be more total tables, but will help eliminate tables with a huge number of columns which can really hurt performance.
Additionally, it will make querying easier as it’s unlikely that every column is needed for every query. This also allows for
Single-to-many relationships such as storing multiple addresses related to a single entry. Don’t be afraid of 20 tables with 20
columns each, be afraid of 1 table with 400 columns!
```

## 6

```
Reserved Words
Avoid using reserved words for any name in your database schema. Words like date, time, decimal, etc. are often used, and
can wreak havoc trying to get queries to work properly, and can cause even more difficulty in debugging. You can
technically use these words if they are placed in back-ticks (`date`), but this is a bad practice and should always be avoided.
```
# Section 3 – Table Design

## 1

```
Data types
MySQL has many data types, probably more than any other database. Using the correct data type for the data being stored
is one of the most important aspects in design. Failing at this step can break a database’s speed and the usability of an
application.
Whole Numbers – BIGINT, INT, MEDIUMINT, SMALLINT, TINYINT
Decimals – DECIMAL, FLOAT, DOUBLE, REAL
Dates – TIMESTAMP*, DATETIME, DATE, TIME, YEAR
Strings – CHAR, VARCHAR, BINARY, VARBINARY, BLOB, TEXT, ENUM, SET
Additionally, using the correct data type allows for the use of MySQL’s built-in functions which can sort, do math,
comparisons, date conversions, etc. For example, I often see dates stored in VARCHAR columns, which completely
prevents MySQL from sorting, or using any date related function.
```
## 2

```
Large Numerical Keys
It’s common for new programmers to use a BIGINT(20) when they need a key column. While admirable, this is a waste of
disk space. An UNSIGNED INT(10) has over 4 billion possible numbers, which is more than most will ever use. Even so, by
that time, you will want to look into partitioning, and will have a variety of other problems on your hand. Don’t use BIGINT’s
unless you need to store very-very large numbers.
```
## 3

```
Smallest Length
Using the smallest length data length is important. Every byte of savings adds up when a database’s size and usage goes
up. Lazy programming by using VARCHAR(255) or DECIMAL(20,2) creates unnecessary overhead and causes problems
down the road. Give yourself one extra byte of space if needed, but 100 is a overkill.
```
## 4

```
Avoid TEXT and BLOB Columns
TEXT and BLOB type columns can eat up a server’s resources when being selected. While these are most certainly needed
to store larger amounts of data, they should only be used for that purpose. VARCHAR can hold up to 255 bytes and should
always be used before TEXT whenever possible. Files should be saved in S3 and then a link put here.
```
## 5

```
Non‐Relational Storage
A huge design mistake is storing data in a non-relational format. It’s common to see data stored in a CSV format like
(value1,value2,value3) in a single column. This effectively bypasses MySQL’s ability to use the data. It’s best to use multiple
tables for single-to-many relationships, as this allows for MySQL to handle the data in an elegant manner. There are some
situations where storing csv-like data would make sense, but for all intensive purposes, avoid storing data like this. NoSQL in MySQL? JS Queries?
```
# Section 4 – Index Optimization

## 1

```
Use proper indexes
MySQL supports several types of indexes (PRIMARY, UNIQUE, NORMAL, PARTIAL, and FULLTEXT). It is important to
use the correct type of index for the job. It is also important to only use indexes when needed, and not to create duplicate
indexes. For example a primary key column already has an index, so adding a second UNIQUE INDEX on the primary key
is a complete waste of overhead and disk space.
```
## 2

```
Multi-Column Indexes
If there is a data set that is constantly queried with more than one column in the WHERE clause, it may be a good idea to
create a multi-column index. If you have an index on (`user_id`,`user_category`) the index will work when both are in the
where clause or the first column (`user_id`) is in the where clause. However, the index will not be used if only
`user_category` is in the where clause.
```
## 3

```
Modifying Indexed Fields During a Query
Unless you specify the length of an index, modifying an indexed column will prevent the index from being used.
For example, if there is an index on `credit_card_number` and you perform a query like this:
SELECT `user_id` FROM `my_table` WHERE LEFT(`credit_card_number`,4) = '5666';
The index will not be used. If this was a common scenario, you could create a partial index of (`credit_card_number`,4), and
the above query would use the index.
```
## 4

```
Indexes With a High Cardinality
Indexes work best when there are many unique values in relation to the total number of rows. This allows the database
engine to quickly reduce the number of possible rows in the result set. Indexes on columns with only a few unique values
are inefficient and will end up being a waste of overhead.
```

## 5

```
Unique and NULL Column Indexes
Allowing NULLS in index columns adds an additional byte of storage per row to the index. This again equates to a waste of
space and overhead and will slow down MySQL’s performance. It’s better to use no value rather than NULL.
```
# Section 5 – Query Optimization

## 1

```
Specific Column Names
Always use specific column names instead of * when querying a table. SELECT * is lazy programming. While it is
completely valid syntax, you won’t know the columns that will be returned. If you don’t know what you’re going to get with a
query, there’s no reason to use it.. right? Write out any column names that you need data from. This way your code is
intuitive, you won’t have problems trying to use data from a column that doesn’t exist, and the next person using your script
wont hate you.
```
## 2

```
MySQL’s Built-in Functions
MySQL has a variety of very advanced, and very fast, built-in functions. They probably are much more efficient than php or
most other application level scripts. These functions can greatly increase your application’s speed, and reduce its
complexity. MySQL has everything from mathematical operations, date comparisons, even spacial functions for calculation
geographic equations. Learn to use them.
```
## 3

```
Selecting TEXT and BLOB Columns
When a TEXT or BLOB column is select in a query, MySQL will create a temporary internal table. If large result sets are
selected with TEXT or BLOB columns, this can create a major load on the database, and unnecessary overhead. This
relates back to SELECT *, don’t select a TEXT or BLOB type column unless you actually need to use the data.
```
## 4

```
Use Transactions
Transactions are another great way of preventing incomplete or corrupted data while inserting or altering data. When using
a transaction, you can insert or alter any number of rows of data. If there is an error, all of the queries in the transaction will
be aborted. Think of inserting 50,000 rows into a report table, and having 10 arbitrary rows not insert correctly. That entire
set of data is now corrupt, and a transaction would have prevented that.
```
## 5

## SQL_NO_CACHE

```
SQL_NO_CACHE is a great way to prevent MySQL from caching a query’s result. This is important for results with a rapidly
changing data, or very large result sets. Both of these situations can eat up server resources without any gain to the
application or end-user.
```
# Miscellaneous

## 1

```
TIMESTAMP vs. DATETIME
TIMESTAMP and DATETIME store dates in the exact same format (YYYY-MM-DD HH:MM:SS) but TIMESTAMP uses less
space to do so. The only limitation is that TIMESTAMP cannot be used for dates older than Jan 1st, 1970.
```
## 2

## SIGNED INT

```
Unless you need to store negative numbers, only use UNSIGNED INT and other numerical data type fields. There’s no
reason to allow for negative numbers if they will never be used.
```
## 3

```
Collation: _ci vs. _cs
The _ci in a collation stands for “case insensitive”. If you care about case sensitivity use a collation that ends in _cs. The can
be very important for searching and other operations where John ≠ john!
```
## 4

```
All the not nullable and frequently used columns should be created to the left of the table. Most frequently nullable columns
should be created to the right of the table definition
5 Always do spell checks
```
```
JOIN Optimization
Use of Generics as much as possible
SQL Injection
Security to not delete the database
Order By, Group By optimizations
Limiting the results to 20 or max 100 always
```


