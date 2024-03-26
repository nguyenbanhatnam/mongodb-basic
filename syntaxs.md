mongosh
show dbs
use dbName
db.createCollection("dbName")
db.dropDatabase()
show collections
ISODate("2001-08-21")
db.collection.insert() insertOne if parameter have objectType or insertMany if parameter have array type 
db.collection.insertOne()
db.collection.insertMany()
field in document is snake case
db.collection.find({_id: ObjectId("")})
db.collection.find({city: {$in: ["A","B"]}})
db.collection.find({"field": {$gt: 50}})
$gt
$lt
$lte
$gte
db.collection.find("":{}) this normal find is $and this is absolute clause
db.collection.find("":{$elemMatch: {}}) this is include element or call this is filter or this is dependent clause
db.collection.find({$or: [{},{}]})
db.collection.find({$and: [{$or: [{},{}]},{$or: [{},{}]}]})
db.collection.replaceOne()
db.collection.updateOne({},{$set: {}},{upsert: true})
db.collection.updateOne({},{$push: {}})
db.collection.findAndModify({
    query: {}
    update: {$inc: {}}
    new: true
})

explain("executionStats")

db.collection.updateMany({},{$set: {}})

db.collection.deleteOne({})
db.collection.deleteMany({})

db.collection.find().sort()
db.collection.find().sort().limit()
db.collection.find({},{a:1,_id:0})

db.collection.countDocuments() == db.collection.countDocuments({})
db.collection.estimatedDocumentCount() this cant add filter

db.collection.aggregate(
    [
        {$match: {customer: {$in: ["Mike", "Karen"]}}},
        {$group: {_id: "$customer", total: {$sum: "$total"}}},
        {$sort: {total: -1}},
        {$out: 'newCollection'}
    ]
)

db.collection.aggregate([
    {
        $stage1: {
            { expression1 },
            { expression2 }...
        },
        $stage2: {
            { expression1 }...
        }
    }
])

Index
single field
compound
multikey indexes operate on an array field

db.collection.createIndex({},{unique: true}})
db.collection.getIndexes()
db.customers.explain().find({
  birthdate: {
    $gte:ISODate("1977-01-01")
    },
  active:true
  },
  {name:1,
    birthdate:1, 
    _id:0
  }).sort({
    birthdate:-1,
    name:1
    })

db.collection.dropIndex()
db.collection.dropIndexes()
db.collection.hideIndex()

db.collection.distinct("")