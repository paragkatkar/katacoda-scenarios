In this step you will learn the MongoDB concepts

# Database
A database is a set of collections (tables). Each databse is physically stored as files on the host filesystem. A single MongoDB instance can host multiple databases. It is equivalent to an RDBMS schema.
To see which databases currently exist type `show dbs`{{execute}}. By default you will see the `local` and `admin` databases. These are specal databases that we will not cover in this tutorial.


# Collection
Collection is a group of documents. It is the equivalent of an RDBMS table. A collection exists within a single database. Collections do not enforce a schema. Documents within a collection can have different fields. Typically, all documents in a collection are of similar or related purpose.

# Document
Entries in MongoDB are called documents, and are representeed by a JSON object,  These are equivelant to a row in a mysql table. 
Documents have dynamic schema which means that documents in the same collection do not need to have the same set of fields or structure. 