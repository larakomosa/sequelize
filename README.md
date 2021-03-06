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

## Database
The database connection is asynchronous, but Nest makes this process completely invisible for the end-user. The CATS_REPOSITORY provider is waiting for the db connection, and the CatsService is delayed until repository is ready to use. The entire application can start when each class is instantiated.

Nest is database agnostic, allowing you to easily integrate with any SQL or NoSQL database. You have a number of options available to you, depending on your preferences. At the most general level, connecting Nest to a database is simply a matter of loading an appropriate Node.js driver for the database, just as you would with Express or Fastify.

You can also directly use any general purpose Node.js database integration library or ORM, such as Sequelize (navigate to the Sequelize integration section), Knex.js (tutorial), TypeORM, and Prisma (recipe) , to operate at a higher level of abstraction.

For convenience, Nest provides tight integration with TypeORM and Sequelize out-of-the-box with the @nestjs/typeorm and @nestjs/sequelize packages respectively, which we'll cover in the current chapter, and Mongoose with @nestjs/mongoose, which is covered in this chapter. These integrations provide additional NestJS-specific features, such as model/repository injection, testability, and asynchronous configuration to make accessing your chosen database even easier.





