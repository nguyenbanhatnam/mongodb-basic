# MongoDB
## Script
- mongosh
- cls

## Show
- show dbs
- show collections
- db.dropDatabase()

## Create
- db.collectionName.insert()
- db.collectionName.insertOne()
- db.collectionName.insertMany([])

## Read
- db.collectionName.find({},{}).explain("executionStats")
- db.collectionName.find().sort({})
- db.collectionName.find().limit()

## Update
- db.collectionName.updateOne({},{$set:{}})
- db.collectionName.updateMany({},{$set:{}})

## Delete
- db.collectionName.deleteOne({})
- db.collectionName.deleteMany({})

## Indexs
- db.collectionName.createIndex({})
- db.collectionName.getIndexes()
- db.collectionName.dropIndex("")

## Collections
- use collectionName
- db.createCollection("",{capped:true, size:, max:}, {autoIndexId:false})
- db.collectionName.drop()
