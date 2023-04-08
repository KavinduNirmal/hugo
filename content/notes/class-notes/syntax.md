---
title: "Language Syntax"
tags: 
- ict 
- language
enableTOC: true
---

## PHP Syntax

[[notes/class-notes/php|PHP]] syntax[^19] is pretty straight forward. Most of the rules are same in comparison to [[notes/class-notes/python|Python]] but it is mostly resembles that of [[JavaScript]]. [^22]

Executing code in [[notes/class-notes/php|PHP]] is done in server-side unlike python, which scripts run in the command line. ==PHP is executed in the server in the background== which outputs the results to a plain [[html]] file to be displayed in the browser. 

>[!note] Note
>
>In Python  the command line was the output, but in PHP its a web page. 

[[notes/class-notes/php|PHP]] is just a fancy way of doing html; `html` is an acronym for `Hypertext Markup Language` and `PHP` stands for `Hypertext preprosessor`[^21], PHP process the html before inside a server and then sends the output to the client. Because of this, php can be written within html with no issues. 

You can write normal html and insert php scripting when necessary by opening a `<?php  ?>` element/tag or just write everything; even putting `html` elements inside a single `<?php  ?>` element. Everything outside of a opening tag `<?php` and closing tag `?>`  are ignored by the PHP parser which allows the php document have mixed content like `html` and `css`.  

```php {title="php"}
<?php  
// PHP code goes here  
?>
```

Below, is an example of a simple PHP file, with a PHP script that uses a built-in PHP function "`echo`" to [[notes/class-notes/Output#Echo Statement|output]] the text "Hello World!" on a web page:

```php {title="index.php"}
<!DOCTYPE html>  
<html>  
<body>  

<?php  
echo "Hello World!";  
?>  
  
</body>  
</html>
```

>[!caution]
>
>Though you can write normal `html` code inside the `php` element, be careful to remember that you are already inside an element, which means the parser[^20] is looking for the end of the tag which is `>` ==this means you cannot open html elements the way you normally would==. If this were to happen the server will throw an error.
>To overcome this you have to pass the html code through the `echo` statement as follows;

```php
<?php  
echo "<h1>Hello World!</h1>";  
?>  
```

>[!info] Did you know?
>
>You can also use short echo tag for quick outputs. This can be done by simple `<?= 'print this string' ?>` This is also equivalent to `<?php echo 'print this string'; ?>`

==PHP statements ends with a semicolon== `;`. You have to be careful to not to forget it. If you remember; in python you did not have to end a line with a semicolon or anything. But PHP needs to be told when a statement has ended and when to move to the other. This is also known as a *statement terminator*[^17] (or statement separator). ==Another thing to note when writing PHP code is that, this language is case sensitive==.

>[!important] Note
>
>In PHP, keywords (e.g. `if`, `else`, `while`, `echo`, etc.), classes, functions, and user-defined functions are not case-sensitive.

This means that In the example below, all three [[notes/class-notes/Output#Echo Statement|echo]] statements below are equal and legal

```php
<?php  
ECHO "Hello World!<br>";  
echo "Hello World!<br>";  
EcHo "Hello World!<br>";  
?>
```

>[!warning]
>
However; all [[notes/class-notes/Variables#PHP Variables|variable]] names are case-sensitive!

Though the reserved words[^18] are excepted from this rule, [[notes/class-notes/Variables#PHP Variables|variables]] are not. For example if you had a variable named `$color` you have to explicitly call the same exact spelling; By calling the variable as anything other than that, for example `$Color`,`$coLOR` or `$COLOR` would not return the value of `$color`. this is because PHP treats each of them as a separate variable.

```php
<?php  
$color = "red";  
echo "My car is " . $color . "<br>";  
echo "My house is " . $COLOR . "<br>"; //wont output anything and will thow an error  
echo "My boat is " . $coLOR . "<br>";  //wont output anything and will thow an error
echo "My boat is " . $Color . "<br>";  //wont output anything and will thow an error
?>
```

[^17]: Reference PHP–[Instruction Separation](https://www.php.net/manual/en/language.basic-syntax.instruction-separation.php)
[^18]: a **reserved word** (also known as a **reserved identifier**) is a word that cannot be used as an [identifier](https://en.wikipedia.org/wiki/Identifier_(computer_languages) "Identifier (computer languages)"), such as the name of a variable, function, or **label**– it is "reserved from use". This is a [syntactic](https://en.wikipedia.org/wiki/Syntax_(programming_languages) "Syntax (programming languages)") definition, and a reserved word may have no user-defined meaning.
[^19]: Reference PHP–[Syntax](https://www.php.net/manual/en/language.basic-syntax.phptags.php)
[^20]: Read more–[What is a parser](https://www.techtarget.com/searchapparchitecture/definition/parser#:~:text=A%20parser%20is%20a%20program%20that,out%20of%20the%20pieces%20of%20input)
[^21]: Reference Wikipedia–[Preprocessor](<https://en.wikipedia.org/wiki/Preprocessor#:~:text=a%20preprocessor%20(or,of%20the%20preprocessor%3B>)
[^22]: Reference Wikipedia–[Comparison Of Programming Language Syntax](<https://en.wikipedia.org/wiki/Comparison_of_programming_languages_(syntax)#:~:text=A%20statement%20separator%20demarcates%20the%20boundary%20between%20two%20separate%20statements.%20A%20statement%20terminator%20defines%20the%20end%20of%20an%20individual%20statement.%20Languages%20that%20interpret%20the%20end%20of%20line%20to%20be%20the%20end%20of%20a%20statement%20are%20called%20%22line%2Doriented%22%20languages.>)