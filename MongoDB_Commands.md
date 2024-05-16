for checking-> version/start 

**1-> mongosh**

* cls -> for cleaning
* show database -> It gives all database / shortcut -> show dbs
* use admin ->  change tha database

### to create a new database

use newdb

===================

* 1-> db.createCollection("students");
* 2-> show collections
* 3-> db.students.renameCollection("students_new");
* 4-> db.students.remove({});
* 4-> db.students_new.drop();


  *Drop pure collection koh hi remove kar deta hai*


  * db.students.insertOne(user);
  * db.students.insertMany([{name : "Rahul" , IP: '121.23.45.96'}, {name : "Chahar", hobby : " "singing"}]);
  * db.students.find();
  * db.students.find({name : 'Rahul'});
  * db.students.find({name : /R.*/});    --> Regular Expression 
  * db.students.find().limit(2);  ---> sirf 2 document show hougye
  * db.students.find().pretty();
  * db.students.find().skip(2);  ---> starting ke 2 doucment skip hou jaygye
  * db.students.find().sort({name : 1});  1 -> Ascending order , -1 -> Descending order
  * db.students.find().count();  --> total count of students
  * db.students.distinct('name');  ---> ise distinct name hi show houte/ List of all unique name

### retrieve distinct value
db.collection.distinct('name')

### Note: name is a field

### For nested fields we can use the following command
db.collection.distinct('comments.message')

### less than
db.collection.find({field: {$lt: 200}})

### less than or equal
db.collection.find({field: {$lte: 200}})

### greater than
db.collection.find({field: {$gt: 200}})

### greater than or equal
db.collection.find({field: {$gte: 200}})

### not equal
db.collection.find({field: {$ne : 'string is also accepted in some operators'}})

### in
db.collection.find((field: [1999, 2010,2019,2022]}})

### all
db.collection.find({field: {$all : [1999,2010]}})


### Updataion Queries
#### Update document
db.collection.update({field: 'value'}, {$set: {ohterField: 'new Value'}}, {upsert: true})

#### increment value
db.collection.updateOne((field: 'value'}, {$inc : {number: 6}})

#### push value to array
db.collection.updateOne({_id: 1}, {$push: {number: 6}})
##### push six into numbers where id is 1

## Deletion Queries
db.operate.deleteOne(

{ name : "Rahul" }

)

db.users.deleteMany({status: { $in: ["dormant", "inactive" ]}})
