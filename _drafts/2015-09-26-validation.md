---
title:  "Form validation - some code behind the Belbin Test website"
date:   2015-09-26 21:00:17
---
I thought I will share some code which have been used for validation on registration page to create Belbin 1.0.

JavaScript can be used validate forms on client side, before the request is sent to the server. By using regular expressions, we can check value inputed in text boxes against the valid characters. Here are two simple funtions in JavaScript that will validate first and last name.

```javascript
function validateFirstname() {
  var firstname = document.getElementById('firstname').value;
  // firstname should be letters only
  var value = /^[a-zA-Z]+$/i;
  //test regular expression against the value in the field
  if (! value.test(firstname) )
{
  //field is cleared to encourage new correct entry
  document.getElementById('firstname').value = "";
  //meassage to be used in an alert box
  result = "Please enter a valid name! (Letters only)."
}
else
{
  //result is an empty string if the entry is correct
  result = "";
}
return result
}
```

And similar code to validate last name:
```javascript
function validateLastname()
{
var lastname = document.getElementById('lastname').value;
// lastname should start and finish letters only
var value = /^[a-zA-Z ,.'-]+$/i;
//test regular expression against the value in the field
if (! value.test(lastname) )
{
//field is cleared to encourage new correct entry
document.getElementById('lastname').value = "";
result ="Please enter a last name!";
}
else
{
  //result is an empty string if the entry is correct
  result = "";
}
return result
}
```
Both functions will validate input text from a text boxes and checked them against set of agreed characters. Values will be cleared if entered incorrectly and it will not allow to submit a form - which in this case, to register.

Where JavaScript does not work correctly in a browser or it is switched off, validation is done using php and this is a server side validation.

```php
<?php
function validate( $firstname, $lastname){
  $msg = "";
  $value1 = "/^[a-zA-Z]+$/i";
  $value2 = "/^[a-zA-Z ,.'-]+$/i";
  $check1 = preg_match($value1, $firstname);
  $check2 = preg_match($value2, $lastname);
  if ( $check1 == 0 ){
  $msg .= "Please enter valid first name!";
  }
  if ($check2 == 0){
  $msg .= "<br/>Please enter valid last name!";
  }
  return $msg;
}
?>
```
This php function has the same purpose as javascript one.

Validation of forms is important. By restricting input of characters and their length you can avoid incorrect entries being submitted to the database but also it can help defend against malicious attacks like SQL injections .
