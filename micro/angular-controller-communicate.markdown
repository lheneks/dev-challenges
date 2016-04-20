## Overview
Given the below HTML and JavaScript, how would you implement the communicate function to make Ctrl1 talk to Ctrl2, so that the input text gets passed and displayed on the page? 

Here's a [JSFiddle](http://jsfiddle.net/abdg8d5e/) you can fork to work in.

```HTML
<div>
    <div ng-controller="Ctrl1">
        <input type="text" ng-model="message" />
        <input type="button" value="Talk to Ctrl2" ng-click="communicate()" />
    </div>
    <div ng-controller="Ctrl2">{{message}}</div>
</div>
```

```JavaScript
var myApp = angular.module('myApp', []);


myApp.controller('Ctrl1', myController);

myController.$inject = ['$scope']

function myController($scope) {
    $scope.message = "set in ctrl1";
	
    $scope.communicate = function () {
		// implement talking to ctrl2
    }
};

myApp.controller('Ctrl2', myController2);

myController2.$inject = ['$scope']

function myController2($scope) {
    $scope.message = "set in ctrl2";
};
```