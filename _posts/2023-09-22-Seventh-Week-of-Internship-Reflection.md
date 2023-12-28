---
layout: post
title: "Reflecting on the Seventh Week of My Internship"
author: jwapano
categories: 
- internship
image: assets/images/wapano-seventh-week.jpg
---
This week, we focused on the initial deployment of our newly created Laravel project with middleware implementation. Here's how it went.

## Seventh Week Reflection:

### Day 1: Middleware Exploration and Reflective Summary
 
Reflecting on our week, our task from the previous week was to delve deeper into middleware. Today, we carried on with this learning journey by examining how middleware is utilized in the fst-admin-ticket-system application. Our objective remained straightforward: comprehending the inner workings of this middleware and the logic behind its code.

Additionally, our instructor introduced us to Syncthing, a tool that facilitates remote syncing between smartphones and laptops. We successfully integrated Syncthing with our Obsidian note application, enabling real-time access to my notes on both my phone and laptop.

Later in the afternoon, our instructor assigned us another task: creating a summary of the reflections we have submitted over the past few weeks. This task encouraged us to revisit our experiences and share our insights with the team, reinforcing the idea that learning and teamwork are intertwined.

As we progress, our exploration of middleware continues, and we eagerly anticipate the discoveries and collective learning that lie ahead.

### Day 2: Deploying a Laravel Project with Middleware

Today, access to Ronin's database server was granted we were able to log in, and our current objective is to deploy a Laravel project with middleware on the remote server. However, personally, I didn't have any existing Laravel projects to deploy. Consequently, I took the initiative to create my project and integrate middleware.

In the late afternoon, I completed the development of my application and was all set for deployment. Unfortunately, I encountered an error when attempting to migrate my tables to the remote database server. This error message indicated that my account lacked the necessary authorization access to perform the migration. With limited time remaining, I decided to postpone deployment to the next workday.

### Day 3: Transferring a Laravel Application with SCP

Today, I encountered the same migration error that persisted from the previous working day. I promptly informed my mentor about the issue and, while awaiting authorized permission to resolve it, I took the step to transfer my Laravel application to the remote Ronin's server using SCP.

The process involved two steps:

1. From my Mac to my phone:
   
   `scp -P 8022 ~/Desktop/my-laravel-project.zip u0_a327@192.168.1.193:~/storage/shared/jwapano-laravel-project`

2. From my phone to the remote server:
   
   `scp ~/storage/shared/zip-laravel-project/my-laravel-project.zip jwapano@san.ronins.site:~/jwapano.ronins.site/zip-laravel-project/`

This workaround allowed me to successfully transfer my Laravel application, ensuring that I could continue my work while waiting for the authorization to resolve the migration error.