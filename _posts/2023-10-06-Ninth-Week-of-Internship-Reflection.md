---
layout: post
title: "Reflecting on the Ninth Week of My Internship"
author: jwapano
categories: 
- internship
image: assets/images/wapano-ninth-week.jpg
---
This week, our main focus was on implementing a cron job that executes the script file for backups. It's truly a valuable opportunity to gain hands-on experience on an actual server, which not everyone gets to experience. I'm grateful, especially to my mentor.

## Ninth Week Reflection:

### Day 1: Task Scheduling Automation using Cron
During the last Friday's cron creation, which backs up my application's database, before I set it to a weekly and monthly schedule, I first conducted some tests and scheduled it for the next day at 8 AM, which is on Saturday. I received an email as expected, but it turns out that the execution time was different; it ran very late. So, today, I checked my cron configuration, and at first, there was nothing wrong with it. However, I didn't realize that the server runs on a different time zone, PDT, which is hours behind. So, I adjusted my cron and configured it for the correct schedule, and now it works as expected. Today, I've learned another valuable lesson: whenever setting up task scheduling automation, make sure to check the timezone first, or it may not turn out as expected.


### Day 2: Exploring Moment.js
Today's task of exploring Moment.js presents an excellent opportunity for us to deepen our understanding of date and time handling in JavaScript. This library can simplify complex date-related operations and improve the functionality of our applications. Our mentor also mentioned that servers run on different timezones, such as UTC:00, to easily identify times; otherwise, there will be complexity when it comes to calculating various timezones. For instance, Netflix is releasing a video on October 5th, and our October 5th is not the same as other timezones; some are ahead, and some are not. To ensure synchronization, this is where Moment.js comes in.

### Day 3: Web Application backup using Cron

Our mentor showed us how to create a .tgz file in a specific directory. So, for today's task, our job is to create a shell script file that backs up our web application and implements a cron job to schedule it weekly on Saturdays. As we work on this task, we have the opportunity to enhance our scripting skills, which can be valuable in various other scenarios. Moreover, it emphasizes the importance of proactive system maintenance and data security, fundamental aspects of web application management.