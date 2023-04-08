---
title: "Assignment Operators"
tags:
- ict
- operator
enableTOC: true
---

## PHP Assignment Operators
The [[notes/class-notes/php|PHP]] assignment [[notes/class-notes/Operators|operators]] are used with numeric values to write a value to a variable.

The basic assignment operator in PHP is `=`. It means that the left operand gets set to the value of the assignment expression on the right.

```php
$x = 10
```

>[!warning]
>
>using `=` **does not** means `x` is equal to `10`. instead in programming, `=` is used to say, the value of the right side is what this value holds. 

![Assignment Operator|350](notes/images/assignment-operator-explenation.svg)

The output would be 6 because; first we assigned 5 to `$x` meaning until it is used or changed, value of `$x` holds the value of 5. Then in the next line we told PHP that; add `+1` to the current value of `$x` and assign the new value to `$x`. If a mathematician saw this they would scream because well in mathematics, "=" means both sides are equal. **But this is not mathematics**! In programming "=" ==is not equal but considered as a reference!==

>[!tip]
>
When reading a or executing assignment operator, read from right to left!

>[!abstract] Hard to understand?
>
>If its still hard to understand imagine this; you have three friends, A, B and C. You have a bag of Oranges, Apples and Bananas. Since you don’t need them right away, you say to A, “hey! can you hold these oranges till I need them?”, And you give A the oranges,  B the apples and C the bananas. 
>Then when you need the apples back, you call your friend B and say “Hey can you give me what I gave you?” and B hands you the Apples. It is the same concept. Your friend B is not an apple, they are just holding onto what you gave them!
>```php
>$A = "oranges";
>$B = "apples";
>$C = "bananas";
>```
>So by that, If B had 10 apples and you gave them another, Now B have another apple meaning now they have 11 apples!
>```php
>$B = 10;
>$B = $B+1;
>//outputs 11!
>```
