Display property - describes the way an element is displayed in a browser, defines the style of a box the element it is using.

Values:
+ ```block``` - takes up a full width of a body which means it will not allow another element sit next it even when it width is less than the ```<body>``` width; you can define padding, width, height, margin; height will expand depend on the content;
HTML tags with ```display:block;``` by default: ```div, header, footer, section, main``` and ```p```.
+ ```inline``` - does not fill whole width; cannot apply ```width, height or margin``` unless applied float property;
HTML tags with ```display:inline;``` by default: ```strong, span, input, label```
+ ```inline-block``` - treats block element like inline element; note: little space appears between blocks because it takes to account white spaces in html

Float property - puts an element in their own flow, it is used to create layout (like multiple columns); when applied parent tag/element will not see children elements with float property, to avoid that apply ```overflow:auto;``` to the parent; element with absolute position will ignore float property (tbc).
Values:left, right

Position property - describes type of positioning method for an element.

Values:
+ ```static``` - default value
+ ```relative``` - creates new document flow inside original document flow; visually changes position but other elements think that previous position is still occupied and cannot see any child elements within element with position set to relative
+ ```fixed``` - relatively to viewport, lies on top of document flow, has no relationship with parent element
+ ```absolute``` - it is fixed to its first non static parent element, if none found will fix to the body

Let see how it will look in a browser: black border is the body, dotted blue border represents first parent which is non static, dotted green border is static parent.


Display values:
```<div>``` is by default block so appears in browser like this:
![display:block]({{ site.url }}/img/block.png)
When inline-block applied:
![display:inline-block]({{ site.url }}/img/inline-block.png)
When inline  and float: left applied:
![display:inline and float:left]({{ site.url }}/img/inline-float.png)
It is visible that parent2 does not see children divs
Here is how it look the overflow: auto is applied and blue and purple divs are floated to the left:
![overflow:auto]({{ site.url }}/img/overflow.png)

Position values: Red div has position value static, blue div-relative, green div-fixed and  purple div-absolute.
![different position values in browser ]({{ site.url }}/img/positionbrowser.jpg)

Base html used:

![HTML code ]({{ site.url }}/img/htmlcode.png)

Base CSS used:

![CSS code]({{ site.url }}/img/csscode.png)
