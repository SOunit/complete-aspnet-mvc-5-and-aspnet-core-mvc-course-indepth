# intro to Entity Framework

- mapping OOP model and DB table
- based on ADO.NET
- before EF, access db was error prone

# features

- modeling
  - create entity data model based on `POCO`
  - `POCO` - plain old CLR object
    - used to save data
    - used to query data
- querying
  - use Linq
- change tracking
- saving
- concurrency
  - optimistic concurrency by default
    - to protect overwriting from other user
- transaction
  - automatic transaction management
  - custom transaction management
- caching
  - repeat query return from cache, no database hitting

# Workflow

- DB
- Model class
  - saveChanges
    - create
    - update
    - delete
  - toList
    - fetch data
- Query / Non-Query
- EF
  - create SQL statement automatically
  - execute SQL statement
  - get Result Data (Data Reader)
  - convert data into object
- Memory
  - save object / collection temporary
- Presentation Logic
  - read / print data to User

# Architecture

- EDM / Entity Data Model

  - Conceptual Model
    - model class created by developer
  - Mapping
    - mapping `conceptual model` to `storage model`
  - Storage Model
    - store list of table / column
    - primary key

- LINQ to Entity

  - toList
  - Where
  - OrderBy
  - etc.

- Object Services

  - convert data into Objects / Collections
  - pass LINQ queries to EntityClient Data Provider

- Entity Client Data Provider

  - convert LINQ Query to SQL Query
  - pass data to Object services

- ADO.NET Data Provider

  - SqlConnection / OleDbConnection to execute SQL query

- Database

# Entity Framework

- Storage Model
  - database information
- Conceptual Model
  - created by developers
- Mapping
  - mapping storage(db) to conceptual model(oop model)

# DbContext

- class which have LINQ Queries
  - CRUD
- has collection of DbSet

# DbSet

- represents table
- 1 db to 1 DbSet
- offer functions

  - Where
  - OrderBy
  - etc.

- 1 database, 1 DbContext
- 1 table, 1 DbSet
