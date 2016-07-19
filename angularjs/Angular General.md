# History

+ 1990, HTML and HTTP are introduced for sharing data.
+ 1993, CGI programing was introduced, first in Perl and etc.. 
+ 1998, DOM convention create by w3 .. yes it happened at 98 only.
+ 2006, Google Chrome browser has released
+ 2009, Angular JS life started by Misko Hevery and Adam abrons
 
# Component of Angular JS

1. **Modules**, break up the application into several module. it is like in java we have jar files and reused accross 
   many projects. Once we have a module, possibly we can re-use in many UI projects
2. **config**, used to configure the application before to run and routing configuration, dynamically configure Services
3. **Controller**, handling UI events and manipulationg Model. **Sit between view and service**
4. **view**, HTML elements .
5. **Directives**, easy to extend HTML view and re use of component, manipulate DOM, form Validation.
6. **Services**, improved the application design,business logic, wrap third party libraries, cross-cutting functions, talking with external server, data sharing across controllers

# Selling/Selection factors

1. Dependency injection, so easy to unit testing any component ( not use "new" operator )
2. Directive, a reusable component access the applications
3. AngularJS's template is just HTML rather than any special one like FreeMaker, Velocity
4. Module and submodule based organization of application files
5. Layered architecture, to separate the concern like MVC
6. data handling for display by filters, expression and form validation using directives
7. two way data binding between model and view thats how avoid a lot of boiler plate code
8. **Compilation**, is the process, to traverse DOM tree by angular and looks for special kind of attribute/element
9. Use of Controller-as syntax to reduce direct use of $scope.
10. have many node.js based tool for dependency resolve, testing, delivery of application.
11. it protect the application against XSS using ng-bind-html
12. it provide support for html-fragmentation using ng-include
13. **view**, component are developed using already famliar technology that is HTML and CSS.
14. **distribution**, easy to distrubute the application using **Grunt/Gulp**

Angular JS Project organization
===============================

+ **inline style**, Good for simple poc
+ **Stereo Typed**, Good for small application, only one js file for each type of component
+ **Specific style**, For big application, one folder for each type. it is opposite to _Domain Model_
+ **Domain model**, For big application, one folder for each application's business-module. 

So, start in inline style --> Stereo type --> Domain Model