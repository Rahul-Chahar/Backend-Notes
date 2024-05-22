# Introduction To NPM
* NPM is a Node Package Manager for JavaScript programming language. You may have heard of tools such as Maven and Gradle for installing third-party libraries in Java
* Similarly, NMP is a package manager that can be used to install third-party/external node library
* It is the default package manager for the JavaScript runtime environment Node.js
* The registry is accessed via the client, and the available packages can be browsed and searched via the npm website. The package manager and registry are managed by npm, Inc
* NPM is included as a recommended feature in Node.js installer
* Whenever you install Node.js, NPM is included in it by default. You can verify it by running the command mentioned below

* npm -v   here v stands for version

#### NPM is the world's largest software library


# Commands
* node -v
* npm -v
* npm init



## What is NPM
* Many companies use NPM to manage private development
* Another package manager, like npm, that we can use to install third-party modules and external libraries is called YARN (Yet Another Resource Navigator) package manager

# YARN
* Yet Another Resource Navigator
* NPM is a prerequisite for installing YARN, and you need to use this command to install YARN
* npm install yarn -global
* YARN generates a 'yarn.lock' file.
* YARN add command logs are brief and much cleaner. They are ordered in the form of a tree. An image of it is attached on the next slide
* To install a package in YARN, we use the command given below





# NPM
* It is the default package manager
* You need not install npm; it is included in the Node.js installer
* The npm generates a package-json.lock file

# YARN
* Unlike npm, it is not the default package manager
* To install YARN, npm needs to be installed
* YARN generates a yarn.lock file

# MODULES, DEPENDENCIES AND PACKAGES
*Terms commonly used in Node.js:*

### Modules
are single or multiple files that contain code for a single concept, functionality or library

There are 3 types of Module

* Custom Module
* default Module
* External Module


### Dependencies 
are requirements that you need to use an API or a function that is part of an internal module then for that you need that module as a dependency

### Packages
are single modules or collections of multiple modules



### Server
***Never Stopping process***
```
const http = require('http');

const server = http.createServer((req, res) => {
    if(req.url == '/hello'){
        res.end('Hello World ! Welcome to the world of Node.js')
    } else{
        res.writeHead(404);
        res.end('Use the right URL')
    }
    })

    server.listen(3000,() => {
        console.log('Server is running on port 3000')
    })

```


# Event Loop Compoenets
call stack

Libuv 
* Macro Task Queue
  * -> Time Queue
  * -> I/O Queue
* Micro Task Queue
  * -> promise Queue
  * -> process.nextTick
 
***Micro Task Queue sabse phele execute houga ouske baad Macro Task Queue execute houga.***



# Modules 
Modules ek chhota function hai, ham ise import or export karte hai 

-> Module koh **export** karne ke liye

module.exports

-> Module koh **import** karne ke liye

require('')  keyword ka use karte hai


-> Modules example
* HTTP
* FS
* PATH
* OS


### Interview imp question
# How to make a server without using express 
Ans -> Using http module 

eg->
```
var http = require('http');

http.createServer(function(req, res){
res.writeHead(200,{"Content-type":'text/html'});
res.write("Hello World");
}).listen(5001,()=>{
console.log("Listening to port 5001")
})
```
