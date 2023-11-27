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

"__dirname" is used to signify where the file that runs the script is running from.     

# the api only understands json so we send data in json format to the api and when we recieve data we need to parse it for javscript to understand it.