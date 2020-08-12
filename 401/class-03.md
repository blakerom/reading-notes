# Data Modeling and NoSQL Database

### Reading, Research, and Discussion
    Why would a developer choose to make data models?
    Primarily to Ensure all data objects required by the database are accurate, Helps the developers at the conceptual, and logical level. Helps to define relational tables, keys, and stored procedures.
    
    What purpose do CRUD operations serve?
    They are the four basic functions of persistent storage
    
    What kind of database is Postgres? What kind of database is MongoDB?
    Postgres is an open-source relational database. MongoDB is a cross-platform document-oriented database.
    
    What is Mongoose and why do we need it?
    Mongoose is a MongoDB object modeling tool designed asynchronously. Supports promises and callbacks.
    
    Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.
    An application with users, products, and a shopping cart. Each user will have a similar product list or can vary by user, the product list updates the cart when selected, the cart finalizes information. All pieces of information are cascaded and update by the thing proceeding it.
    

### Term                              ### Definition

database                          Collection of data.
data model                        Conceptual representation of data objects adn their associations.
CRUD                              Create, Read, Update, Delete the four basic operations for persitent data.
schema                            Structured or organized data.
sanitize                          Removing all dangerous characters from an input or stringbefore passing it to SQL
Structured Query Language (SQL)   Relational database driven by structure of available data.
Non SQL (NoSQL)                   Application specific queries.
MongoDB                           Cross-platform document-oriented database.
Mongoose                          Database object modeling tool that runs async.
record                            Data structure that can hold data items of different kinds.
document                          Stored procedures used for explanation of tables and data.
Object Relation Mapping (ORM)     Writing of queries in our language of choice to communicate with queries.

### Resources
https://www.guru99.com/data-modelling-conceptual-logical.html
https://www.sqlshack.com/crud-operations-in-sql-server/
https://www.npmjs.com/package/mongoose
https://www.quora.com/What-exactly-is-data-sanitization-with-respect-to-SQL-injection
https://www.tutorialspoint.com/plsql/plsql_records.htm
https://blog.bitsrc.io/what-is-an-orm-and-why-you-should-use-it-b2b6f75f5e2a

