---
layout: post
title: "Tales of the 5th Week Intern"
author: raya-ay
categories: 
- internship
- livewire
image: assets/images/anthony/5th-week.png
---

## Happy Monthsary!
Its officially been one month since my onboarding to this company. Looking back, it felt like a long time already. I knew that this is what I would eventually be at this point, as I used to imagine years ago, but to actually be at this point gives me a feeling of relief and joy that I am moving forward in my life, slowly, but surely.

--- 

## Monday (2023-09-11):
---

I started the day off with updating my pull requests and tickets in Jira. I was tasked to add more details to one of my tickets which was regarding an overlapping input. I was to add details on which browser I was using and which resolution my device was on, as well as, if the problem persists in other browsers. To my surprise, there was no issue when using other browsers.

There was also comments regard my fixes. Although it does solve the problem, it was by using that was not conventional which does not fit the standards and of the company. It was a singular inline style that I applied which does not fit the consistency of the structure of the project. What I was advice to do is, as much as possible, avoid in-line styling, and instead use the external app.css of the project. But that does not mean I can just insert a style anywhere. I understand that the .css file also follows its own structure and you have to order which selectors comes first. So I found the appropriate selector in the middle of the file and inserted my fix there.

This ticket branch  was one the first ones that I worked on and since then, I had a branches that were branching off from themselves, consequitively, starting with this branch. This brought me to my next task which was to synchronize my later branches from the changes I made in a previous branch. So the issue is that I have branch 160, which branches off to 161, which branches off to 162, which, as you guessed it, branches off to 163. So in order for branch 163 to be updated from the changes made in 160, I would have to update branch 162 before that. But before I can update branch 162, I have to update branch 161. So what I did was to call `git merge` in each branch and I were to merge the current branch and the branch it branched off from.

I feel like this was too excessive and that there could possibly be a better method in resolving such an issue, but I am sure I will be able to encounter that solution as I continue my journey as a programmer.

Near the end of our shift, we were tasked to explore livewire, in which I started with installing it to the project and followed the documentation on how to set it up and how to use it. However it ended with a website that was not working and I knew I could continue and success on my next work day.

## Wednesday (2023-09-13)
---
The day continues with exploring livewire. Instead of installing livewire and start working on it on an existing project, I decided to start on a blank canvas. I then followed the documentation again but this time the application was working. I continued my exploration on livewire by following a tutorial on youtube which held a collection of multiple projects, each exploring the cabalities and functions of livewire. Exploring livewire was a nostalgic experience. It reminded me of how I used to explore react and vue. Aside from that, it was also a refresher on laravel as a whole because, after a long while, I got to work on a laravel project as a whole and not just focusing on a single part of it. By that I mean I be making a component as well as configuring the `web.php` file for my routes and making my migrations.

The weather was particularly harsh ever since noon. It was to the point that my fellow interns and I had to buy food from this block and eat in the company pantry, which was a first. I ended the day waiting an hour after my shift for the heavy rain to subside while enjoying a hot beef noodle soup with egg in  a convenience store.

## Friday (2023-09-15)
---
The last day of the week, I assume the task would be similar to what I have done in the past two work days, which was to continue exploring livewire, which I was looking forward to because there was a project that I had in mind which I wanted to explore. I have also read in forums that livewire is not an adviceable framework for beginners as it does most of the heavy work and also has a lot of "magic" done behind the scenes, away from the eyes of the programmer. As a result, it may lead the programmer to be too dependent on it and would impede on their oppurtunity to grasp and understand some concepts on what goes on into making a website. So I wanted to explore that aspect as to the strengths and weaknesses of each framework.

However that task was put to a halt as we were given a new task, which was to explore and do research on the middleware component of a laravel project.

Upon checking out the middleware of the application, it was an set of a nostalgic experience as I have previously encountered this component and had the same thoughts as I have now: "*What is this and how does it work...*".

The last time I encountered this was in my project in my course called 'Information Management 2'. My groupmates and I made a Content Management System for a online exhibit, and I encountered the middleware when it came to user authentication and that is what middleware does. It inspects and filters the HTTP requests entering the application. But other middleware can be written to perform a variety of tasks besides authentication.
