In this step, you will learn how to insert documents

To work on a specifc database, you use the `use DATABASE_NAME` command.

We will work on `mydb` database. Type `use mydb`{{execute}} to switch to `mydb` database.

To check the current database, type `db`{{execute}}. Before we continue, make sure you are indeed using `mydb`. 

Let's insert our first documents to a `users` collection. We don't need to create the collection in advance - it will be created as soon as we insert the first document.

To insert a document we use `db.collection_name.insert(document)`, where `document` is the JSON representing the object we would like to store.
For example:
`db.users.insert( {
			fname: "John",
			lname: "Doe",
			email: "john.doe@inrhythm.com",
			age: 42
		  });`{{execute}}