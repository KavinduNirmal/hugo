# Variables

Variables[^15] are containers to store information in a computer memory temporarily; for the duration of the program is running. 

The book definition is:
>[!todo] Definition
><mark style="background: #FFB8EBA6;">A variable is a named unit of data that is assigned a value.</mark> If the value is modified, the name does not change. Variables are used with most programming languages and come in many forms, defined by the script or software programmer.

Some variables are mutable, meaning their values can change. Other variables are *immutable*, meaning their value, once assigned, cannot be deleted or altered.

If a variable's value must conform to a specific data type, it is called a *typed variable*.

![memory explenation](notes/images/memory-explenation.svg)

Variables are used to store a repeating value or values that needs to be remembered by the computer program to use later in the program. 

By declaring a variable we take a slot in the computer memory to store some data to use later. But why do we use variables? cant we write these things down? This question might pop into your head. 

The reason we use variables is that we are trying to create a structure. To create a program that process and do something, But we cannot always predict what will happen in the future or what could be changed. This is why we need to flexible and our code to be easily changed. 

Variables are things that can change, for example think about a computer program for marking attendance. What do we need to know? The number of the students and who came to school today. Now imagine if we didn’t have variables. You’d have to write all the names by yourself again and again, this is ineffective. But imagine you had a variable named students and a variable named attendees. You can easily change these without any problems. You can even use this program in a office or any other place without any issues as you only have to change the variables and the rest of the programs will work as normally.

>[!hint] The more you know
>
>In programming to see if something is equal we use double equal signs " == " or '' === '' in some cases. You’ll learn about it in the future!

Variables also have something called [[notes/class-notes/Variable scope|Variable scope]] it determines where can a variable be called.

## PHP Variables

In-order to create (declare) a variable in [[notes/class-notes/php|PHP]] you have to follow few rules. These are similar to the rules while declaring python variables, but some extra rules have been added.
1. A variable name can only contain letters `A-Z`, digits `0-9` and underscores `_`.
   - No other special characters are allowed `!,@,#,%,^,&` etc.
   - An identifier can be any length,
2. A variable ==name cannot start with a number==.
   - It can be started with a letter or underscore, but the first letter cannot be a number.
3. ==PHP is case sensitive ==on variable names.
   - hello, Hello and HELLO are not the same.
4. A variable **must** have a `$` ==dollar sign in-front of the name== / identifier.
5. A variable ==cannot be named after a reserved keyword==[^16].

```php
$variableOne = "PHP";
$_variable2_ = 1995;
$a = 10.5;
$B = "1690";
```

After the execution of the above statements `$variableOne` would have the value of `"PHP"` and `$_variable2_` the value of `1995`. Unlike other programming languages; PHP does not have a command for declaring variables. It is created the moment you assign a value to it. 

- checkout [[notes/class-notes/Variable scope#PHP Variable scope|PHP Variable scope]]

>[!example] Keep in mind
>
>When you assign a text value to a variable, put quotes around the value. 

[^16]: a **reserved word** (also known as a **reserved identifier**) is a word that cannot be used as an [identifier](https://en.wikipedia.org/wiki/Identifier_(computer_languages) "Identifier (computer languages)"), such as the name of a variable, function, or **label**– it is "reserved from use". This is a [syntactic](https://en.wikipedia.org/wiki/Syntax_(programming_languages) "Syntax (programming languages)") definition, and a reserved word may have no user-defined meaning.