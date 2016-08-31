# Introduction

Node.JS is a platform, rather than language.

```
Node built on top of V8 as virtual machine (similar java uses JVM) + libuv => Non Blocking IO 
```

This Non-Blocking IO enables

1. access file system

2. access network

3. creating child process


**Node.js is ALSO platform for WEB application development**

1. Web server need to single thread based request handling
2. I\/O event based programming for large **data **intensive project
3. Javascript best for `first-class function`, `closure`
4. CommonJS add module scope in javascript



5. Node takes javascript to server side programming and  Browsers takes javascript to client

  REPL - read evaluate print loop


### Environment Variable

* NODE\_PATH, & NODE\_MODULES enviornment variables location searched when module require
* NODE\_ENV, used by express

# Important Topic

1. require - for module construct
2. npm -  for package manager
3. package.json for easy management of package dependency
4. Routing Http Request
5. ​V8 + libuv

