---
title:  "Introduction to HTML and CSS"
date:   2015-09-29 21:00:17
---

HTML stands for HyperText Markup Language and used to create web pages. A web browser reads HTML files and render them into visible or audible pages.
A simple HTML structure looks like this:
![HTML Code]({{ site.url }}/img/htmlCode.jpg)
And in a browser
![HTML in Browser]({{ site.url }}/img/htmlBrowser.jpg)

Every html page must start with ```<!DOCTYPE html>```. It defines the version of the document and its type.
```<html>``` is the root of the document.
```<head>``` tag is used to contain metadata which are describes in tags like: ```<title> <style> <link> <meta>```.
Title is the title of the document.
Style describes the styling.
Link contains references to external files.
Meta is used to describe the page, include keywords for search engines.
```<body>``` describes content visible in a browser.
Headers are contain in ```<h1> <h2> <h3> ...``` tags; paragraphs in ```<p>```; tables in ```<table>``` tag and so on
The important thing is to remember to close the tag: ```</html> </body> </h1>``` etc
There are of course exceptions to the rule: ```img, input, br, hr, meta``` tags do not have closing tags.

Tags have properties and attributes. Property in put inside a opening tag after its name and attributes in similar way however the value needs to be specified:
<tagname property attribute="value"></tagname>


CSS stands for Cascading Style Sheets and it a stysheet language that describes how HTML document should be presented. You can change font size, family or colour, background, apply border and many more.
Here a simplified code structure in css:

![CSS code]({{ site.url }}/img/cssCode.jpg)

This example will change background colour to blue for whole html body.
Browser may have different default styles for html tags so if no style applied html page may look bit different depend on a browser.
There are three ways on applying css to html:

1. In line css - applied in inner tags: ```<tagname style="background-color: blue;"```
2. In head tag inside html <style></style>
3. In separate css file

To find out more about HTML and CSS visit following links:
+ [w3 - html](http://www.w3.org/TR/html/)
+ [w3schools](http://www.w3schools.com/)
+ [HTML.net](http://html.net/)
