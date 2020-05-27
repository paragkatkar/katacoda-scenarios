In this step, you will learn how to query documents

### Query Documents

This page provides examples of query operations using the db.`collection.find()` method in the mongo shell. The examples in this step use the inventory collection created in the previous step.

### Select All Documents in a Collection

To select all documents in the collection, pass an empty document as the query filter parameter to the find method. The query filter parameter determines the select criteria:

`db.inventory.find( {} )`{{execute}}

### Specify Equality Condition

To specify equality conditions, use `<field>:<value>` expressions in the query filter document

The following example selects from the inventory collection all documents where the status equals "D":

`db.inventory.find( { status: "D" } )`{{execute}}

### Specify Conditions Using Query Operators

A query filter document can use the query operators to specify conditions in the following form:

`{ <field1>: { <operator1>: <value1> }, ... }`

The following example retrieves all documents from the inventory collection where status equals either "A" or "D":

`db.inventory.find( { status: { $in: [ "A", "D" ] } } )`{{execute}}

### Specify AND Conditions

A compound query can specify conditions for more than one field in the collection’s documents. Implicitly, a logical AND conjunction connects the clauses of a compound query so that the query selects the documents in the collection that match all the conditions.

The following example retrieves all documents in the inventory collection where the status equals "A" and qty is less than ($lt) 30:

`db.inventory.find( { status: "A", qty: { $lt: 30 } } )`{{execute}}

### Specify OR Conditions

Using the $or operator, you can specify a compound query that joins each clause with a logical OR conjunction so that the query selects the documents in the collection that match at least one condition.

The following example retrieves all documents in the collection where the status equals "A" or qty is less than ($lt) 30:

`db.inventory.find( { $or: [ { status: "A" }, { qty: { $lt: 30 } } ] } )`{{execute}}

### Specify AND as well as OR Conditions

In the following example, the compound query document selects all documents in the collection where the status equals "A" and either qty is less than ($lt) 30 or item starts with the character p:

`db.inventory.find( {
     status: "A",
     $or: [ { qty: { $lt: 30 } }, { item: /^p/ } ]
} )`{{execute}}

