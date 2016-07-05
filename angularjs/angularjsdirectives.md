
 + Directive can be either as element/attribute/class/comment 
 + Directives are case insenstive 
 + it extends HTML behaviour


## essential directives ##

1. **ng-app**, bootstrap and it define root of the Angular js application
2. **ng-controller**, to attach the controller with view, actually going to control the view
3. **ng-bind**, read data from controller to view (usually <span> element ) by $scope
1. **ng-bind-html**, display raw html, helps to avoid XSS. it comes from **angular-sanitize.js**
4. **ng-model**, take data from view to controller by $scope

## display-view directives##

1. **ng-view**, use with $route service to display the template in SPA
1. **ng-class**, dynamically apply a class with help of  *ng-model*
3. **ng-style**, it is better than *ng-class*, directly declare style property
2. **ng-options**, to populate <options> tags
1. **ng-include**, it include html fragment from another file like <JSP:include> directive


## control,looping directives##

1. **ng-repeat**, iterate  a array, objects
1. **ng-if**, it is similar to *ng-show*, but avoid rendering HTML Element itself. it save network band width
1. **ng-disabled**, disable a UI component, based on boolean expression
1. **ng-hide**, hide the element based on boolean value
1. **ng-show**, show the element based on boolean value

## Event handling directives##

 1. **ng-click**,  click event handler
 2. **ngBlur**, 
 3. **ngChange**, 
 4. **ngCopy**,
 5. **ngCut**, 
 6. **ngDblClick**,
 7. **ngFocus**,
 8. **ngKeyPress**, 
 9. **ngKeyDown**,
10. **ngKeyUp**,
11. **ngMousedown**, 
12. **ngMouseenter**,
13. **ngMouseleave**,
14. **ngMousemove**,
15. **ngMouseover**, 
16. **ngMouseup**, 
17. **ngPaste**.

## form validation directives ##

1. **ng-required**, enforce the a UI field is necessary
1. **ng-minlength**, enforce the minimum length of value
1. **ng-maxlength**, enforce the maximum length of value
1. **ng-pattern**, enforce the match with regular expression

# Filters ( work along with expression)

1. **currency**,  display currency of locale
1. **date**, display date 
1. **filter**, to filter out any data from an array
1. **json**, to display the java object as JSON
1. **limitTo**, to limit the display elements/characters
1. **lowercase**, to lowercase the characters
1. **uppercase**, to uppercase the characters
1. **number**, to display the numeric values
1. **orderBy**, order the elements in Array





  