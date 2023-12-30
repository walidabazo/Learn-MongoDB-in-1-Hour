# Learn-MongoDB-in-1-Hour
Like any other database management language, MongoDB is based on a NoSQL database that is used for storing data in a key-value pair. Its work is based on the concept of document and collection. It is also an open-source, document-oriented, cross-platform database system that is written using C++. 

[![Watch the video](https://img.youtube.com/vi/iLcJZ1QdE-E/0.jpg)](https://youtu.be/iLcJZ1QdE-E)

# what main Collections ?
Collections can be defined as a cluster of MongoDB documents that exist within a single database. You can relate this to that of a table in a relational database management system. MongoDB collections do not implement the concept of schema. Documents that have collections usually contain different fields. Typically, all the documents residing within a collection are meant for a comparable or related purpose.

# what main document?
A document can be defined as a collection of key-value pairs that contain dynamic schema. Dynamic schema is something that documents of equal collection do not require for having the same collection of fields or construction, and a common field is capable of holding various types of data.

# Learning 

## MongoDB tutorial for beginners
        - MongoDB Overview
        - MongoDB installation 
        - MongoShell installation
        - Set Environment variable PATH
        - VSCode with Mongosh
        - Database creation and drop

## insert
         db.staff.insertOne(
         {
          name:"walid",
          age:40,
          Fulltime:false,
          ReguisterDate:new Date(),
          BirthDate:New Date(1984-8-2),
          Corses:["ASP.NET","C#","MS SQl server"],
          Address{street:"4 st.",City:"cairo",zipcode:123456}
          })
## data types
## Sorting and limiting

        db.staff.find()
        db.staff.find().sort({name:1})
        db.staff.find().sort({name:-1})

        db.staff.find().sort({age:1})
        db.staff.find().sort({age:-1})

        db.staff.find().limit(1)
        db.staff.find().limit(3)

        db.staff.find().sort({age1}),limit(1)
        db.staff.find().sort({age:-1}),limit(1)
        
## find
        get all 
        db.staff.find() 

       db.staff.find({name: "adam"})
       db.staff.find({age: 25})
       db.staff.find({FullTime: false})

       .find({query},{Projection})

       db.staff.find({age: 40}, {FullTime: false})

       db.staff.find({}, {name: true})
       db.staff.find({}, {_id: false, name: true})
       db.staff.find({}, {_id: false, name: true, age: true})

## update
      db.staff.find()
       - updateOne()
      db.staff.updateOne({name:"adam"}, {$set:{FullTime:true}})
      db.staff.updateOne({name:"adam"}, {$unset:{FullTime:""}})

      updateMany()
      db.staff.updateMany({}, {$set:{FullTime:true}})
      db.staff.updateMany({FullTime:{$exists:false}}, {$set:{FullTime:true}})
      
## Delete and import-export db
      db.staff.deleteOne({name:"adam"})
      db.staff.deleteMany({Fulltime:false})
      db.staff.deleteMany({RegisterDate:{$exists:false}})
      
## comparison operators
        $eq : Values are equal.
        $ne : Values are not equal.
        $lt : Value is less than another value.
        $lte : Value is less than or equal to another value.
        $gt : Value is greater than another value.
        $gte : Value is greater than or equal to another value.
        $in : Value is matched within an array.
        
## logical operators
       $and: Returns documents where both queries match
       $or: Returns documents where either query matches
       $nor: Returns documents where both queries fail to match
       $not: Returns documents where the query does not match
       
## indexes
## collections



