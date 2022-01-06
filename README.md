<h1 align="center">PHP</h>

```yaml
(PHP: hypertext preprocessor)
```

### Facts:
* The first word of the acronym is an acronym, recursive backronym, originally the acronym stood for Personal Home Page
* Developed in 1994
* PHP is a server scripting language. It can send emails, process a contact form, or connect to a database. HTML, CSS, JS are run on web browser, and we can not use them to store the user info permanently, because the browser gets closed down and we want a way to store that data somewhere centrally so that user can access it anywhere on the web.

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

<h1 align="center"> Variables </h1>
   
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

   <h1 align="center"> Arrays </h1>

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

<h1 align="center"> If statements </h1>

```php
$user = "rob";
if ($user == "rob") {
    echo "Hi Rob!";
}   else {
    echo "I don't know you";
}
```
   
```php
$age = 25;
if ($age >= 18 || $user == "rob" ) {
    echo "you may proceed..";
} else {
    echo "You're too young, sorry!";
}
```
Note: || means OR

<h1 align="center"> Loops </h1>

#### For loops

When Gmail is showing all of your emails that's a loop because it's looping all the emails and displays them for you.

`for` loop
`var` counter variable
`i` counter variable name
`i = 0` setting `i` to its initial value

```php
for ($i = 0; $i < 10; $i++) {
      echo #i."<br>";
}
```

it will display
`
0
1
2
3
4
5
6
7
8
9
`

```php
for ($i = 2; $i <= 30; $i = $i + 2) {
      echo #i."<br>";
}
```

it will display
`
2
4
6
8
10
12
14
`
up to
`30` including.

```php
for ($i = 10; $i >= 0; $i--) {
      echo #i."<br>";
}
```

It will display
`
10
9
8
7
6
5
4
3
2
1
0
`
#### Looping through arrays

```php
$family = array("rob", "Tommy", "M");

for ($i = 0; $i < sizeof($family); $i++) {      
    echo $family[$i]."<br>";
}
```
It will display -->
`
rob
Tommy
M
`
2nd method is `foreach` loop

```php
foreach ($family as $key => $value) {
      echo "Array item ".$key." is ".$value."<br>";
}
```
it will display -->

`Array item o is Rob`

`Array item 1 is Tommy`

`Array item 2 is M`

#### PHP, While Loops

```php
$i = 0;
while ($i <= 10) {
    echo $i."<br>";
    $i++;
}
```
It shows
`
0
1
2
3
4
5
6
7
8
9
10
`

```php
$i = 5;
while ($i <= 25) {
    echo $i."<br>";
    $i = $i +5;
}
```

if you use instead of $i++ e.g.

$i = $i +5;

it will increase numbers by 5 and show
`
5
10
15
20
25
`
or another way:
```php
$i = 1;
while ($i <= 10) {
    $j = $i * 5
    echo $j."<br>";
    $i++;
}
```

To present items from the array:  
```php
$family = array ("A", "B");
$i = 0;
while ($i < sizeof($family)) {
echo $family[$i]."<br>";
$i++;
}
```
It shows items:
`
A
B
`
<h1 align="center"> GET Variables </h1>

#### GET Variables & POST Variables are used to create interaction between user and server.

1. Get variable in the URL string --> `/?name=rob&password=1234&gender=male`

to access them need to know that they are contained in the $_get. So you need to type
```php
print_r($_GET);
```
to present a particular value:
```php
echo $_GET("gender")
```
2. Use a form: 

As HTML:
```html
<p>What is you name?</p>
<form>
    <input name="name" type="text">
    <input type="submit" value="Go!">
</form>
```
For PHP:
```php
echo "Hi there "$_GET['name']."!"
```
and you get Hi there and any name you input in the form's input field.

- Challenge: filename: is_it_prime.php

<h1 align="center"> POST Variables </h1>

#### Post Variables are different than GET Variables, because they aren't encoded in URL, so that makes them a bit more secure. 

```html
<p>What is you name?</p>
<form method="post">    
    <input name="name" type="text">    
    <input type="submit" value="Go!">
</form>
```

for PHP -->
```php
print_r($_POST);
```

If you will want to submit some data twice, you'll get a pop-up telling you to confirm the resumbition. 

- Challenge: When a user enters their name program checks to see if the name is on the array of usernames. If so, hello ...name... is shown on the page. (filename: checking_users.php)
