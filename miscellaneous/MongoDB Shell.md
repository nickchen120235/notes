# MongoDB

## shell
### Create
#### Database
Directly using <code>use</code> commands to a non-exist database will create a new one.
>Example: <code>use newdbname</code> will create a new database **newdbname** is it does not exist.

#### Collection
Directly using <code>insert</code> commands to a non-exist collection will create a new one.
>Example: <code>db.newcollection.insertOne({"aaa": 1})</code> will create a new collection **newCollection** if it does not exist.

### Insert
#### db.collectionname.insertOne(document)
>Example: <code>db.newCollection.insertOne({"aaa": 1})</code> will insert **{"aaa": 1}** to collection **newCollection** under current database.