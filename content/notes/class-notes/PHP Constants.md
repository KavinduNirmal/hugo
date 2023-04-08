---
title: "PHP Constant"
tags:
- ict
- php
- datatype
enableTOC: false
---

# PHP Constants

PHP constants are similar to variables, however; ==once they are defined. It cannot be changed or undefined== in another section of the document. A constant is an identifier (name) for a simple value. The value cannot be changed during the script.

>[!important]
>
>A valid constant name starts with a letter or underscore (no $ sign before the constant name).

>[!note]
>
>Unlike variables, constants are automatically global across the entire script.

In-order to create a constant we will use the built in function of php `define()`.[^19]

Normal:
```php
define(name, value, case_insensitive);
```


Detailed:
```php
define(string $constant_name, mixed $value, bool case_insensitive = false): bool
```

The define function expects three parameters
1. name 
	- **Type: String**
	- The name of the constant

> [!note]
>It is possible to **define()** constants with reserved or even invalid names, whose value can (only) be retrieved with [constant()](https://www.php.net/manual/en/function.constant.php). **However, doing so is not recommended.**
2. value
	- Type: Mixed
	- Mixed values means, constants accept any type of value, `string`, `int`, `boolean` or even `arrays`.
3. case_insensitive ← **Has been deprecated**!

>[!warning]
>
>In PHP 8.0.0 Passing **`true`** to `case_insensitive` will emits an **`E_WARNING`**. Passing **`false`** is still allowed.
This is because in PHP version 7.3.0 `case_insensitive` has been deprecated and was removed in version 8.0.0.

How to use `define()` to create a constant:

```php
define("length",100);
define("greeting", "Hello World!");
echo length; //outputs 100
echo greeting; //outputs Hello world
```

Another thing to keep in mind is that ==constants are always global==.

```php
define("greeting", "Hello World!");

function greet() {
	echo greeting;
}

greet();
```

>[!success] Tip
>
>When naming constants make it a habit to always use Uppercase letters as the name. This is not a rule in the book but a industry standard.
>```php
>define("NAME", "Sri Lanka")
>```

## PHP Constant Arrays
You can also create arrays inside a constant[^18]. This is similar to Lists in Python. To create a Constant Array try following:

```php
define("mobile_phones", ["Apple","Samsung","Huawei"]);
```
In-order to access the data within you have to call each index one by one as `mobile_phones[0]` otherwise if you try to call it just by a single `echo mobile_phones;` it will throw an error:

```php
echo mobile_phones;

// output
// Warning: Array to string conversion in /home/user/scripts/code.php on line 4
// Array

echo mobile_phones[0];
// outputs Apple
```

[^19]: Reference PHP–[Constant](https://www.php.net/manual/en/function.define)