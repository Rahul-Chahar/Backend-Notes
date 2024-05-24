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
