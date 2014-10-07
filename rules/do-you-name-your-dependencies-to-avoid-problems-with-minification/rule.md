---
type: rule
title: Do you name your dependencies to avoid problems with minification?
uri: do-you-name-your-dependencies-to-avoid-problems-with-minification
created: 2014-10-07T14:42:09.0000000Z
authors:
- id: 37
  title: Ben Cull

---

 Angular uses parameter names to determine which dependencies to inject. When you minify your angular code, the parameter names are changed, so you must name your dependencies to ensure they work correctly. 

The standard way to inject your dependencies looks a little like the following. We're defining a controller in this case.


```
phonecatApp.controller('PhoneListCtrl', function ($scope, $http) {...}​
```






ct.




You can fix this in two ways. The first one uses the $inject property to identify the name of the parameters in order:



```
function PhoneListCtrl($scope, $http) {...}
PhoneListCtrl.$inject = ['$scope', '$http'];
phonecatApp.controller('PhoneListCtrl', PhoneListCtrl);​
```




The second and preferred option is to pass an array containing the names, followed by the function itself. Take a look:



```
phonecatApp.controller('PhoneListCtrl', ['$scope', '$http', function($scope, $http) {...}]);​
```

​


Using this method will ensure you don't run into problems with minification. If you'd like to read more, check out the [Angular tutorial for ​Dependency Injection​](https&#58;//docs.angularjs.org/tutorial/step_05).​​

