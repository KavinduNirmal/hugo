---
title: "Datatype | Integer"
tags:
- ict
- datatype
enableTOC: true
---
# Integer
A [[notes/class-notes/Integer|integer]] is a variable with numbers ( non-decimal ).

## PHP Integer / Int
Rules for integers in [[notes/class-notes/php|PHP]]:

-   An integer must have at least one digit
-   An integer must not have a decimal point
-   An integer can be either positive or negative
-   Integers can be specified in: decimal (base 10), hexadecimal (base 16), octal (base 8), or binary (base 2) notation

In the following example `$x` is an integer. The [[notes/class-notes/php|PHP]] `var_dump()`[^1] function returns the data type and value:

```php
<?php  
$x = 5985;  
var_dump($x);  
?>
//int(5985)
```

[^1]: Reference PHP–[Var dump](https://www.php.net/manual/en/function.var-dump)