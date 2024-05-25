# Rxpress 
It is a JS framework

***Note--> Node js is not a framework it is a Runtime Environment***

#### Creating an Express Server
* Create Directory.
* Create index.js file.
* Initalise NPM.
* Install the Express package.
* Write Server application in index.js
* Start server.

```
npm init --y
npm i express

type: "module"

Code
import express from "express";
const app = express();

app.listen(3000, () =>{
console.log("Server running on port 3000.");
})

2nd
import express from "express";
const app = express();
const port = 3000;

app.listen(port,() =>{
console.log('Server running on port ${port}.');
})
```
node index.js


#### Which ports are open ..... checking the command 
* Windows

netstat -ano|findstr "LISTENING"

* Mac/Linux

sudo lsof -i -P -n | grep LISTEN



### Request Vocab
* GET
  * Request Resources to a server
* PPST
  * Sending Resources to a server 
* PUT
  * Replace Resource
* PATCH
  * Patch up a Resource
* DELETE
  * Delete Resource 

## Making Requests
*Postman and making other HTTP requests*

#### HTTP return codes cheat sheet
*  1** Hold on
*  2** Here you go
*  3** Go away
*  4** You F*cked up
*  5** I F*cked up

#### GET
Retrieves information from the specified resource, and should only be used to request data (not modify it).

#### POST
Sends data to the server for processing, usually resulting in a change in the server state or side effects on the server.

#### PUT
Updates a current resource or creates it if it doesn't exist, with the client providing a complete and updated copy of the resource. 

#### PATCH
Updates parts of an existing resource, with the client providing only the parts of the resource that need to be updated. 

#### DELETE
Removes the specified resource from the server.

