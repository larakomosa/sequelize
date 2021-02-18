## Sequelize
- Sequelize is a module that enables developers to work with relational data more easily

- npm install --save sequelize
- npm install --save pg pg-hstore # Postgres

#### Benefits
- You will write less code
- You will write more consistent code
- You can mostly avoid SQL queries
- It abstracts the db engine
- It does aa lot of things automaticallys
- Migrations

#### Disadvantages
- Complicated queries can be slow
- Additional learning curve
- Documentation isn't the best 
- Loss of flexibility

#### Connecting to Database
const { Sequelize } = require('sequelize');

// Option 1: Passing a connection URI
const sequelize = new Sequelize('sqlite::memory:') // Example for sqlite
const sequelize = new Sequelize('postgres://user:pass@example.com:5432/dbname') // Example for postgres

// Option 2: Passing parameters separately (sqlite)
const sequelize = new Sequelize({
  dialect: 'sqlite',
  storage: 'path/to/database.sqlite'
});

// Option 2: Passing parameters separately (other dialects)
const sequelize = new Sequelize('database', 'username', 'password', {
  host: 'localhost',
  dialect: /* one of 'mysql' | 'mariadb' | 'postgres' | 'mssql' 
});

## Object Impedancee Mismatch
- A set of conceptual and technical difficulties that are often encountered when a relational database management system (RDBMS) is being served by an application program (or multiple application programs) written in an object-oriented programming language or style, particularly because objects or class definitions must be mapped to database tables defined by a relational schema.

## Object Relational Mapper
- Object-relational mapping in computer science is a programming technique for converting data between incompatible type systems using object-oriented programming languages. This creates, in effect, a "virtual object database" that can be used from within the programming language. Wikipedia

#### Then/Catch
- Returns the result of a promise.  "Then for success and "catch" for error



