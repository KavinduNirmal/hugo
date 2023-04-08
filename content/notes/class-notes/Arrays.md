---
title: "Datatype | Array"
tags: 
- ict
- datatype
enableTOC: true
---
# Array

An array[^23] is a variable with multiple data. The simplest explanation is that an Array is in a way similar to a train. The carriages resemble a space for a single data. Normally you would store data in a single variable, but there are instances where you have a list of data with a common ground, for example thinks of a list of cars. You cannot go about creating a variable for each car. In these instances, arrays come in handy. 

## PHP Array

In [[notes/class-notes/php|PHP]] arrays are created with the `array()` function. With that you will use `(`for the start of the array and separating each data with a comma `,` and when you want to close the array you will use the `)`. 

For example lets think of F1 teams.

```php
$f1_teams = array("Red Bull", "Mercedes", "Ferrari", "McLaren", "Aston Martin");
```

With the `array_dump()` function it will output the following:

```txt
array(1) {
  [0]=>
  array(5) {
    [0]=>
    string(8) "Red Bull"
    [1]=>
    string(9) "Mercedes"
    [2]=>
    string(7) "Ferrari"
    [3]=>
    string(7) "McLaren"
    [4]=>
    string(12) "Aston Martin"
  }
}
```

>[!todo] Note
>
>You might have already noticed that in the above `var_dump()` function, when outputting the data, it created a list with `0-4`, But we didn’t specify any of those, This is because, arrays have something called an index.
>An index meaning a way for the computer to remember where the data is sorted. Imagine an index like the list of chapters of a book with where the page number is, otherwise you would not be able to find the chapter you’re looking for so easily and have to look through every page. And computers really don’t like wasting time, nor do we. So the processor keeps a tab on where it stored our data. Like on the above array, the computer knows “Mercedes” is in the `$f1_teams` variable in the `1` index.
>>[!success] Tip
>>
>>You might realize the index starts with 0. This is because an array is a pointer, and the index is used as the offset. The first element of the array is precisely at the pointer's memory location; therefore, the offset is zero. The second memory location is one slot further, hence the 1.[^22]

>[!tip] Note
>
>Arrays necessarily doesn’t need to be a single data type. You can add multiple data types in a array.
>Example:
>```php
>$ferrari = array(“Ferrari”, 2.8, 278, true);
>```
>Which will result the following output:
>```txt
>array(1) {
>  [0]=>
>    array(4) {
>     [0]=>
>       string(7) "Ferrari"
>     [1]=>
>       float(2.8)
>     [2]=>
>       int(278)
>     [3]=>
>       bool(true)
>  }
> }
>```

You can also **indented Arrays** too! But what does it means? Well ==indented array is an array within an array== And there’s no limit on how many times you can indent arrays just like a Russian doll. But its not recommended to indent a lot of arrays.

An array works as a a train, as said above, within that train, a carriage represents a cell. A array within an array means a cell contains another array, Just like a cargo carriage have boxes, each box representing data. 

![Array Explenation](notes/images/Array-Explenation.svg)

You can indent arrays within arrays like stated before. But there’s a complication when calling the said arrays. Normally you can call the array with a `echo` statement. However you will not be able to accomplish that for the second array as its nested within a cell. ==This is because the second array is again indexed[^24] starting from== `0`. 

If we turn that array into a list it might look like this:

```txt
$Array
	0. 20
	1. 10.5
	2. Hello
	3. True
	4. 
		0. 10
		1. 20
		3. 30
```

As you can see we have created an array with the variable name of `$Array1`, which have 5 cells, each containing the data of `20, 10.5, "Hello", True` and lastly another array. How can we create this array in php? As follows:

```php
$Array1 = array(20, 10.5, "Hello", true, array(10,20,30));
```

After creating, How do we access the data this array? Well if we use the `var_dump()` function on the entire array as shown in the above diagram you’ll get the entire array, even with the details of the indented array.

```txt
array(1) {
  [0]=>
  array(5) {
    [0]=>
    int(20)
    [1]=>
    float(10.5)
    [2]=>
    string(5) "Hello"
    [3]=>
    bool(true)
    [4]=>
    array(1) {
      [0]=>
      array(3) {
        [0]=>
        int(10)
        [1]=>
        int(20)
        [2]=>
        int(30)
      }
    }
  }
}
```

To get a data of a specific cell you’ll have to use the `echo` statement with the index number, Like `echo $Array1[1]` which will return `10`.

```php
echo $Array1[1];
//outputs 10
```

As for the indented array you cannot simply say `echo $Array[4]` because this will throw an error. This is because as I stated above that the new array starts with the index of `0`. so to access the array you’ll have to use the following.

```php
echo $Array1[4];
//outputs an error

echo $Array1[4][0];
//outputs 10
```

This means that you can get the full data set of an array that is indented; you will have to use the `var_dump()` function. But this does not restrict you from using the echo function to get a single value of the indented array.

>[!warning] Caution
>
>Can you access the second data in the indented array with the following way?
>```php
>echo $Array1[4][0][1][2][3];
>```
>**No**. This is because if you remember in the indentation we used `echo $Array1[4][0];` Which the computer understood as; “Go to the array named `$Array1` and go to the 4th index and the 0th index of that array and fetch me that data.” which means the computer followed the statement as: `$Array1` → `index 4` → `index 0`. 
>But in the above script we are telling the computer to find the array go to its 4th index, then the 0th index of that, then the 1st index of that and the 2nd index of that and so on. But as you know we do not have that many nested elements, well this results an error. 
>This is easy to get confused on but keep in mind that *We are passing the location of the data we are trying to fetch, the above script might look like a “and” as in [0] and [1] and…etc. But the computer understand it as a “in”. Like [0] in [4]* 

[^23]: Reference W3schools–[Arrays](https://www.w3schools.com/php/php_arrays.asp)
[^24]: Reference gimtec–[Array Index](https://www.gimtec.io/articles/why-do-array-indexes-start-at-0/)