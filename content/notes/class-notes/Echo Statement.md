---
title: "PHP | Echo"
tags:
- ict
- php
enableTOC: false
---

# Echo Statement
The following example shows how to output text with the `echo` command in [[notes/class-notes/php|php]] (as stated above notice that the text can contain HTML markup):

```php {titl="php"}
<?php  
echo "<h2>PHP is Fun!</h2>";  
echo "Hello world!<br>";  
echo ("I'm about to learn PHP!<br>");  
echo "This ", "string ", "was ", "made ", "with multiple parameters.";  
?>
```

Displaying variables using the echo command:

```php
<?php  
$txt1 = "Hello World!";  
$txt2 = "Sri Lanka";  
$x = 5;  
$y = 4;  
  
echo "<h2>" . $txt1 . "</h2>";  
echo "I live in " . $txt2 . "<br>";  
echo $x + $y;  
?>
```

>[!done] FYI
>
> commas `,` are used to separate parameters while dots `.` are used for string concatenation[^6]. 