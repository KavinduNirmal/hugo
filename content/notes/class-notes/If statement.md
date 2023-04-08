---
title: "IF conditional Statement"
tags:
- ict
enableTOC: true
---

# IF Condition

The if statement **allows you to control if a program enters a section of code or not based on whether a given condition is true or false**. One of the important functions of the if statement is that it allows the program to select an action based upon the user's input.

## Python If Statements
There are 5 types of If conditional statements in Python.
1. *If*
2. *If - else*
3. *nested If-else*
4. *If - elseif - else*
5. *switch*

### Python If Statement
If condition can be used to execute a set of instructions only if the specified conditions are met. If the specified conditions are not met, the instructions inside the statement will be neglected.

```python {tytle="Python"}
x = 5
if (x>0):
	print("Hi!")
```

### Python If Else Statement

This statement allows you to provide an alternative set of instructions to the compute if the given conditions are not met. The two options are when the conditions are true or false.
The computer will always chose one side of them and neglect the other.

```python {title="Python"}
k = -5
if ($k>0):
	print("Im true!")
else:
	print("Im false!")
```


## PHP If Conditional Statements
There are 5 types of If conditional statements in PHP.
1. *If*
2. *If - else*
3. *nested If-else*
4. *If - elseif - else*
5. *switch*

### PHP If condition
If condition can be used to execute a set of instructions only if the specified conditions are met. If the specified conditions are not met, the instructions inside the statement will be neglected.

```php {title="PHP"}
<php
$k = 5;
if($k>0){
echo "Hi!";
}
?>
```

>[!warning] Note
>
>Though in python indentation is necessary in php it is not. The difference between both is instead of the semicolon php uses curly brackets `{}`. It is as if `if(condition){execute whats inside of me}` keep in mind, that even though we read the code as multiple lines, the compiler sees it as a single line with no fancy style.

### PHP if else

This statement allows you to provide an alternative set of instructions to the compute if the given conditions are not met. The two options are when the conditions are true or false.
The computer will always chose one side of them and neglect the other.

```php {title="PHP"}
$k = -5;
if ($k>0){
	echo "Im true!";
} else {
	echo "Im false!";
}
```

### PHP nested if else
Using if else structure inside another if else structure is known as nesting.
This can be used when there is more than two choices in the conditional statement.
The checking condition should be broken into several boolean conditions to implement this.

```php {title="PHP"}
<?php
$marks = 80;
if ($marks >=75){
	echo "A!";
} else {
	if ($marks >= 65){
		echo "B!";
	} else {
		if ($marks >= 55){
			echo "C!";
		} else {
			if ($marks >= 35){
				echo "S!";
			} else {
				echo "W!";
			}
		} 
	}
}
?>
```

>[!warning] Warning
>
>Using this method for more than 5 nested statements is not healthy[^1] as it adds up to the processing time. In times like this it is better to switch to small portion of statements or use switch statement instead



### PHP if elseif else

This is a shorthand version of nested if else. it is the same concept but trimmed down the 
unnecessary clutter.

```php {title="PHP"}
<?php
$marks = 80;
if ($marks >= 75){
	echo "A";
} elseif ($marks >= 65){
	echo "B!";
} elseif ($marks >= 55){
	echo "C!";
} elseif ($marks >= 35){
	echo "S!";
} else {
	echo "W!";
}
?>
```

### PHP Switch statement

```php {title="PHP"}
<php
$favcolor = "red";
switch ($favcolor){
	case "red":
		echo "color red!";
		break; // telling the compiler to skip to the end
	case "blue":
		echo "color blue!";
		break;
	case "green":
		echo "color green!";
		break;
	default: // the default output if all conditions are false
		echo "Your color is neither red, blue or green";
}
```

[^1]: Read [more on why repeated conditional statements are bad](https://wpshout.com/unconditionally-refactoring-nested-statements-cleaner-code/#gref)