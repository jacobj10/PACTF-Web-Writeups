#SQL: The Sequel (50)
##Dr. Miles looked at our stuff and decided to teach us a lesson. Unfortunately, he was kind of in a rush and decided that the builtin PHP string escapes should be enough. Is he right?

http://159.203.217.155/Injection2/

The query is the same, the only difference in source code is:

```php
 // Nobody will be able to inject into our code now!
  mysql_query('SET SQL_MODE="NO_BACKSLASH_ESCAPES"');
  $uname = mysql_real_escape_string($_POST["username"]);
  $pswd = mysql_real_escape_string($_POST["password"]);
```
This prevents the use of \ as well as '. So we need to do our injection only using the " symbol.
The query " OR 1=1 -- should do the trick, but it returns false.
However, a few minutes of guessing and " OR 1=1 LIMIT 1 -- does the trick and gives the page:

#Welcome!

##Your flag is: bobby_tables_little

flag: bobby_tables_little
