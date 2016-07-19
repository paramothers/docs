
+ we use/define services for handling business logic.
+ Services are defined/registered with $provide object, **5 different ways**

    1. **values**, not available during configuration phase but application can change the value
    1. **constant**, available during configuration phase, but application cannot modify the value
    1. **service**, normal services like java services, instance created by Constructor Function so facility to use THIS word, equivalent to "new" operator.
    1. **factory**, RMP (Revealing Module Pattern) need to be returned
    1. **provider**, configurable services, but complex, for example a service used by many applications, but we want to configure its behaviour different for each application   .

Once service defined in anyone of the way, it available for across application also it can be injected anywhere.
Services are **singleton** object and it can be used by controller, directives, filters and even other services.

**built-in services** 

 1. **$provide**, all the services are registered in this object, in a project.
 2. **$injector**, it inject the requested service instance from factory to application component.
 3. **$http**, communicate to server by AJAX.
 4. **$route**, combine url with view and controller, in SPA
 5. **$httpProvider** to define interceptors
 6. **$routeProvider**, provide _when_ function to define routing
 7. **$routeParams**, provide access the parameter inside of controller
 8. **$location**, service used to navigate within SPA application, it is like <jsp:forward> to another JSP
 1. **$locationProvider**, to enable html5 mode to disable prepend \# in template url.
 9. **$window**, service used to navigate outside of the application
10. **$log**, used to custom log
11. **$logProvider**, used to configure the log
13. **$q** used for deferred/promise objects
14. **$apply** notify the _digest cycle_ manually or _keypressdownevent_.(helps in two-way binding)

15. **timeout**, service used after certain time elapsed
16. **$watch** has list of expressions for a given $scope.(helps in two-way binding)

17. **$compile**, used for compile directives in html
18. **$httpBackend**, used to mock _$http_ service during testing the application
19. **$digest**, it is a service, to control or communicate digest cycle (dirty checking loop)
20. **$boradcast**, to communicate the info from $share without passing it as argument, send event from top to bottom $scope objects hierarchy.
21. **$emit**, send event from child $scope to parent ($rootScope)
22. **$on**, register for a particular event on a $scope objects.
23. **$interval**, it call a specific function at specified interval. it is wrapper of *window.interval*
24. **$resource** - communicate server via RESTful method.


