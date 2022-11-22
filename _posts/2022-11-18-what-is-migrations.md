---
layout: post
title: "What is Migrations"
authors:
- nsagnoy
categories:
- internship
- migrations
- seeding
image: assets/images/database_migrations.png
---

Laravel is an open-source PHP framework built to develop web applications that aim to make the development process easier for developers. It takes care of common services in a project such as routing, authentication, sessions, and database. There are tons of perks to utilizing Laravel. However, in this article, we will focus on a particular feature that is tremendously useful in dealing with the database called **Migrations**.

## What is Migrations?
Migrations, as the word implies, have something to do with movement from one place to another. In this case, it is about moving from a previous state of the database schema to a new one and vice versa. This means that it tracks and manages changes in the schema. Due to this, migrations is often associated with version control systems. Think of migrations as version control but for databases.

Migrations is an essential feature in Laravel. With it, developers can create-modify-drop a table, and/or add-modify-delete column in a database.


## Why you need to use Migrations?
Within the development phase of your application, your database schema may change numerous times. Creating and modifying tables and columns by working with SQL files or database manager (like phpmyadmin) can be tedious and sometimes might cause accidents. For example, using PHPMyAdmin would require you to manually create tables and modify fields on both your local and remote server, increasing the likelihood that you would forget something and destroy your application. However, with migrations, this problem can be prevented since Laravel automatically does it for you. And lastly, migration allows you and your team to define and share the application’s schema with each other. This is because migration files are stored along with the application’s code. Especially if you are using git, your team will only need to fork or clone the repo and then migrate to set up their database.



## Get started with Migrations
**Generate a Migration File**

Migration is a file that defines a table in a schema. It is by default found under `database\migrations` directory.
To create a migration file you simply do the command:

```
php artisan make:migration <name>
```

**Note:** Always give descriptive names to your files. For this example, we want to create a flights table thus the migration file is named 'create_flights_table'.

<img src="{{ site.baseurl }}/assets/images/create_migration.png" alt="new migration file" width="800px">

In our newly created migration file, we observe that it has generated a class with two methods: `up` and `down`. The `up` method is used to define and add new tables, fields/columns or indexes in the database, while `down` method reverses operations executed in the `up` method.

**Run and Rollback Migration**

To run a migration we need to use the command:

```
php artisan migrate
```

This command publishes all our schema to the database. This command also creates the table in the database.

For rolling back latest migration we have command:

```
php artisan migrate:rollback
```

This command reverses the last migration batch.

To rollback and migrate with a single command:

```
php artisan migrate:refresh
```

This will roll back all your migrations and then migrate

For dropping all tables in the database and then execute migrate use this command:

```
php artisan migrate:fresh
```

## Tables
### Create Table

Use the `create` method to create a new database table.
The create function takes two arguments: the name of the table as the first parameter, while the second is a closure which receives a Blueprint object that may be used to define the new table:
<img src="{{ site.baseurl }}/assets/images/change_table_name.png" alt="change table name" width="800px">


### Check if Table and/or column exists

The `hasTable` and `hasColumn` methods can be used to determine whether a table or column is present.

<img src="{{ site.baseurl }}/assets/images/check_if_table_or_column_exist.png" alt="check if table and/or column exists" width="800px">


### Update Table

To add/update a column in an existing table we need to generate a similar migration file to what we have created while creating the migration. The only change would be the migration name which should be descriptive. Like for example:

```
php artisan make:migration update_name_column_in_contacts_table
```

For adding a new column/field, we need to use the `table` method which also possess the same two arguments as `create` method. This also applies when modifying a table.

<img src="{{ site.baseurl }}/assets/images/add_update_table_migration.png" alt="add or update a table migration" width="800px">

Here are common column types:
<table>
  <thead>
    <tr>
      <th>Column Types</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>bigIncrements()</td>
      <td>creates a primary key with auto-increments of unsigned BIGINT</td>
    </tr>
    <tr>
      <td>id()</td>
      <td>is an alias for bigIncrements() method</td>
    </tr>
    <tr>
      <td>boolean()</td>
      <td>creates a BOOLEAN column</td>
    </tr>
    <tr>
      <td>string()</td>
      <td>creates a VARCHAR equivalent column</td>
    </tr>
    <tr>
      <td>timestamp()s</td>
      <td>creates a TIMESTAMP equivalent column</td>
    </tr>
    <tr>
      <td>rememberToken()</td>
      <td>creates a nullable, VARCHAR(100) equivalent column that is intended to store the current "remember me" authentication token</td>
    </tr>
    <tr>
      <td>integer()</td>
      <td>creates an INTEGER equivalent column</td>
    </tr>
    <tr>
      <td>enum()</td>
      <td>creates a ENUM equivalent column with the given valid values</td>
    </tr>
    <tr>
      <td>float()</td>
      <td>creates a FLOAT equivalent column</td>
    </tr>
    <tr>
      <td>foreignId()</td>
      <td>creates an UNSIGNED BIGINT equivalent column</td>
    </tr>
  </tbody>
</table>

To check other available column types in Laravel: [Column Types in Laravel](https://laravel.com/docs/9.x/migrations#available-column-types)


### Renaming / Dropping of Table

To rename an existing database table, use the `rename` method which takes two arguments: `from` and `to`.

<img src="{{ site.baseurl }}/assets/images/renaming_table_migration.png" alt="renaming table migration" width="800px">

To drop an existing table, you may use the `drop` or `dropIfExists` methods which takes an argument of `table_name`.

<img src="{{ site.baseurl }}/assets/images/drop_table_migration.png" alt="dropping table migration" width="800px">


## Columns
### Column Modifiers

Column Modifiers are a predefined function found in LARAVEL Migration that allows you to do things like set a column's default value, make any column nullable, and more.

<img src="{{ site.baseurl }}/assets/images/column_modifier.png" alt="column modifier migration" width="800px">



To check for other available modifiers in Laravel: [Column Modifiers in Laravel](https://laravel.com/docs/9.x/migrations#column-modifiers)


### Modifying Column

The doctrine/dbal package has to be installed using the Composer package manager before you may change a column.
It is used to determine the current state of the column and to make the SQL queries necessary to make the requested changes to a column:

    composer require doctrine/dbal

If you want to also modify columns created using the `timestamp` method, you must add the following configuration to your application's `config/database.php`

    'dbal' => [
      'types' => [
        'timestamp' => TimestampType::class,
      ],
    ],


### Updating Column Attributes

You may alter the type and properties of preexisting columns using the `change` method.
For instance, you want to increase the size of a string column.
Let's make the string size of name column to 50 to demonstrate how the `change` method works.
To do this, we just declare the column's new state and then invoke the change method:

<img src="{{ site.baseurl }}/assets/images/change_column_attribute.png" alt="change column attribute migration" width="800px">


### Renaming a Column

In renaming a column you simply need to use the `renameColumn` method which takes two arguments `from` and `to`;

<img src="{{ site.baseurl }}/assets/images/rename_column_migration.png" alt="rename column migration" width="800px">


**Dropping a Column**

To drop a column,use the `dropColumn` method which takes an argument of the column name. If you want to drop multiple columns at once then you must enclose them with square brackets (an array).

<img src="{{ site.baseurl }}/assets/images/drop_multiple_columns_migration.png" alt="drop column migration" width="800px">


## Indexes
### Adding Indexes

To add an index `unique` into the column `email`, we need to chain the `unique` method onto the column's definition. Alternatively, if you want to create index after defining the column you can simply call the `unique` method on the schema builder blueprint. 


<img src="{{ site.baseurl }}/assets/images/create_index_migration.png" alt="create index migration" width="800px">

Laravel will automatically generate the index's name. However, you may pass a second argument to customize index name.

<img src="{{ site.baseurl }}/assets/images/add_index_custom_name.png" alt="custom index name" width="800px">

Laravel supports various types of indexes. Check this link for further info: [Available indexes in Laravel](https://laravel.com/docs/9.x/migrations#available-index-types)


### Renaming Indexes

To rename an index, use `renameIndex` method. It takes two arguments: `from` and `to`.

<img src="{{ site.baseurl }}/assets/images/rename_index_migration.png" alt="rename index migration" width="800px">


### Dropping Indexes

For dropping an index you can use `dropIndex` method. For example:

<img src="{{ site.baseurl }}/assets/images/drop_index_migration.png" alt="drop index migration" width="800px">


## Foreign Keys
**Foreign Key Constraints**

Foreign key constraints, which are used to impose referential integrity at the database level, are also supported by Laravel. 
To create a foreign key column, use the `foreign` method which takes a string for its column name chained with `references` with the column name of the referenced table. And lastly, chained by `on` method which takes the referenced table name.

<img src="{{ site.baseurl }}/assets/images/create_foreign_key_migration.png" alt="create foreign key migration" width="800px">

Another way is to use the `foreignId` which takes on the same name of the column referenced from the other table and then chained by the `constrained` method which automatically determine the table and column being referenced. Or you can also pass the referenced table name.

<img src="{{ site.baseurl }}/assets/images/foreign_key_way_2.png" alt="create foreign key alternative" width="800px" >

You may also chain various actions for the `on delete` and `on update` properties of the constraint.

<img src="{{ site.baseurl }}/assets/images/actions_ondelete_and_onupdate.png" alt="actios for on delete and on update constraint property" width="800px">

Here are alternatives for these actions: 
<table>
  <thead> 
    <tr>
      <th>Methods</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>cascadeOnUpdate()</td>
      <td>Updates should cascade</td>
    </tr>
    <tr>
      <td>restrictOnUpdate()</td>
      <td>Updates should be restricted</td>
    </tr>
    <tr>
      <td>cascadeOnDelete()</td>
      <td>Deletes should cascade</td>
    </tr>
    <tr>
      <td>restrictOnDelete()</td>
      <td>Deletes should be restricted</td>
    </tr>
    <tr>
      <td>nullOnDelete()</td>
      <td>Deletes should set the foreign key value to null</td>
    </tr>
  </tbody>
</table>

Note: Column modifiers must be called before `constrained` method.


### Dropping Foreign Key

To drop foreign key, use `dropForeign` method and pass the name of the foreign key constraint to be deleted
or pass an array containing the column name of the foreign key.

<img src="{{ site.baseurl }}/assets/images/drop_foreign_key.png" alt="drop foreign key" width="800px">

### Toggle Foreign Key

To enable and disable foreign key follow methods:

<img src="{{ site.baseurl }}/assets/images/enable_or_disable_foreign:_key.png" alt="enable or disable foreign key constraints" width="800px">


## Difference between Migrations and Seeding

Seeding is a utility provided by Laravel to automatically add dummy data to the database. Using the database seeder, developers may easily add test data to their database table. It is quite helpful since it enables developers to find faults and improve efficiency by testing with different data kinds. 
On the other hand, as mentioned earlier, using migration you can build a table in your database. The database schema for the application can be changed and shared easily within your team.
