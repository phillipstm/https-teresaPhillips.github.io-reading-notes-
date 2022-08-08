# Mongo and Mongoose

## nosql vs sql

<https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool>

**Five differnences between:**

**SQL**

-SQL databases are primarily called as Relational Databases (RDBMS)

-SQL databases are table based databases

-SQL databases have predefined schema

-SQL databases are vertically scalable.SQL databases are scaled by increasing the horse-power of the hardware.

-SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful.

-SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL.

**NoSQL**

-NoSQL database are primarily called as non-relational or distributed database.

-NoSQL databases are document based, key-value pairs, graph databases or wide-column stores.

-NoSQL databases have dynamic schema for unstructured data.

-NoSQL databases are horizontally scalable.NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.

-NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database.

-NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb

**What kind of data is a good fit for an SQL database?**

For the complex query intensive environment. 

**Give a real world example.**

For high transactional based application: SQL databases are best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data.

**What kind of data is a good fit a NoSQL database?**

NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.

**Give a real world example.**

NoSQL database are highly preferred for large data set (i.e for big data). 

**Which type of database is best for hierarchical data storage?**

NoSQL

**Which type of database is best for scalability?**

SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. 

## Videos

### sql vs nosql

<https://www.youtube.com/watch?v=ZS_kXvOeQ5Y>

**What does SQL stand for?**

Structured Query Language.

**What is a relational database?**

A database that works with assumptions.

**What type of structure does a relational database work with?**

It works with tables as data tables.

**What is a ‘schema’?**

A precise structure table with fields and id's. A record for value in the fields.

All data has to adhere to the schema.

**What is a NoSQL database?**

Mongo DB

**How does it work?**

You can have multiple documents in one field. And different types of data in the fields. It doesn't have to adhere to a strict schema. And no relations...kinda.

**What is inside of a Mongo database?**

Can easily be split accross multiple servers.
No or very few relations.
Data is generally merged or stored in very few collections.
Both horizontal and vertical scaling is possible.
Great preformance for mass read and write requests.

**Which is more flexible - SQL or MongoDB? and why.**

MongoDB, because it doesn't have a strict structure and you can add different types of data to your queries.

**What is the disadvantage of a NoSQL database?**

Less predictable outcomes. It can have a preformance issue if it is trying to work too hard. Vertical scaling has limits.

### Bookmark and Review

**mongoose api**<https://mongoosejs.com/docs/api.html#Model>

**React Router**<https://reactrouter.com/web/api/BrowserRouter>

## Things I want to know more about

How to determine which type of database is best for intended use.
