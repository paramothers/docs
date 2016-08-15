# Developer tips

## controller and View

1. keep **$controller** size as much as minimum / lightweight
2. Use controller-as syntx in view, to easy from where a variable is coming either from controller itself or from $scope. controller-as variable is defined in current $scope and $scope itself has inheritance hierarchy with $rootScope. So it helps we no need to pass $scope object as parameter to controller function itself. we would access using "this" itself.
3. dont write any even simple logic in view
4. Controller, should not know each other and also its view it controlling.
5. in **ng-model**, use dot notation like user.name, user.password rather than simply name and password, it decouples view and controller by avoiding use of $scope

## $scope

1. treat **$scope** object as read only in view, write only in controller as much as possible.
2. pass **$scope** object as parameter in controller function rather than read directly from $scope
3. Don't pass **$scope** object beyond controller, like to services
8. attach minimum properties and function to **$scope** object. it should be lightweight
4. don't use **$scope** to keep all the variables unless, it shared with view. you can use local variable instead of.
5. Better read directly from **$scope**, object in View
6. use **$rootScope**, for share global variable with in the module, since it is super most $scope object in AngularJS
7. better access **$rootScope** object by module's _run_ method

## others

1. to avoid minify error, use inline array in all service, controller methods
2. Model objects should be sourced from services rather than controller itself.
3. Manipulation of any DOM, should be through link function of directive

## Directives ##

1. create custom directives to populate application wide domain. for ex. list of users account display many page

