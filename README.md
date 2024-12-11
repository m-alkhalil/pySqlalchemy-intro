# pySqlalchemy-intro
Demo, and how to use sqlalchemy in python


To interact with Databases in python:
  - Row SQL queries
  - SQL Query Builder
  - ORM: Object-Relational Mapping

Sqlalchemy
  is a popular Python library used for interacting with databases, It provides both a high-level ORM (Object-Relational Mapping) and a low-level SQL expression language for querying and manipulating relational databases. SQLAlchemy is widely used because of its flexibility, scalability, and powerful features.

 Main Components of SQLAlchemy:
  1- Core (SQL Expression Language):
      The Core layer of SQLAlchemy provides a set of tools for building SQL queries using Python objects. This allows developers to interact with databases at a granular level         without relying on the ORM. The Core includes components like the Engine, Connection, and MetaData objects, which manage database connections and schema definitions,             respectively.
      SQLAlchemy’s Core allows for the construction of SQL queries in a Pythonic way, providing a bridge between Python code and the raw SQL syntax, with support for all SQL           constructs like SELECT, INSERT, UPDATE, and DELETE.
  
  2- ORM (Object-Relational Mapper):
      The ORM layer in SQLAlchemy abstracts the database tables into Python classes and provides an interface to query and manipulate database records as Python objects. 
      The ORM automates the translation between relational database rows and Python objects, reducing boilerplate code for CRUD operations.
      Developers define classes that represent tables in the database, and SQLAlchemy takes care of generating the corresponding SQL commands. Through the ORM, database rows are 
      returned as instances of Python classes, and modifications to these instances can be automatically reflected in the database.
  
  3- Session and Transactions:
      A central part of the ORM layer is the Session object, which serves as a staging area for all operations on objects that are mapped to the database. It is responsible for        tracking object states (new, dirty, deleted) and committing those changes to the database in a controlled and consistent manner.
      SQLAlchemy’s transaction management ensures that operations are executed in a way that maintains database integrity, supporting both explicit transactions and implicit     
      commit/rollback functionality.
  
  4- Query API:
      The Query API in SQLAlchemy is used to construct and execute database queries in a more Pythonic way. Through methods like .filter(), .join(), and .order_by(), developers 
      can construct SQL queries dynamically. SQLAlchemy translates these API calls into the corresponding SQL statements that can be executed against the database.
  
  5- Migrations with Alembic:
      SQLAlchemy is often used in conjunction with Alembic, a lightweight database migration tool for SQLAlchemy. Alembic helps manage database schema changes over time, 
      ensuring that updates to the schema can be applied in a controlled and versioned manner. This is especially important in production environments where schema changes need
      to be applied consistently across multiple instances of the database.
