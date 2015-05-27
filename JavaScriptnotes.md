Sam Joseph [2:09 PM]
@daniel_johnston: if codeacademy javascript is making you lose the will, you might find this an interesting alternative: https://pragprog.com/book/csjava/3d-game-programming-for-kids
title: 3D Game Programming for Kids: Create Interactive Worlds with JavaScript, by: Chris Strom, isbn: 9781937785444, date: 2013-10-23

Sam Joseph [2:10 PM]
@daniel_johnston: there's also this: https://www.youtube.com/watch?v=wWIGEM4E9iw&list=PLxNY6twFc_xCxdSPLlxUS4C0VO3sni2DA
YouTube
UCBerkeley
CS169 Software as a Service - Lecture 16 

Sam Joseph [2:10 PM] 
and this: http://agentcooper.github.io/js-ruby-comparison/
Ruby and Javascript comparison table

Sam Joseph [2:10 PM]
and this http://skilldrick.co.uk/2011/01/ruby-vs-javascript-functions-procs-blocks-and-lambdas/

Sam Joseph [2:12 PM]
BTW, I think my personal preference for ranking up on JavaScript is just repeatedly doing JavaScript katas on http://www.codewars.com/ and using https://developer.mozilla.org/en-US/docs/Web/JavaScript to look up all the new methods

Mozilla Developer Network
JavaScript
JavaScript ® (often shortened to JS) is a lightweight, interpreted, object-oriented language with first-class functions, most known as the scripting language for Web pages, but used in many non-browser environments as well such as node.js or Apache CouchDB. It is a prototype-based, multi-paradigm scripting language that is dynamic, and supports object-oriented, imperative, and functional programming styles. Read more about JavaScript.

Sam Joseph [2:12 PM]
they also have a nice introduction to JavaScript section: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide

Mozilla Developer Network
JavaScript Guide
The JavaScript Guide shows you how to use JavaScript and gives an overview of the language. If you want to get started with JavaScript or programming in general, consult the articles in the learning area. If you need exhaustive information about a language feature, have a look at the JavaScript reference.

Sam Joseph [2:13 PM]
and the chrome console is the place to live and it can be much friendlier with these tips and tricks: https://developer.chrome.com/devtools/docs/tips-and-tricks

here's another resource for "JavaScript for Ruby Programmers" - http://www.martinrinehart.com/models/tutorial/tutorial_19.html
tutorial for Google SketchUp including SketchUp rubies

Ben's lecture Tuesday pm:

var variableName defines a variable. If we don't use var, then JS will look up through the function tree until it finds an existing variable with that name, and create a global variable if none exists. That makes it wise to always use var when declaring variables.

function creates scope, and that's the only thing that defines scope. Except maybe for loops?!

Constructor pattern:

```
function Dog() {
  this.name = 'Barney';
  this.bark = function() {
    return 'Bark!';
  }
}
```

```
dog = new Dog
dog.bark()
=> "Bark!"
dog.name
=> "Barney"
```

Relatedly: always use new when calling a constructor function, and never use new with a non-constructor function, and always use new with a capital letter function, and never use new with a non-capital letter function.

this can be unexpected, so use console.log(this) to check.

Ben's lecture Wednesday am

### Setting up Jasmine

Using standalone version for easy unit testing of JS components

Set up lib, spec, src and specrunner.html acting as test console

lib holds Jasmine code this time round!
spec holds example tests
src holds example code

Create initial test using Jasmine, e.g.

```
describe('Airport', function (){
  it('can land planes', function(){
    var airport = new Airport();
    var plane = {};
    airport.land(plane);
    expect(airport.planes).toContain(plane);
  })
})

Note plane = {} is making a dummy object

Can declare functions in multiple ways

function Airport(){}; # declares function as a function

var Airport = function(){} # declare function as a var. This doesn't come into scope until it's been read and produces difficult to trace errors as the function is anonymous

function Airport(){
  this.planes = [];
  
  this.land = function(plane){
    this.planes.push(plane);
  };
};

    
