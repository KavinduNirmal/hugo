---
title: "Comments"
tags: 
- ict
enableTOC: true
---

## Comments

Comments are a way of telling the compiler[^13] of a programming language to skip a specific section of the code, which results that part of the code to not being executed by the program. It is only used by someone who is looking at the source code as the computer wont see it at all. 

Typically comments are used for mainly to ==let others understand your code==. This is because not everyone can understand each others code. It also helps to communicate with your colleagues or collaborators while working on a project, you can see this really helpful when contributing to open-source projects.

And also ==reminding yourself what you wrote will do==–Most programmers have experienced coming back to their own work a year or two later and having to re-figure out what they did. Comments can remind you of what you were thinking when you wrote the code. 

Another way of using comments if for debugging, to find where a bug is or to temporarily exclude a section of a code without deleting it.

## PHP Comment types
[[notes/class-notes/php|PHP]] supports multiple ways of comments.[^14]
1. Single line comment: `//` or `#`

```php
<?php  
// This is a single-line comment  

# This is also a single-line comment  
?>
```

>[!tip] Tip
>
>The "single-line" comment styles only comment to the end of the line or the current block of PHP code, whichever comes first. This means that [[html|HTML]] code after `// ... ?>` or `# ... ?>` WILL be printed: `?>` breaks out of PHP mode and returns to HTML mode, and `//` or `#` cannot influence that. Reference the example below;
>```php
><h1>This is an <?php # echo 'simple';?> example</h1>
><p>The header above will say 'This is an example'.</p>
>```

2. Multiline comment: `/* */`
   
```php
<?php  
/*  
This is a multiple-lines comment block  
that spans over multiple  
lines  
*/  
?>
```

>[!Caution] Caution
>
>Another thing to keep in mind while creating these types of comments is to not to nest them, as they will cause you some great pain when trying to debug.
```php
<?php  
/*  
echo 'This is a test'; /* This comment will cause a problem */  
*/  
?>
```

3. Inline comment *← Special case, uses the same [[notes/class-notes/syntax|syntax]] as multiline comment* `/* */`

```php
<?php  
// You can also use comments to leave out parts of a code line  
$x = 5 /* + 15 */ + 5;  
echo $x;  
?>
```

You might realize that PHP also supports `#` as a way to start a comment. Just like in [[notes/class-notes/python|python]]. If you want to here are a reminder of what other languages used for comments.

| Language | comment-type            | Syntax                      |
| -------- | ----------------------- | --------------------------- |
| PHP      | Single Line             | `# comment` or `// comment` |
|          | Multi Line & Inline     | `/* comment */`             |
| Html     | Single Line & Multiline | `<!-- comment -->`          |
| CSS      | Single Line & Multiline | `/* comment */`             |
| Python   | Single Line & Multiline | `# comment`                 |
| SQL      | Single Line             | `--comment`                 |
|          | Multiline               | `/* comment */`             |

>[!todo] Little bit of fun
>
>Sometimes you can check out what some of the websites have commented using `inspect` feature on web browsers. This can also be used for debugging. You can access this by simply clicking `F12` or `[Right click]` → `inspect` 

[^13]: Reference Wikipedia–[Compiler](https://en.wikipedia.org/wiki/Compiler)
[^14]: Reference PHP–[Comments](https://www.php.net/manual/en/language.basic-syntax.comments.php)