---
layout: post
title:  "AngularJS Notes # 1"
date:   2017-04-06
---

Im learning AngularJS in order to make a single page website to make calculations.

You can create a `app.js` page and include a module `myapp`. This module will contain the different components of an AngularJS app.

{% highlight javascript %}
var app = angular.module("myApp", []);
{% endhighlight %}

Then in `index.html` we will add in the `<body>` tag `ng-app=myapp` this will tell AngularJS that the myapp module will live in the body element.

In `MainController.js` we created a new controller named `MainController` the controller will manage the data the app is creating.

{% highlight javascript %}
app.controller('MainController', ['$scope', function($scope) {
  $scope.title = 'Top Sellers in Books';
}]);
{% endhighlight %}

Then in the index.html we added `<div class="main" ng-controller="MainController">` this defines the controller scope, this will make the properties attached to scope to become available to use within `<div class="main">`.

Then utilizing `{{title}}` this is a an expression which is used to display values on a page.

Since the Scope has access to both the maincontroller and the index.html page we can use scope to communicate between the two, 
