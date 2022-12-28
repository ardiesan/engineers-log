---
layout: post
title: "PHP Coding Convention"
author: jdayuday
categories:
- internship
- php
image: assets/images/jdayuday-naming-convention-1.png
---
In programming, there are a lot of traditions in addition to the set of guidelines that each programming language provides, but the vast majority of software developers around the world agree with these sets of standards.

Naming conventions are among the most popular conventions of all. As a programmer, you will name a lot of things, like variables, functions, classes, methods, interfaces, etc.

Developers have named various things in their code using different `case types` over the years. As the world of programming and development grows, these cases have been widely known and used by different people. In this article, we are going to focus on letter cases and the PHP naming convention.


<br>

## what are programming letter cases
While some case types are uncommon in spoken speech, they are often applied in computer programming.

Programmatically, the letter cases in programming languages are parsed. They often use basic whitespace, like tabs, newlines, and space characters, to demarcate their syntactic tokens. When the number of tokens, such as function and variable names, increases during the development of complicated software. It is necessary to maintain the source code understandable by humans, and naming conventions that enable this.

<br>

## Popular programming letter cases
As we've talked about programmers using standard and proper naming conventions in different languages and projects, these are the most popular and used by programmers right now.

### Camel case

What is a camel case? In using `camel case`, you begin a name with a small letter. If a name contains more than one word, the subsequent words will all begin with a capital letter.

`Example of camel cases: greetings and firstName`


<br>

### Snake case

Similar to the camel case, snake case names begin with small letters. If the name consists of more than one word, the later words should all begin with tiny letters, and you should use an underscore `_` to separate them.

`Example of snake case: create_table_user or delete_table_user`

### Pascal case

Names are written in pascal's case and begin with a capital letter, unlike the instances above. All words in names with multiple words will begin in capital letters.

`Example of  pascal case: FirstName and LastName`


### Kebab case

Similar to the snake case, the kebab case separates the words using a hyphen `-` rather than an underscore `_`.

`Example of Keabab case: create-table-user or delete-table-user`

<br>

## Naming convention

What is the naming convention for a programmer? A set of guidelines known as naming conventions are used in programming to determine the character sequences that should be used to identify variables, types, functions, and other things in source code and documentation.

<br>

## PHP naming convention
Now you know what is naming convention let's tackle PHP naming conventions. Coding Standards are crucial for producing high-quality code. We may create a homogeneous code that is simple to understand and maintain by using a uniform visual style, naming standards, and other technical parameters. Rules and code requirements, however, cannot account for all significant aspects.

The way some problems are addressed programmatically is also crucial. The personality and expertise of the particular developer come through and eventually determine whether the code is technically sound or represents a mature, well-thought-out solution.

In coding with PHP, you have to follow the standard guidelines for your code to be readable and easy to understand by another developer (if you are working with a team).

### Here's how!

### Code format and layout
As a developer when coding in the project, for your contribution to be called `beautiful code` you first must follow the visual guidelines which means your code must look similar to other developers working on the same project.

For you to have beautiful code, you must consider the following guidelines set for PHP developers.

-  PSR-2 code formatting.
-  Nearly all PHP files in Flow have exactly one class and produce nothing when called directly. Therefore, you start your file with a `<?php` tag and must not end it with the closing `?>`.
-  PHP developers prefer strict typing, so files should contain a `declare(strict_types=1);` statement. In the strict mode, PHP expects the values with the type matching with the target types. If there’s a mismatch, PHP will issue an error.
-  A header containing namespace and license information is required for each file.

Sample:

```
<?php
declare(strict_types=1);
namespace YourCompany\Package\Something\New;

/*
 * This file is part of your YourCompany.Package package.
 *
 * (c) YourCompany
 *
 * This package is Open Source Software. For the full copyright and license
 * information, please view the LICENSE file which was distributed with this
 * source code.
 */

```

Make sure you use the correct package in the header.

<br>

## Naming in PHP

### Php Variables

Php variable naming convention, but first of all `what is a variable?` variable is what keeps data safe. Any form of data is acceptable, including String, Integer, Floating Point, Boolean, and Arrays.

Declaring variables in PHP, most developers use snake cases for declaring their PHP variables.

**Example of how variable implemented in PHP:**

```
$n1 = “Ana”; // Wrong  
$n2 = “Ivan”; // Wrong

$my_name = “Captain America”; // Wrong  
$my_var = “Captain Jones”; // Wrong

$first_name = “Bruce”; // Right
$last_name = “Banner”; // Right

```

What have you noticed? what's wrong with `$n1 and $n2`? As I've mentioned above it is best practice when dealing with variables, it is important to be descriptive as possible, in that other developers will immediately understand what is the relation of your code to the declared variable.

Let's try another example that you can relate to:

```
$i = “Laptop AcerNitro 5 (8GB, 500GB, 3050Ti)”; 
$p = “899.00”;
$d = "10.00";
$t = “810.00”;
```

As a developer, let's pretend that this is your first time seeing this code, will you be able to know what are things stored in each variable? The answer is no, as for other developers that you will be working with, it is not helpful and your contribution may be disregarded.

Let's try again, but this time let's make it as descriptive as possible for the variable purpose.

```
$item = “Laptop AcerNitro 5 (8GB, 500GB, 3050Ti)”; 
$price = “899.00”;
$discount = "10.00";
$total = “810.00”;
```

Can you see the difference? It is clear that by just properly defining variables correctly it is much easier to understand.

Additional information for variables when working with Strings in PHP, when declaring a string variable with value in it, is an important reminder when you want to concatenate strings, A space must be inserted before and after the dot for better readability of your code.

String example:

```
$message = 'Hello' . $your_name . ', I am' . $my_name . ' Nice to meet you!';
```

<br>

## Whitespace
**`Tabs vs Space` which is better?**

For whitespace in your code, use tabs rather than spaces. Although using tabs rather than spaces may seem like a minor detail, it allows the developer who is reviewing your code to change the indentation level in the application they are using. Additionally, since one tab character is stored rather than, for example, four space characters, it leads to (somewhat) more compact files.

<br>

## Comments
The code should generally be well-annotated. For less experienced programmers, it not only clarifies the purpose and flow of the code, but it may also be quite helpful when revisiting your code months later.

For using PHP and general programming it is advisable to use the Do block style when committing to a block of code, and take note, keep it simple but descriptive enough, to be understood easily by other developers.

Example:

```
/**
 * Super Class
 *
 * @package     Package Name
 * @subpackage  Subpackage
 * @category    Category
 * @author      Author Name
 * @link        http://example.com
 */
class Super{
}

```
<br>

## Php Functions
`What is a function?` A piece of code known as a function performs a certain purpose. There are several functions in each programming language, each of which performs a particular purpose.

In defining functions in PHP, there are two of the majority of developers used: lower snake case and camel case

**Example of how functions are implemented in PHP:**

Lower snake case:

```
function get_name(){
  // Do something
}
```

Camel case:

```
function getName(){
  // Do something
}
```

In declaring a function you can choose between the two shown above, but depending on your team you might just follow what case they are using when creating a function.

An important reminder when you are working with a function it is important to keep in mind that a function should always start with a `verb` which means universally that functions are created to change the state `entity` of your program.

An additional example for PHP function declaration:

```
writeMsg() // Right
namesList() // Wrong
familyName() // Right
sendEmail() // Right
deleteUserById($id) // Right
connectToDatabase() // Right
databaseConnection() // Wrong
prepareOutput() // Right
```

<br>

## Php Class Methods
PHP Class Method is simply a function but inside a class. The class keyword is used to define a class, which is then followed by the class name and two curly brackets `{}`. Inside the brackets are all of its attributes and operations.

This is how you define a class in PHP:

```
<?php
class Pet{
  // code goes here...
}
?>
```

When you are naming a class in PHP it is advisable to use `Pascal Case` with `_` as a separator, which most PHP developers do it.

Additionally, when working with variables and properties in a class it's important to remember  that both `private and protected` inside must be declared with `_` (underscore) such as:
```
<?php
class Circle{
  // code goes here...
  
  public PI = 3.14;
  private $_radius; 
  
  private function _calculateArea(){
   return self::PI * $_radius * $_radius;
  }
  
}
?>
```

<br>

## Importing Namespaces
When importing the namespace using the `use` statement makes your code more readable, and you refer to other classes or interfaces, you should do so. For each imported namespace, there is one use statement per line.
Additionally, it is advisable to alphabetically order your imported namespaces.

Example:

```
namespace App\Actions\Fortify;

use App\Models\User;
use Illuminate\Support\Facades\Hash;
use Illuminate\Support\Facades\Validator;
use Laravel\Fortify\Contracts\CreatesNewUsers;
use Laravel\Jetstream\Jetstream;
```


<br>

## PHP curly braces
Every developer has preferences in using parenthesis in their program. The majority of developer only uses to parenthesis format which widely uses.

K&R style format:

```
<?php
class Pet{
  // code goes here...

  
  public function printTable(){
   return;
  }
  
}
?>
```

<br>

Allman style format:

```
<?php
class Pet
{
  // code goes here...

  
  public function printTable()
  {
   return;
  }
  
}
?>
```

which is better than the two? honestly, as I've mentioned above, it depends, on whom you are working with on your project. The k&R is designed for a compact look of code, but Allman is better for reading codes.


## When should I use the naming convention?
When should I use the naming convention as a programmer? The answer to that is "always" even though is it not required if you are working by yourself creating your project. Things will change if you are working with other people on the same project.

I know that each of us is unique, and we come from various backgrounds. For others, one might define something very differently. More than that, various cultures have distinct ways of describing the same things.

Experience and countless hours of coding sessions and reading are necessary when choosing the appropriate name for a function or variable, etc. It is important when working with a group of people to follow specific guidelines for the project, not only make you a better developer it also helps to lessen the burden of another developer in reading and understanding your code.

<br>

## Benefits of using a naming convention

List of benefits of using a naming convention for your PHP projects, not just PHP but also in other languages and projects.

- Easier to read and comprehend source code.
- To make it possible for code reviews to concentrate on topics more crucial than syntax and naming conventions.
- To allow code quality review tools to concentrate their reporting primarily on important issues other than syntax and style preferences.


## Summary
To make it simple the importance of naming convention as a developer. I've mentioned above many times it lessens other developer time in understanding and reading your code, especially for those newcomers, which will be boarding on your projects.

It is important to follow certain guidelines which will enable you and other developers in your team to produce better and quality code. Additionally, many companies already have their code guidelines, and it's best practice to follow those guidelines for you to contribute quality code.
