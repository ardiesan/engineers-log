---
layout: post
title: "Reflecting on the Eighth Week of My Internship"
author: jwapano
categories: 
- internship
image: assets/images/wapano-eighth-week.jpg
---
This week, we were finally able to deploy our Laravel application without any problems. I've also gained valuable new knowledge about Cron and Regex expressions.

## Eighth Week Reflection:

### Day 1: Successfully Deploying Laravel Application
On this day, I was finally able to deploy my Laravel application on the remote server, thanks to my mentor who guided us on how to do it properly. As a result, I was also able to migrate my tables to the remote database without any problems. Overall, this has been a valuable learning experience, especially since it's my first time deploying a web application that can be accessed remotely. I'm very thankful for the guidance and support.

Here's my laravel app `jwapano.ronins.site`.

### Day 2: SSH Connection and OAuth2 Google Sign-In Integration
Today, our objective was to establish an SSH connection between the remote server and VSCode for efficient file editing. By the end of the day, I successfully accomplished this task through some configurations, and I'm quite satisfied with the outcome. Additionally, I implemented an OAuth2 Google sign-in feature into my application.


### Day 3: Bash Scripting for MySQL Backups
In the morning, we were tasked with creating a Bash script to dump a MySQL database. The filename format for the dump is expected to follow the pattern "YYYY-MM-DD-HHIISS.tgz." This Bash script will be scheduled to run weekly and monthly at midnight using Cron. I successfully completed this task on a remote server.

Cron is a time-based job scheduler in Unix-like operating systems, enabling users to automate the execution of tasks or commands at specified intervals or times. Users can create "cron jobs" by defining a schedule using a special syntax in a crontab (cron table) file. The schedule can be configured to run tasks at minutely, hourly, daily, weekly, or monthly intervals, or even on specific dates and times. Cron is widely used for automating routine system maintenance, backups, and other repetitive tasks on Unix-based systems.

In the afternoon, our mentor introduced us to regular expressions (regex), and we were presented with a challenge to create a regex expression for validating email addresses. This experience was both enjoyable and challenging, as it was my first time working with regex. I gained valuable insights and knowledge today.

Here's the regex expression we've come up with: `^([a-zA-Z0-9-_.]*)@([a-z\-]*)((.[a-z]{2,3}){1,2})$`. It may not be perfect, but it should work for many common email address formats.