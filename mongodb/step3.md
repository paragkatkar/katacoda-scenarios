In this step you will start the MongoDB server

## Start the MongoDB server

The default settings for _datafiles_ is _/data/db_. You can specify an alternate path for _datafiles_ using the _--dbpath_ option as show below. Run the below command to start the server with the _--dbpath_ and _--logpath_ overrides 

`./mongod --dbpath ~/data/db --logpath ~/data/mongod.log --fork`{{execute}}