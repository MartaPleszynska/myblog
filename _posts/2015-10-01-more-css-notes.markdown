Display property - describes the way an element is displayed in a browser, defines the style of a box the element it is using.

Values:
+ ```block``` - takes up a full width of a body which means it will not allow another element sit next it even when it width is less than the ```<body>``` width; you can define padding, width, height, margin; height will expand depend on the content;
HTML tags with ```display:block;``` by default: ```div, header, footer, section, main``` and ```p```.
+ ```inline``` - does not fill whole width; cannot apply ```width, height or margin``` unless applied float property;
HTML tags with ```display:inline;``` by default: ```strong, span, input, label```
+ ```inline-block``` - treats block element like inline element

Float property - puts an element in their own flow, it is used to create layout (like multiple columns); when applied parent tag/element will not see children elements with float property, to avoid that apply ```overflow:auto;``` to the parent; element with absolute position will ignore float property (tbc).
Values:left, right

Position property - describes type of positioning method for an element.

Values:
+ ```static``` - default value
+ ```relative``` - creates new document flow inside original document flow; visually changes position but other elements think that previous position is still occupied and cannot see any child elements within element with position set to relative
+ ```fixed``` - relatively to viewport, lies on top of document flow, has no relationship with parent element
+ ```absolute``` - it is fixed to its first non static parent element, if none found will fix to the body

Let see how it actually looks like.
I have created four ```<div>``` tags with different background colour to see what happens when we change the values in given properties. Three images represent: view in browser, html code and css code.

1.```display:block;```

![display block browser]({{ site.url }}/img/blockbrowser.jpg) ![display block html]({{ site.url }}/img/blockhtml.jpg)![display block css]({{ site.url }}/img/blockcss.jpg)

2.```display:inline-block;```

![display inline-block browser]({{ site.url }}/img/inline_blockbrowser.jpg)
![display inline-block html]({{ site.url }}/img/inline_blockhtml.jpg)![display inline-block css]({{ site.url }}/img/inline_blockcss.jpg)

Note: little space appears between blocks because it takes to account white spaces in html

3.```inline``` - when applied ```inline``` to green and red divs (blue and yellow still set to inline-block) they sit on top of each other and also the blue div do not interact with them hence it also sit on top of them.

![display inline on red and green in browser]({{ site.url }}/img/inlinebrowser.jpg)
![display inline on red and green in css]({{ site.url }}/img/inlinecss.jpg)

You can fix it by applying float property:

![display inline and float on red and green in browser]({{ site.url }}/img/inlinefloatbrowser.jpg)
![display inline float on red and green in css]({{ site.url }}/img/inlinefloatcss.jpg)

Note: no more gaps between red, green and blue divs.

When applying position absolute red and green div will sit next to each other but on top of blue and yellow one as they are in separate document flow:

![display inline and absolute on red and green in browser]({{ site.url }}/img/inlineabsolutebrowser.jpg)
![display inline absolute on red and green in css]({{ site.url }}/img/inlineabsolutecss.jpg)

Here is how different elements will look in a browser when various position values applied:

![different position values in browser ]({{ site.url }}/img/positionbrowser.jpg)

Black border is the body, dotted blue border represents first parent which is non static, dotted green border is static parent. Red div has position value static, blue div-relative, green div-fixed and  purple div-absolute.
