---
title: "Variable Scope"
tags:
- ict
- language
enableTOC: false
---

## PHP Variable scope
In PHP  you can create variables anywhere in the document. And variable scope means where can that variable be referenced or used. Mainly there are 3 types of variable scopes in PHP.
1. Local 
2. Global
3. Static 

A **Global variable** means any variable that is in the document that is not inside a function. ==These variables can be accessed from anywhere, but you cannot access them within a function== unlike in python.

```php
<?php  
$x = 5; // global scope  
  
function myTest() {  
  // using x inside this function will generate an error  
  echo "<p>Variable x inside function is: $x</p>";  
}  
myTest();  
  
echo "<p>Variable x outside function is: $x</p>";  
?>
```

output:

```txt
Warning: Undefined variable $x in /home/user/scripts/code.php on line 7
<p>Variable x inside function is: </p><p>Variable x outside function is: 5</p>
```

>[!success] Note
>
>In-order to access a global scope variable you can used the `global` keyword!
>```php
>$x = 5;  
>$y = 10;  
>
>function myTest() {  
>  global $x, $y;  
>  $y = $x + $y;  
> }
> myTest();  
> echo $y; // outputs 15  

This means a variable declared inside a function has a **Local Scope** and ==can only be accessed inside a function==. You cannot access variables that are created inside a function outside of that function.

```php
<?php  
function myTest() {  
  $x = 5; // local scope  
  echo "<p>Variable x inside function is: $x</p>";  
}  
myTest();  
  
// using x outside the function will generate an error  
echo "<p>Variable x outside function is: $x</p>";  
?>
```

Output:

```txt
<p>Variable x inside function is: 5</p>
Warning: Undefined variable $x in /home/user/scripts/code.php on line 10
<p>Variable x outside function is: </p>
```

>[!note] The more you know!
>
>PHP also stores all global variables in an array called `$GLOBALS[_index_]`. The _`index`_ holds the name of the variable. This array is also accessible from within functions and can be used to update global variables directly.

```php
>$x = 5;  
$y = 10;  
function myTest() {  
  $GLOBALS['y'] = $GLOBALS['x'] + $GLOBALS['y'];  
}  
myTest();  
echo $y; // outputs 15
>```

Normally, when a function is completed/executed, all of its variables are deleted. However, sometimes we want a local variable NOT to be deleted. We need it for a further job.

To do this, use the `static` keyword when you first declare the variable:

```php
function myTest() {  
  static $x = 0;  
  echo $x;  
  $x++;  
}  
  
myTest();  
myTest();  
myTest();  
```

Then, each time the function is called, that variable will still have the information it contained from the last time the function was called.

>[!caution] Note 
>The variable is still local to the function.
