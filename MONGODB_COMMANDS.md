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
  db.collection-name.find()
```

Show all Rows in a Collection (Prettified)

```bash
  db.collection-name.find().pretty()
```

Find the first row matching the object

```bash
  db.collection-name.findOne({key:value})
```

Insert a row in Document

```bash
  db.collection-name.insert({
    key:value
 })
```

Insert many rows in Document

```bash
  db.collection-name.insert([{key:value},
  {key:value},
  {key:value}
  ])
```

Search in a MongoDb Database

```bash
  db.collection-name.find({key:value})
```

Less than

```bash
  db.collection-name.find({key: {$lt: value}})
```

Less than equal to

```bash
  db.collection-name.find({key: {$lte: value}})
```

Greater than

```bash
  db.collection-name.find({key: {$gt: value}})
```

Greater than equal to

```bash
  db.collection-name.find({key: {$gte: value}})
```

Limit the number of rows in output

```bash
  db.collection-name.find().limit(2)
```

Update a row

```bash
  db.collection-name.update({key: value},
{key:updated-value}, {upsert: true})
```

Mongodb Rename Operator

```bash
  db.collection-name.update({key:value},
{$rename:{
    key: newkey
}})
```

Delete Row

```bash
  db.collection-name.remove({key:value})
```
