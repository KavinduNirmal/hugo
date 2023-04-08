---
title: "Datatype | String"
tags:
- ict
- datatype
enableTOC: true
---

## PHP String

A string is a  sequence of Unicode characters surrounded by single `''` or double `" "` quotation marks.

Example:
```php
"Hello", "World", "M@il", "සිංහල"
```

>[!Note] 
>
>[[notes/class-notes/php|PHP]] supports all Unicode characters within a string. Even emojis!
>```php
>$string = "🎁";
>echo $string;
>```

To create a variable with a string, simply surround the data within quotation marks.

```php
$name = "Herath";
```

You can get the help of a function called `var_dump()`[^23] to get even more details about a [[notes/class-notes/Variables#PHP Variables|variable]]. This function will display the type of the variable passed through. Outputting the type, the data and the length.

```php
var_dump($value);
```

example:

```php
$name = "Herath";
var_dump($name);

// outputs
// string(6) "Herath"
```

[^23]: Reference PHP–[Var dump](https://www.php.net/manual/en/function.var-dump) 