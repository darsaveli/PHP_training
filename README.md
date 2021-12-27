<h1 align="center">PHP</h>

```yaml
(PHP: hypertext preprocessor)
```

### Facts:
* The first word of the acronym is an acronym, recursive backronym, originally the acronym stood for Personal Home Page
* Developed in 1994
* PHP is a server language. It can send emails, process a contact form, or connect to a database. HTML, CSS, JS are run on web browser, and we can not use them to store the user info permanently, because the browser gets closed down and we want a way to store that data somewhere centrally so that user can access it anywhere on the web.

(HTML...CSS...JS...WebGL)Web Browser <---->internet<----->Web Server (PHP...MySQL, Apache, Server Modules)

So languages that work on the web server allow us to do the web service-specific things like logging a user in or returning their tweets or saving their progress in a game. 
* PHP is powering 81.8% of the web as of 2021. 
* It's a language in which WP is built and learning PHP will enable you to create WP plug ins, customize WP themes and etc.
* .php file can contain HTML, CSS, JS and PHP code.

### Tips:
#### How to display error messages in PHP (if you forged " or smth else)
* create a separate new file, call it php.ini, it will contain initialization options
* set 2 variables
* `error_reporting = E_ALL`
* meaning report on any type of errors and
* `display_errors = On`
* these will allow displaying errors when we develop site. If it's online, need to delete them so the hackers won't use the error messages to access your website.
* if error message refers to line 6, the error may be on previous line, because the error was not detected until line 6.

* echo "Hello World"; --> displays text in php. Use only semi columns.

* must put HTML outside of these tags
```php
<?php 
some php code here
?>
```

#### String variables (containing a string of characters) in PHP

```php
<?php
$name = "Rob";
?>
```

example:
```php
<?php
$name = "Rob";
echo "My name is $name";
?>
```

It will display variable value -->

`my name is Rob`

```php
<?php
$name = "Rob";
echo $name;
?>
```

it will display -->

`Rob`

* How to put strings together (Concatenating)

```php
$string1 = "This is the 1st part of a sentence";
$string2 = "here you have the 2nd one";
echo $string1.$string2;
```

`." ".` is used to put a space between strings

you can put HTML inside those strings to make them appear on different lines. Add `<p>` tag.

```php
$string1 = "<p>This is the 1st part of a sentence</p>";
$string2 = "<p>here you have the 2nd one</p>";
echo $string1." ".$string2;
```

* PHP Variables containing a string of numbers

```php
$myNumber = 45;
$calculation = $myNumber * 31 / 97 + 4;
echo $calculation;
```

it will display -->

`18.381443298969`

for multiplication use asterisk (*)

```php
$myNumber = 45;
$calculation = $myNumber * 31 / 97 + 4;
echo "The result of the calculation is ".$calculation;
```

* Boolean variables in PHP

```php
$myBool = true;
echo "<p>This statement is true? ".$myBool."</p>";
```

It will show -->

`1`

```php
$myBool = false;
echo "<p>This statement is true? ".$myBool."</p>";  
```

It will show -->

`0 or nothing`

Note: it doesn't give true false, but 1 or 0. This is how PHP treats true and false. 

* Store Variable names within variables:

```php
$name = "Mari";
$variableName = "name";
echo $$variableName;
```

#### Arrays (ways of storing a number of different values in the same object) in PHP

```php
$myArray = array("a", "b", "c", "d");
print_r($myArray);
shows -->
```

`Array ( [0] => a [1] => b [2] => c [3] => d )`

`print_r` shows the contents of the array (_r stands for readable)

In the page source, it displays like -->

```php
Array
( 
   [0] => a 
   [1] => b 
   [2] => c 
   [3] => d
)
```

* Get items from Array

```php
echo $myArray[1];
```

displays `b`

* Define an array by creating values manually:

the arrays are associative, meaning you can put anything you like in the index, e.g. jump from 2 to 5 or call it "myFavouriteFood"

```php
$anotherArray[0] = "a";
$anotherArray[2] = "b";
$anotherArray["myFavouriteFood"] = "ice cream";
print_r($anotherArray);
```

* Putting line breaks:

```php
echo "<br><br>";
```

* If you want to make an associative PHP array like "myFavouriteFood" to store info about password, username, etc, then:

```php
$thirdArray = array("France" => "French", "USA" => "English");
print_r($thirdArray);
```
Shows -->
`Array ( [France] => French [USA] => English )`

* Get the length of the array (number of items in the array)
```php
echo sizeof($thirdArray);
```
Shows -->
`2`

* Add an item to the end of an array

```php
$myArray = array("a", "b", "c", "d");
$myArray[] = "e";
print_r($myArray);
```

* Remove item using unset command
```php
$myArray = array("a", "b", "c", "d");
unset($myArray["0"]);
print_r($myArray);
```
Shows -->
```php
Array 
( 
   [1] => b 
   [2] => c 
   [3] => d 
)
```
