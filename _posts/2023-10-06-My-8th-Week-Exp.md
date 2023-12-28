---
layout: post
title: "Tales of the 8th Week Intern"
author: raya-ay
categories: 
- internship
image: assets/images/anthony/8th-week.png
---

Cron Jobs! They are a way of scheduling tasks to run on your server. Cron is a service running in the background that will execute commands (jobs) at a specified time, or a regular interval. This week was loaded with Cron job-related tasks and I am glad I got introduced to this method.

---

## Monday (2023-10-02)
---

Previously, my task was to make a cron job run at a certain time however the issue is that it won't perform the command at all when the time passes. The next day, throughout the weekend, I got notifications at 6 a.m. saying that the file/directory did not exist even tho I scheduled the task to be run at 10 a.m. This gave me the speculation that the command worked and is just that the output takes a long process. 

When I arrived at the office, I was set on solving the issue. Thanks to the help of Jade, another fellow intern. The issue was so obvious, it left me dumbfounded. It turned out that the server that my cron job was operating on was in a different time zone, which is 15 hours behind ours. I tried to solve the situation by changing the local timezone of the server to be set to the timezone of Hong Kong, which is the same timezone that the Philippines follows. But unfortunately I wasn't able to make it work. So an alternate remedy I implemented was to just adjust the time manually, meaning that if I want my code to run at midnight here in the Philippines, I have to schedule the cron job to run the task at 9 a.m.

For the rest of the day, I dived deeper into what my task was last Friday which was Regular Expressions. It is a powerful tool to use and I believe not many people truly appreciate how much regex has helped them as they don't even realize, at the core of it, all of searching is utilizing regex to an extent. Regex has been streamlined to the point that anyone and everyone can use it by just typing the words they want to find, without all the expressions.


## Wednesday (2023-10-04)
---

I began the day by reconfiguring my cronjob so that the backup would have a prefix to identify whether the backup was a weekly or a monthly snapshot. My previous application of the code is that there would only be two cron commands that run the same script one of which would be weekly, while the other would be every end of the month. 

This is what the cron job used to look like:
```
0 0 * * 6 bash ~/dumpAutomation.sh 
0 0 30 * * bash ~/dumpAutomation.sh
```

The issue with this is that there would be no clear indication of which files would be the result of the weekly command or the monthly command. Sure you can just check the date in the name of the file and see if it's the end of the month. But what if if the end of the week would also be the end of the month, what would happen to the file? would the monthly backup overwrite the weekly backup? So my solution to this issue was instead of creating a separate script dedicated to the monthly schedule, how about I apply parameters/arguments? So after a quick search, I was able to implement bash arguments.

This is the cron job with the implementation of arguments
```
0 0 * * 6 ~/dumpAutomation.sh weekly 
0 0 30 * * ~/dumpAutomation.sh monthly
```

Within my bash script here is how the argument is utilized
```
timeTitle=$(date +%Y-%m-%d-%H%M%s)
//code for the creation of $timeTitle.sql is omitted for confidentiality
tar -czvf $1_$timeTitle.tgz $timeTitle.sql
```

In this script, the argument is stored in `$1` and that is how arguments are utilized. If more arguments are necessary, they are separated with a space and to access them, call them from the order in which they were arranged, starting from `$1` to `$n`.


## Friday (2023-10-06)
---

I started the day by starting from where I stopped on my previous workday. It would be an application of what I have already applied regarding my cronjob. I made a bash script that will make a backup of my web application and format it to a .tgz format. Afterward, I made a cronjob that would run that script weekly.

I spent the rest of my afternoon researching Laravel events and listeners lastly, I ended my week by making my Friday reflection.