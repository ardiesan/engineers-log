---
layout: post
title: "ORM - Eloquent Relationships"
author: nsagnoy
categories:
- internship
- eloquent
- relationships
- orm
image: assets/images/entity_relationship_diagram.png
---

The increasing complexity of SQL queries with the growing database size is a struggle for developers, especially when using object-oriented programming (OOP) languages where it is hard to align the programming code with the relational database structure.
Object-relational mapping (ORM) comes into the picture by providing a framework that connects these two various approaches to organizing and storing data.

### What is ORM (Object-Relational-Mapping)?

When interacting with data in the database you may perform different operations to it such as `Create`, `Read`, `Update` and `Delete`.
By default, developers utilizes SQL for executing these operations in a relational database. However, there are instances wherein SQL queries becomes complex and hard to implement. 
Thus, inorder to simplify the interaction between relational databases and oop language, ORM was developed.

ORM is a programming mechanism for efficiently mapping application model objects to the corresponding database tables.
It is a technique used in forming a **"bridge"** between OOP programs and relational databases.

Simply put, you can think of ORM as a middleman or a middle layer that connects object-oriented programming to relational databases.


### Why you need to use ORM?

When linking a database to an application, object-relational mapping technologies enable developers to automate object-to-table and table-to-object data conversion with a minimum of SQL knowledge. 
By focusing on creating business logic, developers can overcome the difficulties of writing and understanding complex SQL queries and achieve increased productivity at lower development and maintenance costs.

<br>

## Eloquent - ORM for PHP Laravel
Eloquent is an ORM tool for Laravel designed to facilitate handling of database records by representing data as objects. 
It serves as a layer of abstraction on top of the database engine utilized to store an application's data/information.
The process of interacting with database tables is made easier by Eloquent, which offers an object-oriented method for adding, updating, and removing database entries as well as a streamlined interface for running sophisticated SQL queries.


There are various features Eloquent offers such as models, relationships, collections, etc. However, in this article, we will focus more on Eloquent Relationships. 
A prerequisite for eloquent relationships is `Model`. To know and learn about Eloquent Model check laravel page: [Eloquent Model - Laravel](https://laravel.com/docs/9.x/eloquent).

### What are database relationships?

To better understand, let us first learn **what exactly is a relationship?**
A relationship, in database, means that two or more tables in the schema are related to each other.
This is done by creating a foreign key column to table_no.2 that reference a column (most likely its primary key) of table_no.1.
For example, you have a `students` table, and each student is enrolled to multiple `subjects`. How would you connect the two?
Usually this is done by adding a `student_id` column in the `subjects` table, so that you can easily identify that a student is enrolled to a specific subject.
This connection that allows you to easily figure out which record is connected to another, is called **"Relationship"**.

<br>

## Types of Eloquent Relationships
### 1. One to One
The most simple relationship is the "one-to-one" relationship.
It is a "Has One" or "One-to-One" relationship. This means that a certain record is related to another record but not multiple other records.

For example, we have two tables: `employee` and `computer` table.

<img src="{{ site.baseurl }}/assets/images/one-to-one.png" alt="one-to-one ERD example" width="800px">
As shown above, visually we see a one-to-one line that connects the employee and computer table (vice versa). 
This indicates the exclusive relationship between the two table. Meaning, an employee can have or possess one computer and a computer can only be owned by one employee in the company.

To define a `one-to-one` relationship in Laravel, we need to place `computer` method in the `Employee` model. The `computer` method should call
the `hasOne` method which takes in two argument: 1. `Computer` class, 2. `computer_ID` foreign key and then return its result.

<img src="{{ site.baseurl }}/assets/images/one-to-one-example.png" alt="one-to-one hasOne example" width="800px">

#### Defining Inverse of One-to-One
Now that we can access our `Computer` model from our `Employee` model. 
Now, let us do the same and define the relationship on the `Computer` model that will let us access the `Employee` that owns the computer.
To inverse, we need to use `belongsTo` method.

<img src="{{ site.baseurl }}/assets/images/belong-to-example.png" alt="one-to-one belongsTo example" width="800px">


### 2. One to Many
When one model owns any number of additional models, the relationship is referred to as "one-to-many". 
For example, a blog post, for instance, might receive an infinite number of comments. 
One-to-many relationships are defined, by adding a `hasMany` function to your Eloquent model. 

<img src="{{ site.baseurl }}/assets/images/one-to-many-has-many.png" alt="hasMany example" width="800px">
In this example, we did not pass a name of the foreign key since actually eloquent will automatically determine the proper foreign key column on the Comment model. 
If you wish to override this convention, you may pass a second argument of a foreign key.

#### Defining Inverse of One-to-Many
Like what we did with `One-to-one`(inverse). We also need to use the `belongsTo` method in the `One-to-Many` relationship (inverse).

 <img src="{{ site.baseurl }}/assets/images/one-to-many-inverse.png" alt="one-to-many inverse" width="800px">

Once the relationship has been established, we can use the `comments` property of post to access the collection of comments and also get the specific post where the comment belongs to by using the `post` property of comment.
```
// comments property
    $post = App\Post::find(1);
    echo $post->comments;
     
// post property
    $comment = App\Comment::find(1);
    echo $comment->post;
```


### 3. Many to Many
Much more complex than `hasOne` and `hasMany` relationships are `many-to-many` relationships.
An example of such a relationship is a user with many roles, where the roles are also shared by other users. For instance, a lot of users might hold the "Admin" role. 
`Users`, `roles`, and `role_user` are the three database tables required to define this relationship. 
The `user_id` and `role_id` columns are found in the `role_user` table, which was created using the eloquent model names in alphabetical order.

You might be thinking, **what is the purpose of the third table, "role_user"?**

Consider the following `many-to-many` relationship: each `User` can have many `Roles`, e.g. a user can be an `admin` and `editor` at the same time, and each role can belong to multiple `Users`.
What can we do with it? We cannot just add a role_id on the users table, because there are potentially multiple roles. And neither can we add a user_id on the Role model, because there are potentially multiple users as well.
To fix this, we require some form of intermediary table. The name of this intermediary table is a **"pivot table"**, and in most instances, its only purpose is to store two ids in the same row.

In our `Pivot Table`: `role_user`, we add columns: `id`, `user_id`, and `role_id`. Both `user_id` and `role_id` are foreign keys that reference to tables: `Users and Roles`.

**Note:** Eloquent will join the two linked model names in alphabetical order to get the table name of the relationship's joining table. Hence, the third table name `role_user`.
You may choose to disregard this custom, though. You can achieve this by providing the belongsToMany function with a second argument of the custom table name.

#### Defining Many-to-Many
Many-to-many relationships are defined by writing a method that returns the result of the `belongsToMany` method. 
For example, let's define the `roles` method on our `User` model:

<img src="{{ site.baseurl }}/assets/images/many-to-many.png" alt="many-to-many example" width="800px">

#### Defining Inverse of Many-to-Many
You make another call to `belongsToMany` on your related model to define the inverse of a `many-to-many` relationship.
To continue our user roles example, let's define the `users` method on the Role model:

<img src="{{ site.baseurl }}/assets/images/many-to-many-inverse.png" alt="many-to-many inverse example" width="800px">

### 4. Has Many Through
Accessing distant relations through an intermediary relation is made simple by the "has-many-through" relationship. 
As an illustration, a `Country` model may have numerous `Post` models through a middle `User` model. 
In this case, it would be simple to gather every blog post for a particular country. 
Consider the tables below to define this relationship:

```
countries
    id - integer
    name - string
 
users
    id - integer
    country_id - integer
    name - string
 
posts
    id - integer
    user_id - integer
    title - string
```
Although `posts` does not contain a `country_id` column, the `hasManyThrough` relation provides access to a country's posts through `$country->posts`. 
To perform this query, Eloquent inspects the `country_id` on the intermediate `users` table. 
After finding the matching `user IDs`, they are used to query the `posts` table.

To define this relationship, use the `hasManyThrough` method which takes two arguments: 1. name of the final model you wish to access, 2. name of the intermediate model.

<img src="{{ site.baseurl }}/assets/images/many-to-many-has-many-through.png" alt="hasMany Through example" width="800px">

<br>

## Conclusion
Eloquent is an ORM, which means it can take care of your models' relationships for you automatically. 
Using this tool, you can retrieve related models without writing complex queries.
And it also makes managing and working with relationships simple and easy. 