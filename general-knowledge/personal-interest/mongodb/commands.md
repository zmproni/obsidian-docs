```js
show dbs            // Show all databases
use <database>      // Connect to database, create if doesnt exist
show collections    // Show collections in <database>
db.dropDatabase()   // Deletes database in use
cls                 // Clear screen
exit                // Exits terminal
```

```js
use appdb
db // Prints name of current databse connected to 
db.users.instertOne({name:"John"}) // Creates a record inside of a collection
```

Database
	Collections
		Document