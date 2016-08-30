

#  Modules are three different types

   1. file system based
   2. core module
   3. node_module


# Module Name and their usage

**CORE**

1. __fs__,  to read/write filesystem
2. __os__,  to work with operating system.
3. __path__,  to get filesystem path handling
4. __q__,  a third party library provide Promises facility.
5. __util__,  set of utility functions including console global object.
5. __crypto__

**Async Programming**

1. __events__,  built in support for event emit and handling.
2. __async__, to load items in asynchronous manner.
3. __nimble__, to execute asyncrounous jobs in serial order.
4. __request__, is simplified HTTP Client.

**Debugging**

1. __node-inspector__,  for easy debugging

**Testing**

1. __assert__,  for supporting unit-test cases.
2. __chai__,  provide additional assertions.
3. __chai-datetime__,  provide additional assertions.
4. __mocha__,  a unit-test framework for javascript.

**NET/TCP**

1. __net__,   providing TCP server and client
2. __url__,   to parse URL and query string
3. __socket-io__, it is web socket protocol implementation for node js.
4. __dgram__ , provide UDP protocol support

#Authentication and Security
1. __jsonwebtoken__,
1. __passport__,
1. __passport-local__
1. __passport-bearer__
1. __passport-http-bearer__

**WEB/HTTP**  

1. __http__ , provide http server functionality
2. **router**, for routing http request
8. __body-parser__,  to parse form data/requst to string to JSON object.
4. __querystring__,   to parse qurery string.used as body
5. __mime__ , to extract mime type from file extension
6. __serve-static__ , to server static files like css, images, js and etc.
7. __serve-index__,  to server a directory content.
9. __cookie-parser__, to parse cookie from requesst and parse into JSON object.
3. __https__ , TSL/SSL support along with Http protocol.
10. __cookie-session__, to parse cookie from requesst and parse into JSON object.
11. __htmlparser__, to convert RSS feed into javascript construct..
12. __formidable__, to handle the multipart request.
13. __connect__ ,it is framework, to keep a set of middle ware component for web application  

**Web frameworks**

1. __express__ ,it is middleware for web sites
2. __express-session__ , need to have large set of information in user's session

**Web View**

1. __ejs__, expres template engine for views.

**DATABASE**  

1. __mysql__, mysql driver for node js
2. __db-oracle__, oracle driver for node js
3. __pg__, postgresql driver for node js

4. __mongodb__, used to connect mongodb from node.js
5. __mongoose__, an abstraction on top of mongodb driver from node.js
6. __connect-mongo__, use to store the user's http-SESSION information in mongodb
7. __redis__, redis driver for node js (NoSQL)
8. __connect__redis__, redis driver for node js (NoSQL)
9. __hiredis__, alternative speed up library for redis database for node js (NoSQL)

**Deployment**

1. __forever__, used to keep server up always, irrepsective of error
2. __cluster__, to run the node.js in muilticore processor
3. __UpStart__, to run the node.js , it is advanced than __forever__
4. __ngen__, to build our own custom module for npm repository.

## Utility

1. chalk
