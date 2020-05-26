In this step, you will learn how to insert documents

To work on a specifc database, you use the `use DATABASE_NAME` command.

We will work on `mydb` database. Type `use mydb`{{execute}} to switch to `mydb` database.

To check the current database, type `db`{{execute}}. Before we continue, make sure you are indeed using `mydb`. 

### CREATING A COLLECTION

If the collection does not currently exist, insert operations will create the collection.

### Insert a Single Document

`db.collection.insertOne()` inserts a single document into a collection.

The following example inserts a new document into the inventory collection. If the document does not specify an _id field, MongoDB adds the _id field with an ObjectId value to the new document. 

`db.inventory.insertOne(
   { item: "canvas", qty: 100, tags: ["cotton"], size: { h: 28, w: 35.5, uom: "cm" } }
)`{{execute}}

`insertOne()` returns a document that includes the newly inserted document’s _id field value.

To retrieve the document that you just inserted, query the collection:

`db.inventory.find( { item: "canvas" } )`{{execute}}

### Insert Multiple Documents

`db.collection.insertMany()` can insert multiple documents into a collection. Pass an array of documents to the method.

The following example inserts three new documents into the inventory collection. If the documents do not specify an _id field, MongoDB adds the _id field with an ObjectId value to each document. 

`db.inventory.insertMany([
   { item: "journal", qty: 25, tags: ["blank", "red"], size: { h: 14, w: 21, uom: "cm" } },
   { item: "mat", qty: 85, tags: ["gray"], size: { h: 27.9, w: 35.5, uom: "cm" } },
   { item: "mousepad", qty: 25, tags: ["gel", "blue"], size: { h: 19, w: 22.85, uom: "cm" } }
])`{{execute}}

`insertMany()` returns a document that includes the newly inserted documents _id field values.

To retrieve the inserted documents, query the collection:

`db.inventory.find( {} )`{{execute}}
