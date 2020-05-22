In this step you will start a Monto shell

## Launch a Mongo shell

Then type the following to start the Mongo shell.

`./mongo`{{execute}}

Display available commands.

`help`{{execute}}

Display available databases.

`show dbs`{{execute}}

To use a particular database (lets say myappdb) we can type the following.

`use myappdb
db`{{execute}}

To create a collection and insert a document into it, run the below command

`db.users.insert({fname: 'Shyam', lname: 'Arjarapu'})`{{execute}}

To see all the collections with in the database, run the following command

`show collections`{{execute}}

To see the document we just created, run the following command

`db.users.find()`{{execute}}