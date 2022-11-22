---
layout: post
title: "Understanding Laravel migration and seeding for beginner's"
authors:
- jdayuday
categories:
- internship
- migrations
- seeding
---

Web application frameworks  according to GeeksforGeeks as "a software framework that is meant to assist the creation of web applications including web services, web resources, and web APIs." In layman's terms, web frameworks are pieces of software that allow you to design and execute web applications. As a result, you don't have to write on your own and hunt for any errors and miscalculations.

Web frameworks were established in the early days of web app development as a way to eliminate hand-coding of apps where only the creator of a specific app could update it. The advancement of web development now we have web-specific languages that allow developers to solve altering the structure of an app has been overcome by the emergence of general performance. In this article, we are going to focus on the Laravel web application framework.
## What is Laravel?
Laravel is a reliable and simple-to-use open-source PHP framework. It adheres to the model-view-controller pattern of design. Laravel makes use of pre-existing parts from other frameworks to build online applications. The resulting web application is more organized and practical.

Incorporating the fundamental components of PHP frameworks like CodeIgniter and Yii as well as other programming languages like Ruby on Rails, Laravel provides a wide range of functionalities. The extensive feature set of Laravel will accelerate web development.

<img src="{{ site.baseurl }}/assets/images/jdayuday_laravel_1.png" alt="static vs dynamic site" width="600px">



**Here are some disadvantages that the Laravel framework can offer for web-based applications:**
- The Laravel framework helps the web application become more scalable.
- Since Laravel reuses the components from other frameworks while constructing web applications, a significant amount of time is saved during the web application design phase.
- It has namespaces and interfaces, which aid with resource management and organization.

**Two fundamentals that you need to understand in getting started with the Laravel web application framework.** 

## Migration and Seeding
You can build a table in your database using Laravel Migration, which is a crucial functionality. The database schema for the application can be changed and shared. A new column can be added to the table, or an existing column can be removed.

## What is Laravel migration?
Within the development phase of your application, your database schema may change numerous times. Creating and modifying tables and columns by working with SQL files or database manager (like phpmyadmin) can be tedious and sometimes might cause accidents. For example, using PHPMyAdmin would require you to manually create tables and modify fields on both your local and remote server, increasing the likelihood that you would forget something and destroy your application.

However, with migrations, this problem can be prevented since Laravel automatically does it for you. And lastly, migration allows you and your team to define and share the application’s schema with each other. This is because migration files are stored along with the application’s code. Especially if you are using git, your team will only need to fork or clone the repo and then migrate to set up their database.

## Importance of Laravel migration
The main importance of migration in Laravel is that you will do it on your development server/station, and you will be able to change the schema many times in development, migrate, rollback migrations, and re-migrate them, and once your application is finished, you will not have to remember what you need to do in your production environment because Laravel will do it automatically for you.

The schema of the tables is preserved in migration files. You may never have to use phpMyAdmin again if you use migration (except for creating a DB). After that, simply execute the command 'PHP artisan migrate' to construct the tables from the PHP side. You will also never have to worry about the DB environment (MySql, Postgres, SQL Lite, etc.) because the migration is not dependent on the environment in which the tables are being migrated.


## Performing a migration in Laravel
Assuming that you already created and can connect your database (any) Mysql in my case from your Laravel project. Now let's perform a Laravel migration.

In your preferred CLI first, run the `PHP artisan list`, CLI will display all the possible lists of commands that you can use in your project.
```
php artisan list
```

**To create a migration, you may use this inside your CLI migrate:make:**
```
php artisan migrate:make create_users_table
```
<br>


After you the command you will be able to see your project file under in `app/database/migrations folder/directory`.

If you want to specify a specific path for your migration you can use this command instead:
```
php artisan migrate:make foo --[path]=app/migrations
```

This is a reminder this is not the only way to do migrations in the Laravel project, but for now, we are going to focus on the basic command.

**Now we can make a migration, let's run your migration**
Running all outstanding migrations in your Laravel project:
```
php artisan migrate
```

Running all outstanding migration for a path:
```
php artisan migrate --[path]=app/foo/migrations
```
<br>

**Additional information for Laravel migration power**
Basically migration rollback is reverse migration that brings back your previous database state.

<br>

Rollback your last migration just use this command: 
```
php artisan migrate:rollback
```

Rollback all the migrations:
```
php artisan migrate:reset
```

Rollback all migrations and run them all again:
```
php artisan migrate:refresh

php artisan migrate:refresh
```

<br>

**To know more about migration you can check the website for official Laravel migration website.** 

References: https://laravel.com/docs/4.2/migrations

## Laravel database seeding

**What is seeding?**

To make it simple Data seeding is the process of populating a database with an initial set of data. 

In Laravel December 24, 2020. Database seeding is the process of populating data tables with fictitious data. This procedure is used by developers for testing. Using seeder classes, Laravel allows you to fill data tables with test data. The database/seeds directory contains all seeder classes.

Laravel offers the ability to use seed classes to populate your database with data. The database/seeders directory contains all seed classes.

## Writing and generating Laravel seeder
To make a seeder use this command in your preferred CLI:
```
php artisan make:seeder UserSeeder
```

<br>

sample: 
<img src="{{ site.baseurl }}/assets/images/jdayuday_laravel_1.png" alt="static vs dynamic site" width="600px">


By default, a seeder class has exactly one method: run. When the db:seed Artisan command is issued, this method is invoked. You can insert data into your database however you want using the run method.

## Running your Laravel seeder
To seed your database you may use db:seed by default this command will run the `Database\Seeders\DatabaseSeeder`:
```
php artisan db:seed
```

**Additional to Laravel seeder**
You can use `migrate:fresh` to see your database with `--see` the option. This command will drop all tables and re-run all of your migrations. This command is useful for completely re-building your database:
```
php artisan migrate:fresh --seed
```

<br>

**For additional information regarding Laravel writing seeders, you can check the official Laravel website**

References: https://laravel.com/docs/9.x/seeding#running-seeders 

To sum it up, the difference between **migrating and seeding** (Laravel), you can think of migration as somewhat version control for your database in which it will allow you to modify your database schema and keep it updated. During migration, it is typically paired with a schema builder which handles and manages your application schema. On the other hand, seeding is another way of storing data inside your database including its test data for seed classes (Laravel).

<br>

**To know more about Laravel PHP web framework you can their official website for more information.** 

References: https://laravel.com/docs/9.x

