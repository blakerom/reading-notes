# DM Normalization

Database Normalization is used to organize a database into tables and columns. By limiting a table to one purpose you reduce the amount of duplicate data. 

### Three Reasons for Database Normalization
- Minimize duplicate data
- Avoid data modification issues
- Simplify queries

Database tables should each have one purpose. Having more than one purpose can lead to data duplication.

![](https://www.essentialsql.com/wp-content/uploads/2014/06/Intro-Table-Not-Normalized.png)

Notice that office phone numbers are repeated. This can be normalized. Not normalizing data and creating duplication increases storage size thus decreasing performance.

First Normal Form - information is stored in a relational table with each column containing atomic values, no repeating groups or columns.

Second Normal Form - Table is in first normal form and columns depend on primary keys.

Thrid Normal Form - Table is in second normal form and columns are not transitively dependent on primary keys.

A primary key will point to the unique data, whereas foreign keys point to the primary key containing the data.

