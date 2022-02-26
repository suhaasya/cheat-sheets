
# MongoDb commands

## Database commands

View all databases

```bash
  show dbs
```

Create a new or switch databases 

```bash
  use dbName
```

Delete database

```bash
  db.dropDatabase()
```

## Collection commands

Show Collections

```bash
  show Collections
```

Create a new collection 

```bash
  db.createCollection('collection name')
```

Drop/Delete a collection 

```bash
  db.collection-name.drop()
```

## Row/Document commands

Show all Rows in a Collection  

```bash
  db.comments.find()
```

Show all Rows in a Collection (Prettified)

```bash
  db.comments.find().pretty()
```

Find the first row matching the object

```bash
  db.comments.findOne({key:value})
```

Insert a row in Document

```bash
  db.comments.insert({
    key:value
 })
```

Insert many rows in Document

```bash
  db.comments.insert([{key:value},
  {key:value},
  {key:value}
  ])
```

Search in a MongoDb Database

```bash
  db.comments.find({key:value})
```

Less than 
```bash
  db.comments.find({key: {$lt: value}})
```

Less than equal to
```bash
  db.comments.find({key: {$lte: value}})
```

Greater than 
```bash
  db.comments.find({key: {$gt: value}})
```

Greater than equal to
```bash
  db.comments.find({key: {$gte: value}})
```

Limit the number of rows in output

```bash
  db.comments.find().limit(2)
```




Update a row

```bash
  db.comments.update({key: value},
{key:updated-value}, {upsert: true})
```

Mongodb Rename Operator

```bash
  db.comments.update({key:value},
{$rename:{
    key: newkey
}})
```

Delete Row 

```bash
  db.comments.remove({key:value})
```







    