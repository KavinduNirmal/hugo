---
title: "PHP Print statement" 
tags:
- ict
- php
enableTOC: false
---

# Print Statement

The following example shows how to use print statement for data outputting, Notice that there are no example with multiple parameters. Another thing to remember is print would always return a string, even if you pass through an integer[^16],

```php
<?php
// Output strings
print "<h2>PHP is Fun!</h2>";  
print "Hello world!<br>";  
print "I'm about to learn PHP!";  

// Output variables
$txt1 = "Hello World!";  
$txt2 = "Sri Lanka";  
$x = 5;  
$y = 4;  
  
print "<h2>" . $txt1 . "</h2>";  
print "I live in " . $txt2 . "<br>";  
print $x + $y;
?>
```

>[!warning] FYI
>
>you might encounter `printf()` function as a recommendation in _intelliSense_ while you’re coding.  But keep in mind these two; `print()` and `printf()` are completely two different functions.
