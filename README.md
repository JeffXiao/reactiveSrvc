# reactiveSrvc

An AngularJS based subscribe/broadcast service using reactive design pattern

In general, it is not efficient in terms of performance to use $rootSceop to send and receive message, such as:
  $rootScope.$emit
  $rootScope.$on

Here I use an AngularJS service to implement a reactive design pattern:

// subscribe the service when button1 is clicked
reactiveSrvc.subscribe('button1Clicked', function () {
  $scope.button1Count++;
});

// notify the service that button1 is clicked
$scope.button1Clicked = function () {
  reactiveSrvc.notify('button1Clicked');
};

Here is the demo:
https://jeffxiao.github.io/reactiveSrvc/index.html

It is very simple to use. Enjoy!
