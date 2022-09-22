# Data Modeling

## nosql vs sql

<https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool>

**SQL**
Sql-SQL databases as either open-source or close-sourced from commercial vendors.

SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL.

SQL databases are good fit for the complex query intensive environment
-table based databases 
-databases have predefined schema 
-databases are vertically scalable
-Relational Databases
-databases uses SQL ( structured query language ) for defining and manipulating the data
-best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data.

**Nosql**
-non-relational or distributed database.
-databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.
-NoSQL databases have dynamic schema for unstructured data.
-horizontally scalable
-database, queries are focused on collection of documents
-database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb
-not good fit for complex queries.
-don’t have standard interfaces to perform complex queries
-highly preferred for large data set
-Support relies on community support, and only limited outside experts are available for you to setup and deploy your large scale NoSQL deployments.
-storing data as graph databases, key-value store databases, document store databases, column store database and XML databases.

**What type of database is the best fit for the complex query intensive environment?**

SQL databases are good fit for the complex query intensive environment.

**What type of database is the best fit for hierarchical data storage?**

NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.

**Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.**

SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server.
-vs-
NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.

## sql modeling techniques

<https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/>

**Among data tables, what is a one-to-many relationship and how do we “relate” them?**

An entry in one table that can be related to more than 1 entry in another tabe.
ex and employee in a department. There are likely many departments with many employees.

**Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.**

Model a diagram.

**Explain the difference between a primary and foreign key.**

Primary keys uniquely identify each row in a table.

Foreign key is a column or set of columns which match a primary key in another table.

## sql vs nosql

<https://www.youtube.com/watch?v=ZS_kXvOeQ5Y>

**How do we treat keywords and parameters differently in SQL syntax?**

SQL uses certain syntax keywords as SELECT,FROM
and parameters as id,name,price...products

ex SELECTid,name,priceFROMproducts

**Define normalization within the context of schemas and data.**

It is one of the rules in using SQL that all fields in the data table has to adhere to that each cell in the table contains only the type of data that it is structured to contain. No empty cells.

**Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.**

One-to-One
User table-Contact table

One-to-Many
User table-Product table-Orders table

## sequelize api

Documentation:<https://sequelize.org/master/>

Sequelize is a promise-based Node.js ORM tool for Postgres, MySQL, MariaDB, SQLite, Microsoft SQL Server, Amazon Redshift and Snowflake’s Data Cloud. It features solid transaction support, relations, eager and lazy loading, read replication and more.
const { Sequelize, Model, DataTypes } = require('sequelize');
const sequelize = new Sequelize('sqlite::memory:');

class User extends Model {}
User.init({
  username: DataTypes.STRING,
  birthday: DataTypes.DATE
}, { sequelize, modelName: 'user' });

(async () => {
  await sequelize.sync();
  const jane = await User.create({
    username: 'janedoe',
    birthday: new Date(1980, 6, 20)
  });
  console.log(jane.toJSON());
})();

<https://sequelize.org/master/>

// Callee is the model definition. This allows you to easily map a query to a predefined model

const projects = await sequelize.query('SELECT * FROM projects', {
  model: Projects,
  mapToModel: true // pass true here if you have any mapped fields
});
// Each element of `projects` is now an instance of Project

## Things I want to know more about

Finding more time in a day to look into all the great tools and have more time to practice the tools.
