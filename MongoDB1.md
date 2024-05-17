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
