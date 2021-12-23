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
##### How to display error messages in PHP (if you forged " or smth else)
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
