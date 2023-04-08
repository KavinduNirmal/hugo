---
title: "PHP"
tags: 
- ict
- php
---

# What is php?

PHP stands for `Hypertext Preprosessor`, is a widely-used ==open source general-purpose scripting language== that is especially suited for web development and can be embedded into HTML.

PHP is written inside of a normal html template, But instead of the file extension being `index.html` when creating a php file it should end with the extension of `index.php`. Php can be injected anywhere within `<body>` tag, it has no restrictions as `<script>` tag. 

```php {title="index.php"}
<!DOCTYPE html>  
<html>  
<head>  
<title>Example</title>  
</head>  
<body>  
  
<?php  
echo "Hi, I'm a PHP script!";  
?>  
  
</body>  
</html>
```

>[!tip] Note
>
>PHP parser recognizes the tag `<? php -- ?>` as the injected php. We use this tag to write down the php scripts.

## Use case of PHP
PHP Is used for many different scenarios. But mainly it is used for server side scripting. More info [@php](https://www.php.net/manual/en/intro-whatcando.php). But following are the 3 main use cases of PHP.

- **Server-side scripting**. This is the most traditional and main target field for PHP. 
- Command line scripting. 
- Writing desktop applications. ← Not the best case.

>[!info] Tip
>
>In A/L only server side scripting is focused on, if you’re interested in more details about the second and third use case, you can check out the details [here](https://www.php.net/manual/en/intro-whatcando.php#:~:text=Command%20line%20scripting,for%20more%20information.) and [here](https://www.php.net/manual/en/intro-whatcando.php#:~:text=Writing%20desktop%20applications,PHP%2DGTK%2C%20visit) respectively.

## Get started
In order to start with Server-side scripting with PHP; You need three things: the PHP parser (CGI or server module), a web server and a web browser. You need to run the web server, with a connected PHP installation. 

You can access the PHP program output with a web browser, viewing the PHP page through the server. All these can run on your home machine so check the [installation instructions](https://www.php.net/manual/en/install.windows.php) from PHP for information on getting started. 

### Setting Up
1. Start the XAMPP server on your PC as stated on the installation guide, 
	1. **XAMPP** is a popular all-in-one development environment for php, MySQL and others.
	2. Download it through [here](https://www.apachefriends.org/) and it will automatically install and set up a development server for you.
	3. If it was hard to follow along you can reference the following links for simple step by step instructions. 
		- [Install php](https://www.geeksforgeeks.org/how-to-install-php-in-windows-10/) 
		- [Install XAMPP](https://www.geeksforgeeks.org/how-to-install-xampp-on-windows/?ref=rp)
		- [Executing PHP through XAMPP Server](https://www.geeksforgeeks.org/how-to-execute-php-script-in-website-using-xampp-webserver/?ref=rp)

2. Go to the following file path `xampp/htdocs/gfg/` and create a file named `index.php` and insert the following code.

```php
<!DOCTYPE html>  
<html>  
<body>  

<h1>My first PHP page</h1>  
  
<?php  
echo "Hello World!";  
?>  
  
</body>  
</html>
```

3. Open your browser and go to the path of `localhost/gfg/index.php`.
>[!tldr] Note
>
>The file name does not have to be named `index.php` , You can name it as any name you desire, but when you access the file through the browser you’ll have to enter that name as the URL like `localhost/gfg/[your-file-name].php`

| Notes                                   | tag |
| --------------------------------------- | --- |
| [[notes/class-notes/syntax#PHP Syntax]] | ict | 
| [[notes/class-notes/Output#PHP Output]] | ict | 
| [[notes/class-notes/Operators#PHP Operators]] | ict | 
| [[notes/class-notes/Datatypes#PHP Datatypes]] | ict | 
| [[notes/class-notes/Comments#PHP Comment types]] | ict | 
| [[notes/class-notes/Variables#PHP Variables]] | ict | 