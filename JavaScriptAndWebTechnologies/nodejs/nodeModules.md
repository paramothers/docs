# Modules are three different types

1. file system based
2. core module
3. node\_module

# Module Name and their usages

**CORE**

1. **fs**,  to read\/write filesystem
2. **os**,  to work with operating system.
3. **Stream, **it provide API to create read\/write\/duplex\/transferable stream
4. **buffer**, it helps to work different data format.
5. **path**,  to get filesystem path handling
6. **q**,  a third party library provide Promises facility.
7. **util**,  set of utility functions including console global object.
8. **crypto**

**Async Programming**

1. **events**,  built in support for event emit and handling.
2. **async**, to load items in asynchronous manner. It helps developer to do async programming
3. **nimble**, to execute asyncrounous jobs in serial order.
4. **request**, is simplified HTTP Client.

**Debugging**

1. **node-inspector**,  for easy debugging

**NET\/TCP**

1. **net**,   providing TCP server and client
2. **url**,   to parse URL and query string
3. **socket-io**, it is **web socket** protocol implementation for node js.
4. **dgram** , provide UDP protocol support

# Authentication and Security

1. **jsonwebtoken**,
2. **passport**,
3. **passport-local**
4. **passport-bearer**
5. **passport-http-bearer**
6. **passport-oauth2**

# MiddleWare

1. **connect** ,it is framework, to keep a set of middle ware component for web application  
2. **express** ,it is middleware for web sites
3. **express-session** , need to have large set of information in user's session
4. **morgan** , middleware for logging\/debugging
5. **bunyan** , middleware for logging\/debugging use of concept stream
6. **domain** , middleware for logging\/debugging use of concept stream

# WEB\/HTTP

1. **http** , provide http server functionality
2. **router**, for routing http request
3. **body-parser**,  to parse form data\/requst to string to JSON object.
4. **querystring**,   to parse qurery string.used as body
5. **mime** , to extract mime type from file extension
6. **serve-static** , to server static files like css, images, js and etc.  
7. **serve-index**,  to server a directory content.
8. **cookie-parser**, to parse cookie from requesst and parse into JSON object.
9. **https** , TSL\/SSL support along with Http protocol.
10. **cookie-session**, to parse cookie from requesst and parse into JSON object.
11. **htmlparser**, to convert RSS feed into javascript construct..
12. **formidable**, to handle the multipart request.

**Web View**

1. **ejs**, expres template engine for views.

**DATABASE**

1. **mysql**, mysql driver for node js
2. **Levlel**, it is from Goolge
3. **db-oracle**, oracle driver for node js
4. **pg**, postgresql driver for node js

5. **mongodb**, used to connect mongodb from node.js

6. **mongoose**, an abstraction on top of mongodb driver from node.js

7. **connect-mongo**, use to store the user's http-SESSION information in mongodb

8. **redis**, redis driver for node js \(NoSQL\)

9. **connect**redis\_\_, redis driver for node js \(NoSQL\)

10. **hiredis**, alternative speed up library for redis database for node js \(NoSQL\)


## Utility

1. chalk
2. prettyjson

## **Testing**

1. **assert**, for supporting unit-test cases.
2. **chai**, provide additional assertions. it is like "assertThat" for junit.
3. **chai-datetime**, provide additional assertions.
4. **mocha**, a unit-test framework for javascript.
5. **sinon, **it is mocking framework for javascript.
6. **Karma**, is test runner like Junit
7. **Jasmine**, - used to write test cases for Angular JS
8. **Protractor **- used to write integration test for Angular JS
9. **Wows,** used to write test case for Node JS application

### JavaScript code coverage modules

1. instanbul

2. jscoverage


### Workflow

1. grunt-cli

2. grunt-contrib-sass \/ grunt-sass

3. node-sass

## **Deployment**

1. **forever**, used to keep server up always, irrepsective of error
2. **cluster**, to run the node.js in muilticore processor
3. **UpStart**, to run the node.js , it is advanced than **forever**
4. **ngen**, to build our own custom module for npm repository.

