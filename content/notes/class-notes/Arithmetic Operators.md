---
title: "Arithmetic Operators"
tags:
- ict
- operator
enableTOC: true
---

## PHP Arithmetic Operators
The [[notes/class-notes/php|PHP]] arithmetic operators are used with numeric values to perform common arithmetical operations, such as addition, subtraction, multiplication etc. 

| Operator | Name           | How To     | Example       |
| -------- | -------------- | ---------- | ------------- |
| `+`      | Addition       | `$x + $y`  | $5 + 2 = 7$   |
| `-`      | Subtraction    | `$x - $y`  | $5 - 3 = 2$   |
| `*`      | Multiplication | `$x * $y`  | $5 * 2 = 10$  |
| `/`      | Division       | `$x / $y`  | $5 / 2 = 2.5$ |
| `%`      | Modulus        | `$x % $y`  | 5 % 2 = 1     | 
| `**`     | Exponentiation | `$x ** $y` | $5 ** 2 = 25$ |

>[!tldr] Note
>
>Unlike the python division operator, The division operator in PHP does not always return floating numbers!

>[!tip] More 
>
>In PHP there is no operator for integer division like you’re used to in python with the `//` operator. In-order to achieve this in PHP you have to use a function called `intdiv()`. Apart from this function, there is no built in function to accomplish this.
>**Function Description**
>```php
>intdiv(divided,divisor);
>
>//example
>
>intdiv(5,2); //outputs 2
>```
