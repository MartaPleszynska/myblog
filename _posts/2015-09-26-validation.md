---
title:  "Form validation - some code behind the Belbin Test website"
date:   2015-09-26 21:00:17
---
I thought I will share some code which have been used for validation on registration page to create Belbin 1.0.

JavaScript can be used validate forms on client side, before the request is sent to the server. By using regular expressions, we can check value inputed in text boxes against the valid characters. Here are two simple funtions in JavaScript that will validate first and last name.

![First Name Validation]({{ site.url }}/img/validateFirstName.jpg)
![Last Name Validation]({{ site.url }}/img/validateLastName.jpg)

Both functions will validate input text from a text boxes and checked them against set of agreed characters. Values will be cleared if entered incorrectly and it will not allow to submit a form - which in this case, to register.

If you try to register with empty fields you will get alert message:

![Alert message]({{ site.url }}/img/alertmsg.jpg)

Which another JavaScript function is responsible for.

![Alert message]({{ site.url }}/img/validateOnSubmit.jpg)

Where JavaScript does not work correctly in a browser or it is switched off, validation is done using php and this is a server side validation.

![PHP function]({{ site.url }}/img/phpfunction.jpg)

This php function has the same purpose as javascript one.

Validation of forms is important. By restricting input of characters and their length you can avoid incorrect entries being submitted to the database but also it can help defend against malicious attacks like SQL injections.

[Read more](https://validator.w3.org/docs/why.html) about why validate websites.
