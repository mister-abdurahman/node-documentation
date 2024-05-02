# What is NodeJS & why use it?

node is a javascript runtime built on the v8 engine that makes it possible for us to run javascript outside of the browser.

# Some things we can now do with javascript on the node environment that we couldnt do on th ebrowser are : accesing the file system, better networking capabilities, all these advantages spice up a perfect condition for using node as a web server i.e using javascript on the server-side of web development.

repl stands for read.eval.print.loop

use "node" to enter the node repl and ".exit" or "ctrl+D" to exit the repl.
hit "tab" when in the node repl to see all the global variables available on node or to see all global variables on a particular variable like string, do "string.(hit tab)"

Done reading and writing files in nodejs ✅

# Blocking & Non bloking asynchronous nature of Nodejs

Synchronous code = blocking code 👎 (Node is single threaded)
Asynchronous code = non-blocking code 👍

A solution to callback hell is using Promises or async/await.

http module gives us networking capabilities

"\_\_dirname" is used to signify where the file that runs the script is running from.

# the api only understands json so we send data in json format to the api and when we recieve data we need to parse it for javscript to understand it.

In NodeJS, every file is treated as a module.
"module.exports" to export from a module.

# NPM

NPM is a software we use to manage all the 3rd party libarires we decide to use in our project

Watch Later:

# How the web works behind the scene

# How node works behind the scene

Never Block The Event Loop.!!!

# Asynchronous JS

# Restful API design

API should be stateless, server doesnt hve to remember previous data

Only return the data.length if its an array of data

53. Handling POST Requests
    middleware are fns that run between a req and res.

# Middleware and the req-res cycle

ex. parsing body, logging, setting headers, router...

NB:
the order of middleware in the stack is actually in the order it is written in the code.
routers are middlewares but are specific to certain urls/routes!

next() is used to run the next middleware in the stack. never forget to add next in your middleware !!.
router is usually the last middleware in the stack so we dont call the next in it.

Morgan is a 3rd party middleware that allows us see req data in console

# Param middleware:

param middleware runs when an assigned params is in the designated route path.

remember to always return any verification done in a middleware to avoid moving to the next function as the case may be

# Chaining multiple middleware functions:

Dont forget, all routes are essentially middlewares and nodejs is a single threaded program

# Serving static files:

to serve static files, use the express.static method and parse the route containing the file

# Environment variables:

nodejs env are located in "process.env", while express env are in app.get("env").

We use the dotenv package to configure env in the project. It works by adding the data in our dotenv file to nodejs environment variables.

# Configure eslint and prettier in your node app:

`npm i eslint prettier eslint-config-prettier eslint-plugin-prettier eslint-config-airbnb eslint-plugin-node eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react --save-dev`

don't forget eslint and prettier config files, also configure eslint using the eslint config file

# MongoDB:

Database => Collection (Tables) => Document (Rows)

MongoDB is stored in a data format like json but is called bson bcos it is "typed".

Embedding/Denormalization is the act of including similar data in a single document which allows for quick access and easier data models BUT SQL data tables are normalized.

current max size for each document is 16mb

# Mongoose:

is an Object Data Modeling library for mongodba nd nodejs providign a higher level of bstraction

NB: methods that are available on model.prototype (in the docs) are only accesible on an instance model document rather than on the model itself.

# Back-end Architecture:

We use MVC (most popular), one of the majo use of MVC is to separate business logic from application logic.
Keep application logic in controllers and keep business logic in model.

# Creating document:

use model.create and when using async/await use trycatch block too.

# Update document:

use patch to update, also: findByIdAndUpdate works best with patch method

# Delete document:

in a DELETE restful api, its a convention to not retun anything back

# Modelling:

trim only works on string and is used to remove whitespaces

NB: note that when you update your schema, the previously created model data recieves the default part of the updated schema.
