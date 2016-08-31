# Introduction

Node.JS is a platform, rather than language.

```
Node built on top of V8 as virtual machine (similar java uses JVM) + libuv => Non Blocking IO 
```

This Non-Blocking IO enables

1. access file system

2. access network

3. creating child process


**Buffers**, - Add supports to deal Binary data in Node JS.
**Streams**, used as event interface to pass data around

### V8 engine 

* To do compiling and executing of javascript. 

* Also do memory management

* it has one fast GC garbage collector
* it has one built-in profiler
* it compile source code directly to machine\/binary code. Not to any byte code like java.

**Node.js is ALSO platform for WEB application development**

1. Web server need to single thread based request handling
2. I\/O event based programming for large **data **intensive project
3. Javascript best for `first-class function`, `closure`
4. CommonJS add module scope in javascript

5. Node takes javascript to server side programming and  Browsers takes javascript to client


### Environment Variable

* NODE\_PATH, & NODE\_MODULES enviornment variables location searched when module require
* NODE\_ENV, used by express

# Important Topic

1. require - for module construct
2. npm -  for package manager
3. package.json for easy management of package dependency
4. Routing Http Request
5. ​V8 + libuv
6. Profiling, is act of performance analysis.

