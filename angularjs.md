* What's two way binding?
  * Two-way binding means that any data-related changes affecting the model are immediately propagated to the matching view, and that any changes made in the view (say, by the user) are immediately reflected in the underlying model. When app data changes, so does the UI, and conversely.
* What's ng-model?
  * The ngModel directive binds an input,select, textarea (or custom form control) to a property on the scope. 
* What is `$http`?
  * A service for making AJAX calls via the HTTP protocol
* What is ng-repeat?
  * Used for repeating a set of elements and iterating over a collection. 
* What are `$index`, `$even`, `$odd`, `$first`, and `$last`?
  * $index - The index of the current element.
  * $first - Boolean indicating if the element is first in the collection.
  * $middle - Boolean indicating if the element is neither first nor last in the collection.
  * $last - Boolean indicating if the element is last in the collection.
  * $even - Boolean indicating if the element's index is even.
  * $odd - Boolean indicating if the element's index is odd. 
* How would you filter a list via ng-repeat?
  * div class="row col-xs-12 col-sm-12 col-md-12 col-lg-12 productBorder"
		ng-repeat="product in products | orderBy:'name' | filter:search" (search is a scope variable)
* What's the difference between `angular.module('app' , [])` and `angular.module('app')`
  * first one creates a module injecting the dependency modules. second is used to reference the creation of controllers and directives. 
* What are directives (briefly)? 
  * At a high level, directives are markers on a DOM element (such as an attribute, element name, comment or CSS class) that tell AngularJS's HTML compiler ($compile) to attach a specified behavior to that DOM element (e.g. via event listeners), or even to transform the DOM element and its children. 
* Why would you use ng-submit instead of ng-click in some cases?
  * The ngSubmit directive binds to the submit event in the browser, which is fired when a form is submitted. The ngClick directive allows you to specify custom behavior when an element is clicked.
* What's Dependency Injection?
  * Where you do not create the dependencies required instead have the framework provide it to you.
* Do other frameworks use dependency injection (even if only for internal use)? Answer: yes (React,Ember)
* How would you inject services and what are the different ways to do so?
 * Passing a dependency as Function Arguments, Passing a dependency as Array Arguments, Passing a dependency using the $inject service 
* What's jqLite?
 * jqLite is a tiny, API-compatible subset of jQuery that allows Angular to manipulate the DOM in a cross-browser compatible way. jqLite implements only the most commonly needed functionality with the goal of having a very small footprint. 
* How do you ensure Angular uses jQuery when including them both?
  * To use jQuery , simply ensure it is loaded before the angular.js file.  
* What are promises and how would you use them?
  * A promise represents the eventual result of an operation. You can use a promise to specify what to do when an operation eventually succeeds or fails. Using $q. (http://www.dwmkerr.com/promises-in-angularjs-the-definitive-guide/) 
* What's the difference between factory/provider/service/value/constant?
 * Factory returns an object. Services do not return an object. Providers have a $.get function() which returns an object. 
* When would you use each one?
 * https://gist.github.com/demisx/9605099 
* What are filters?
 * Filters can be added in AngularJS to format and transform data. (http://www.w3schools.com/angular/angular_filters.asp)
* Why would you use ng-src, ng-bind, and ng-cloak?
 * http://www.w3schools.com/angular/ng_ng-bind.asp 
 * http://stackoverflow.com/questions/27554765/use-of-ng-src-vs-src 
 * https://docs.angularjs.org/api/ng/directive/ngCloak 
* What's the difference between ng-if and ng-show?
 * If ng-if is used on an element, then it won't be included in the DOM, but for ng-show the element is present just its display is none. 
* What phases are there in angular? Answer: config -> bootstrap -> run
* Why would you use `.config()` and `.run()` phase?
 * Config block is executed during the provider registration and configuration phase. We can have these as many as we want in the application. Only providers and constants can be injected into configuration blocks and not instances. Run block is executed after the execution of configuration block. It inserts instances and constants but not providers. This block is created using run() method. 
 * (http://codeanalyze.com/Que/Ans/38295/What-is-difference-between-config-and-run-method-in-AngularJS) 
* What is ng-app and how does angular bootstrap?
 * https://docs.angularjs.org/guide/bootstrap 
* When would you use `$q.all()`?
 * https://www.jonathanfielding.com/combining-promises-angular/ 
* Where would you make your network calls controller, template, directive, or service and why? (where would you use $http)
 * In services for reusabilty purposes. 
* Say that you are going to alert an error where would you put that alert from a network call? Service, controller, template and why? [Answer](https://gist.github.com/gdi2290/b9d34955f0d3bce2c1b6)
* How would you dynamically filter a list with an ng-repeat? (clicking on different filters)
* What's ng-messages and ng-message?
* What's ng-style and ng-class?
 * dynamically add styles and classes  
* How would you attach something to the header of every http call?
* What is `$scope.$on()` and how would you use it?
 * to intercept events. 
 *  $scope.$on('timer-tick', function (event, args) {    });
 * http://stackoverflow.com/questions/14502006/working-with-scope-emit-and-on 
* What are `$http` interceptors?
* What is `"$locationChangeStart"`?
 * http://stackoverflow.com/questions/26779704/difference-between-locationchangestart-routechangestart-and-statechangestar 
* What's html5Mode?
* How do you turn off cache for a `$http` call?
* What is the `$templateCache`?
 * http://pracujlabs.io/2015/12/28/using-templatecache-in-angularjs.html 
* How would you implement auth as in locking down certain parts of the app? 
* What's ui-router and why use it over ng-route?
 * ui-router is a 3rd-party module and is very powerful. It supports everything the normal ngRoute can do as well as many extra functions.
 * http://stackoverflow.com/questions/21023763/angularjs-difference-between-angular-route-and-angular-ui-router
* What are states?
 * A state corresponds to a "place" in the application in terms of the overall UI and navigation. A state (via the controller / template / view properties) describes what the UI looks like and does at that place.
 * https://github.com/angular-ui/ui-router/wiki#state-manager
* How do you resolve resources via state/route and how would you do so?
 * http://plnkr.co/edit/u18KQc?p=preview
* Given 3 nested states, how would you load the most nested one after the root state resolves while allowing the middle state to load asynchronously?
 * http://plnkr.co/edit/SDOcGS?p=preview
* What types of directives are there? Angular: element, attribute, class (no one uses class)
* What is `$scope`?
  * The scope is the binding part between the HTML (view) and the JavaScript (controller).
  * http://www.w3schools.com/angular/angular_scopes.asp
* What is `$rootScope`?
 * $rootScope is a parent scope of all $scope and can be shared to all $scope.
 * http://www.codeandyou.com/2015/09/what-is-rootscope-in-angularjs.html
* What is `"$destroy"`?
 * Angular will broadcast a $destroy event just before tearing down a scope and removing the scope from its parent. Listening for this event is crucial for cleaning up tasks and resources that otherwise might continue to chew up memory or CPU.
 * http://odetocode.com/blogs/scott/archive/2013/07/16/angularjs-listening-for-destroy.aspx
* What's one time binding?
 * Achieved using ::
 * https://toddmotto.com/angular-one-time-binding-syntax/
* When and where would you normally use `.$watch()`?
 * For watching scope variables.
 * $scope.$watch('alertFilter', function (newAlertFilter, oldAlertFilter) {    }, true);
* What's a stateful filter vs a stateless filter?
* What are `.$dirty`, `.$pristine`, `.$valid`, `.$invalid`, and `.$submitted`?
* What's NgModelController? 
 * NgModelController provides API for the ngModel directive. The controller contains services for data-binding, validation, CSS updates, and value formatting and parsing.   
 * https://docs.angularjs.org/api/ng/type/ngModel.NgModelController
* What's FormController?
 * https://docs.angularjs.org/api/ng/type/form.FormController
* What's ng-model-options and why would you use it?
* What are `$validators` and `$asyncValidators`?
* What's the difference between `scope`, `$scope`, and `$rootScope`?
 * Already covered.
* What's the difference between controller and link directives?
* How do you require a controller in a directive?
* How do you require more than one controller in a directive?
* What's an isolated scope?
 * Adding a scope property into the directive created an isolated scope.
 * http://weblogs.asp.net/dwahlin/creating-custom-angularjs-directives-part-2-isolate-scope
* For an isolate scope what are these symbols `?`,`@`,`=`,`&`,`*` in relation to directives
* What are compile/pre-link/post-link phase for directives?
* What is `$interpolate`?
* What is `$compile`?
* What is `$observe`?
* What's transclusion?
* Why would you need transclusion?
* What's `bindToController:` and `controllerAs:` syntax? 
* What are directives and what are components?
* What's the difference between `.$broadcast()`, and `.$emit()`?
 * $broadcast() - children scopes and below.
 * $emit() - parent scopes and above.
* What are `$timeout()` and `$interval()` and how do you cancel them?
 * AngularJS wrappers for setTimeout() and setInterval().
 * using $timeout.cancel(timeout)
* What's dirty checking?
 * Angular "digest" is also called "dirty checking", because, in a way, it scans the scope for changes.
 * http://stackoverflow.com/questions/24698620/dirty-checking-on-angular
* Do other frameworks use dirty checking? Answer: yes (React,Polymer)
* What is the `.$digest()` loop?
 * https://www.ng-book.com/p/The-Digest-Loop-and-apply/
* What's the difference between `.$digest()` and `.$apply()`?
* What are `$watchGroup` and `$watchCollection`?
* What are `$eval`, `$parse` and `$evalAsync`?
* What is `$applyAsync`?
* What's a decorator in relation to angular's module system?
* How would you filter a large list with ng-repeat to include data from the server and client?
* How would you grab the `$injector`/`$scope` from the chrome console?
* Why is there ng-form?
* How would you dynamically create forms?
* What's CSP and how does it relate to angular?
 * Content Security Policy (CSP) and it slows down the execution by 30%.
 * http://www.w3schools.com/angular/ng_ng-csp.asp
* How do you structure your files for a large team/project?
* How would you use a module loader/bundler such as browserify, webpack, or systemjs with angular?
* How would you asynchronously load angular?
* How would you inject server rendered data into client angular?
* What's a document fragment?
* What's the ShadowDOM?
 * Shadow DOM refers to the ability of the browser to include a subtree of DOM elements into the rendering of a document, but not into the main document DOM tree.
 * https://glazkov.com/2011/01/14/what-the-heck-is-shadow-dom/
* What is needed for your angular web app to work with JavaScript disabled?
 * <noscript>You must have JavaScript enabled to use this app.</noscript>
 * http://stackoverflow.com/questions/22256371/how-to-handle-javascript-being-disabled-in-angularjs
* What is needed for your angular web app to be rendered on the server to be sent down to the client?
* Generally speaking how would you paraphrase angular?
* How would you progressively enhance your RESTful app with a pub/sub?
* How would you structure your app if you only had a realtime (pub/sub) API (no REST)?
* What are the pros and cons of each design?
* What are some anti patterns developers tend to fall into while using angular?
* What are the problems currently facing angular1?
 * Two way Data binding, $digest cycle.
 * https://larseidnes.com/2014/11/05/angularjs-the-bad-parts/
* Explain how Angular 2 is solving all of the problems from 1.x
 * http://angular-tips.com/blog/2015/06/why-will-angular-2-rock/
* Demonstrate a few ways to migrate an Angular 1 app to Angular 2
* What's the difference between MVC, MVVM, MVP(SC), MVP(PV), PM, and how does it compare to Flux/Redux architecture?
* How are dependencies handled when testing Angualar controllers and services?
* How is `$scope` injected when testing Angular controllers?
* What is the purpose of wrapping core Angular providers and services in double underscores? ex: `_$rootScope_`?
* Describe the necessary steps to test the Angular `$http` service
 * $httpBackend.when('GET', 'resource/en.json').respond(__fixtures__['resource/en']);
 * Call the method.
 * $httpBackend.flush();
* How would you test an `$http` request to a third party API such as Youtube?
 * $httpBackend - Fake HTTP backend implementation suitable for unit testing applications that use the $http service.
* How would you test the data being returned from the API request?
 *  $httpBackend.when('GET', 'resource/en.json').respond(__fixtures__['resource/en']);
* What frameworks, languages and tools are available for testing in Angular?
* How is $scope used when testing Angular controlers?
* Explain what `$httpBackend` and `$httpBackend.flush` are used for
 * Covered above.
* Explain what `angular.mock` is used for
 * The ngMock module provides support to inject and mock Angular services into unit tests. In addition, ngMock also extends various core ng services such that they can be inspected and controlled in a synchronous manner within test code.
 * https://docs.angularjs.org/api/ngMock
