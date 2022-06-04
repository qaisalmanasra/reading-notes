# **Sequelize**
## ***SQL vs NoSQL***
* SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database.
* SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.
* SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data.
## ***SQL Database Examples***
### `MySQL Community Edition`
#### MySQL database is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js.
### `MS-SQL Server Express Edition`
#### It is a powerful and user friendly database which has good stability, reliability and scalability with support from Microsoft.
### `Oracle Express Edition`
#### It is a limited edition of Oracle Enterprise Edition server with certain limitations. This database is free for development and deployment.
## ***NoSQL Database Examples***
### `MongoDB`
#### It is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema.
### `CouchDB`
#### It is also a document based NoSQL database. It stores data in form of JSON documents.
### `Redis`
#### It is another Open Source NoSQL database which is mainly used because of its lightening speed. It is written in ANSI C language.
## ***Data Modeling***
### `Data Modeling – Table Elements`
* The Table Name, which is located at the top of the table.
* The Primary Keys.  Remember the primary keys uniquely identify each row in a table.  A table typically has one primary key, but can have more.  When the key has more than one column, it is called a compound key.
* Table Columns – There can be one or more table columns.  To keep the diagrams simple, I don’t show the data types.  I may introduce those later when we focus on more comprehensive modeling.
* Foreign Key – This is a column or set of columns which match a primary key in another table.
### `Data Modeling – Table Relationships`
#### We connect lines between tables to show relationships.  In some cases an entry in one table can be related to more than one entry in another.  This is called a one-to-many relationship.
#### A many-to-one relationship is similar to a one-to-many relationship, this difference is in the point-of-view you take when naming the relationship.
### **[Reference](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)**
### **[Reference](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)**
### **[Bookmark](https://sequelize.org/docs/v6/)**