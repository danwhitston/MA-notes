SJ Mog put together a github repo and recorded a video on 2/6/15 with CSS info.

CSS is a separate file that acts as a list of styles to be applied to different bits of the DOM.

```
selector {
  attribute: value one;
}

/* This second statement overrides the first */

selector {
  attribute: value two;
}
```

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

*** The Box Model

display: block puts blocks underneath each other

display: inline shrinks blocks to size of content and puts them beside each other

margin: changes the distance between the block and other content

margin: auto tries to centre the block between other objects

margin: 0 auto will try to centre horizontally and go to the edge vertically

display: inline-block puts them side-by-side
everything is defined using rectangular boxes

Within a defined div, all styling only affects the inside, so e.g. border: 2px goes inwards not outwards.

can use text-align: center to centre objects in a display: inline-block div

position: absolute is mostly useful for stopping something from affecting rest of page flow and positioning

position: fixed doesn't move when the rest of the page scrolls
