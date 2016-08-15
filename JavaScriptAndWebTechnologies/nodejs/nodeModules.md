

#  Modules are three different types
    
   1. file system based
   2. core module
   3. node_module

 
# Module Name and their usage 

**CORE**

1. __fs__,  to read/write filesystem 
1. __os__,  to work with operating system. 
1. __path__,  to get filesystem path handling 
1. __q__,  a third party library provide Promises facility. 
1. __util__,  set of utility functions including console global object. 

**Async Programming**

1. __events__,  built in support for event emit and handling.
1. __async__, to load items in asynchronous manner. 
1. __nimble__, to execute asyncrounous jobs in serial order. 
1. __request__, is simplified HTTP Client. 

**Debugging**

1. __node-inspector__,  for easy debugging

**Testing**

1. __assert__,  for supporting unit-test cases.
1. __chai__,  provide additional assertions.
1. __chai-datetime__,  provide additional assertions.
1. __mocha__,  a unit-test framework for javascript.

**NET/TCP**

1. __net__,   providing TCP server and client 
1. __url__,   to parse URL and query string
1. __socket-io__, it is web socket protocol implementation for node js.
1. __dgram__ , provide UDP protocol support 

**WEB/HTTP**  
 
1. __http__ , provide http server functionality 
1. __https__ , TSL/SSL support along with Http protocol.
1. __querystring__,   to parse qurery string.used as body
1. __mime__ , to extract mime type from file extension
1. __serve-static__ , to server static files like css, images, js and etc. 
1. __serve-index__,  to server a directory content. 
1. __body-parser__,  to parse form data/requst to string to JSON object. 
1. __cookie-parser__, to parse cookie from requesst and parse into JSON object. 
1. __cookie-session__, to parse cookie from requesst and parse into JSON object. 
1. __htmlparser__, to convert RSS feed into javascript construct.. 
1. __formidable__, to handle the multipart request. 
1. __connect__ ,it is framework, to keep a set of middle ware component for web application  

**Web frameworks**

1. __express__ ,it is middleware for web sites 
1. __express-session__ , need to have large set of information in user's session

**Web View**

1. __ejs__, expres template engine for views.

**DATABASE**  

1. __mysql__, mysql driver for node js
1. __db-oracle__, oracle driver for node js
1. __pg__, postgresql driver for node js

1. __mongodb__, used to connect mongodb from node.js
1. __mongoose__, an abstraction on top of mongodb driver from node.js
1. __connect-mongo__, use to store the user's http-SESSION information in mongodb
1. __redis__, redis driver for node js (NoSQL)
1. __connect__redis__, redis driver for node js (NoSQL)
1. __hiredis__, alternative speed up library for redis database for node js (NoSQL)

**Deployment**

1. __forever__, used to keep server up always, irrepsective of error
1. __cluster__, to run the node.js in muilticore processor
1. __UpStart__, to run the node.js , it is advanced than __forever__
1. __ngen__, to build our own custom module for npm repository.