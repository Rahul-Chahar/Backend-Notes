# MongoDB
* Document Oriented
* Stores Data in the forms of collections and documents
* Gained Popularity in the 2000s


**-> Mongo means Big/humongous**

### RDBMS ->
* MySql
* Oracle

***In ke kuch limitaitions they*** 

***RDMS ka sabse bada limitations tha ki ye tabhi work karta hai jab aapka ka Schema fix hai***


### RDBMS
* Database
* Tables
* Rows
* Columns

### MongoDB
* Database
* Collections
* Documents
* Fields

  *MongoDB mein tables koh Collections bolte hai Rows koh Documents or Columns koh Fields*

  ## Documents in MongoDB
  JSON type structure

  ## Collections in MongoDB
  Store Documents

  ### Advantages of MongoDB
  * Best of SQL and NoSQL
  * Open Source
  * Horizontally Scalable
  * Data Replication
  * Reliable
  * Flexible Scheme
 
### Use cases of MongoDB
* Product Data Management
* CMS  -> Content management system
* Operational Intelligence
* Online Application

### Sharding in MongoDB
Distributing data on multiple machines 

### How MongoDB Stores Data?
**Ans-> BSON**

Why BSON?

-> Because it helps in 

* Space
* Performance
* Jyda data type lata hai

***Note-> mongoDB mein ek document ka max storage 16mb houta hai***

*References -> It works like foreign keys*

### Relationship
* Embedded document
* References

#### Embedded document advantage
* 1-> Fast query because a single query can fetch me all the data
* 2-> Easy to create
* 3-> East to maintain trannsaction

### Challenges
* 1-> Too much embedding can exceed the 16MB limit
* 2-> Excess of data loaded each time -> eager loading   ( kyu ki data ek hi jagha pada hua hai toh saara data ek saath load houga magar hame sab ki jarurat thodi hai but phir bhi load pura data houga  ***Embedded mein document ke ander document houta hai***



### Referencing advantage
* 1-> Small documents ( toh kabhi bhi ham 16MB ki limit exceed nahi karegye)
* 2-> Lazy loading ( Load only that much data which is needed)


### Challenges
* 1-> Query could be slower
* 2-> Transaction becomes complex 


**Summary**

MongoDB -> DBMS -> NoSQL


### What is MongoDB?
MongoDB is an open-source, document-oriented NoSQL database management system.


*10gen company ne mongoDB koh banaya tha later on 10gen ka naam mongoDB hi hougya or phela version mongoDB ka 2012 mein aaya tha*




### Commands
* mongosh   ---> server start
* show dbs


***Note->> You won't see a database listed in the output of the show dbs command until that database contains at least one collection with data in it.***


#### Create database
* use students  (use (name))
* db.createCollection('data')

#### delete
db.data.drop()
db.dropDatabase()


### Inserting Documents in MongoDB
* db.data.insertOne({'name':'rahul',age:29})
* db.data.insertMany([{'name':vinod',age:29},{'name':'binamra',age:30},{'name':'arjun',age:30}])
* db.data.find()

#### Ordered and Unordered Inserts
* Ordered Inserts
The default behavior is ordered, where MongoDB stops on the first error.

isme jha bhi error ajeyga ouske baad se kuch bhi add nahi krega error se phele ka krega bss

eg-> db.<collection-name>.insertMany([doc1, doc2,...]);

* Unordered Inserts
When executing bulk write operations with an unordered flag, MongoDB processes after encountering an error.


isem error se phele or bhaad ka sab add kar lega 

eg-> db.<collection-name>.insertMany([doc1,doc2,...],{ordered:false});



### Read Operations in MongoDB
**Reading Documents in MongoDB**
* Comparison Operators
* Logical Operators
* Cursors in MongoDB
* Elements Operators

### Finding Documents in MongoDB
**find()**
* db.collection_name.find({key:value})

eg ->> db.data.find({'name':'vindo'})

**findOne()**
* db.collection_name.findOne({key:value})

eg->> db.data.findOne({'name':'vinod'})


# Importing JSON in MongoDB
* mongoimport jsonfile.json -d database_name -c collection_name
* mongoimport products.json -d shop -c products
* mongoimport products.json -d shop -c products --jsonArray

*Note--> Here, --jsonArray accepts the import of data expressed with multiple many documents withing a single JSON array.*

