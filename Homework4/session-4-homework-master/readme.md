##Homework

Review the [steps we took](https://github.com/mean-spring-2017/session-4b#angular-as-a-templating-engine) to add Angular to our page. 

Be sure to check out the links provided in the readme for Angular:
* [directives](https://www.w3schools.com/angular/angular_directives.asp)
* [scope](https://docs.angularjs.org/guide/scope#!)
* [expressions](https://docs.angularjs.org/guide/expression)
* [directives](https://docs.angularjs.org/api/)

Go to: `https://api.github.com/users/dannyboynyc`

Your first job is to extract your username from your github api and display it on a page using Angular. (You need not use Express or npm for this.) 

Run `$ lite-server` in the homework directory (or `$python -m SimpleHTTPServer 3000` for those without lite-server installed).

Examine the code below:

```
app.controller("NavController", function( $scope, $http ) {

$http.get('https://api.github.com/users/dannyboynyc')
.then( onUserComplete )

var onUserComplete = function (response){
  $scope.user = response.data
} 
```

`<p>{{ user.name }}</p>`

One new item in the scripts above is `$http`. We will be using this extensively so you should skim the [documentation](https://docs.angularjs.org/api/ng/service/$http).

Another item which is new here is `.next`. This innocuous little bit of code is actually quite important in our work as it represents what is known as a promise - a relatively new feature which aids in the management of asynchronous events. We'll learn more about them as we go on however it might be worthwhile skimming this Google Developers [article](https://developers.google.com/web/fundamentals/getting-started/primers/promises).

Implement this script in `index.html` and `navItems.js` (the code is in place, you need only uncomment and review).

Go to [this link](http://oit2.scps.nyu.edu/~wiseb/daniel-was-here/) (thanks Brian!).

Now use this data api:

`https://api.punkapi.com/v2/beers/`

to make `index.html` display beer data in the same way. Then add images from the punkapi. 

1. Apply any required css to have the page display properly (pay attention to responsive design)

2. Sort them alphabetically and create an input field to act as a filter.

Finished code is available in the homework folder: `index-DONE.html` - try to accomplish the homework without peeking at it first.

That's it! Simple - right?

