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

### The Below JavaScript's Constructs  are good candidate for Node js

1. **First Class Function** - a anonymouse function can be assigned to a variable

2. **Immediate execute function**, it create new variable scope

3. **Closure **- inner function, which bound the variables declared in outer function.

4. **Higher Order function** - a function accept another function as argument

5. **Object Literal** -  easy to define arbitary properties

6. **Module Reveal Pattern** -  return a object from a method. for each call. So it every returned instance will own copy of methods and properties. _**it  occupy memory like anything**_

7. **Prototype**, using prototype, all instance can share a method definition. \(similar in java -static methods\)

8. Generally** Function **is powerful in javascript than any other lanugages.

9. 

`The Node.js platform allows developers to easily separate code. So there are many modules are there. most of time, as a developer has to orchestrate appropriate module for complete a project`

### V8 engine

* it is easy to integrate with other projects

* it is platform independent

* To do compiling and executing of javascript.

* Also do memory management

* it has one fast GC garbage collector

* it has one built-in profiler

* it compile source code directly to machine\/binary code. Not to any byte code like java compiler.


**Node.js is ALSO platform for WEB application development**

1. Web server need to single thread based request handling
2. I\/O event based programming for large **data **intensive project
3. Javascript best for `first-class function`, `closure`
4. CommonJS add module scope in javascript

5. Node takes javascript to server side programming and  Browsers takes javascript to client


### Environment Variable

* NODE\_PATH, & NODE\_MODULES enviornment variables location searched when module require
* NODE\_ENV, used by express

## Module supports frameworks

1. AMD

2. CommonJS, realeased on 2009, provide file based module system on server. node js use this module


### Module types

1. file module

2. core module
3. external node\_modules

# Important Topic

1. require - for module construct
2. npm -  for package manager
3. package.json for easy management of package dependency
4. Routing Http Request
5. ​V8 + libuv
6. Profiling, is act of performance analysis.

