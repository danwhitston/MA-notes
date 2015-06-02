CSS is a separate file that acts as a list of styles to be applied to different bits of the DOM.

```
selector {
  attribute: value one;
}

/* This second statement overrides the first */

selector {
  attribute: value two;
}

** Selectors and how to target them

* Element ( div ) =>
* Class ( .my-class ) => .my-class { color: red }
* ID ( #my_id ) => <h1 id="this-header"> => #this-header { color: red }
* Attribute ([href="http://google.com"]) => 
* Chain ( .ancestor .descendant )
* Child ( .parent > .child )
* Sibling ( .element + .sibling )

Ideally, style classes not elements, i.e. don't style h1 as that's styling semantics.
Ideally, don't style id and use them for JS interactivity instead.
Can use attribute to e.g. find all .co.uk links and style them.



