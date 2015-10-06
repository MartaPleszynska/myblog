---
title:  "CSS selectors"
date:   2015-10-03 21:00:00
---
Here are some noted selector we have talked about:

For element(s) with specified class:
.classname{}

For element(s) with specified id:
#idname {}

For all elements:
* {}

The same style for different elements:
selector1, selector2 {attribute:value;}

Example: p, a {text-decoration:underline;} - will apply underline to all p and a elements.  

For all elements(2) inside another element(1):
selector1 selector2 {attribute:value;}

For all elements (2) that is a direct children of its parent element(1):
selector1 > selector2 {attribute:value;}

For every element(2) that has a direct parent element(1):
selector1 ~ selector2 {attribute:value;}

Selector with specific attribute:
selector[attribute]{attribute:value;}
selector[attribute=value]{attribute:value;}
Example: input[type=radio]{}

Specific selector inside another selector:
selector1 selector2+selector2+selector2 {attribute:value;}
(third selector2 inside selector1 - must be directly after...)

selector:hover{} - for the elements on mouse over
selector:active{} - for an active link
selector:focus{} - for the element which has focus
selector:selected{} - (for radio buttons, dropdown)
selector:checked{} - (for check boxes)
selector:visited{} - for all visited links
selector:required{} - for input elements with the "required" attribute specified
selector:empty{} - for every element that has no children
selector:nth-child(n){} - for every element that is the n-th child of its parent

selector:nth-of-type(n){} - for every selected element that is the n-th element of its parent of the same type
  Example: p:nth-of-type(4) -	selects every <p> element that is the fourth <p> element of its parent

selector:first-child{} - for the first child of the selected element
selector:last-child{} - for the last child of the selected element (not widely supported yet)

selector::before{} - inserts something directly before the content of selected element but after the previous one.
selector::after{} - inserts something directly after the content of selected element but before the next one.
Example:
 li::before{content:">"}
inserts '>' before each list element

For more about selectors and more example checkout following links:
+ [w3schools-selector reference](http://www.w3schools.com/cssref/css_selectors.asp)
+ [w3schools-try it](http://www.w3schools.com/cssref/trysel.asp)
+ [w3-css3 selectors](http://www.w3.org/TR/css3-selectors/)
