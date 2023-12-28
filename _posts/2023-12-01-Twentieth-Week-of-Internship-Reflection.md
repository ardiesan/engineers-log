---
layout: post
title: "Twentieth Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/mtrinidad-week20.png
---
During my 20th week, I decided to challenge myself by moving my Jekyll project from GitHub Pages to our server. It seemed tricky at first, but exploring Jekyll's manual deployment using Rsync, a tool I knew from handling backup files, made things clearer. The puzzle was figuring out where to put my Jekyll project on the server, and after a bit of experimenting, I found a simple solution by tucking it inside the 'public' directory of my Laravel project. 

--- 
## Jekyll Deployment Challenges

On the first day of my 20th week of internship, I decided to take on my mentor's suggestion and deploy my Jekyll project on our server rather than just relying on GitHub Pages. Initially, I doubted its feasibility, but diving into Jekyll's documentation on manual deployment revealed the use of Rsync, a tool I was already familiar with from syncing backup files.

The hurdle came when figuring out where to place my Jekyll project's `_site` directory on the server. After a bit of trial and error, I opted to nest it inside my Laravel project's `public` directory, considering it housed the Laravel app's entry point. Creating a directory within 'public' with the same name as my Jekyll project's base URL surprisingly did the trick. It was simple but satisfying, reminding me that sometimes, the solution is just a directory away. 

---
## Streamlining with Automation

For this week, I took steps to enhance efficiency. I applied version tagging to both my Laravel app and Jekyll project, a small but crucial step for keeping track of changes. To further streamline the release process, I set up a workflow file leveraging GitHub Actions. This not only automated releases but also brought the added benefit of reducing manual effort and potential errors.

Additionally, I modified the deployment workflow to execute only when there were new releases. Embracing automation not only saves time but also ensures a more controlled and error-resistant deployment process. This experience reinforced the importance of leveraging tools like GitHub Actions for simplifying and enhancing our development workflows.

---
## To wrap things up
This week, I made things smoother. I started using version tags for both my Laravel app and Jekyll project, a small but handy way to track changes better. Then, I set up a cool thing called GitHub Actions to automate releases, making my life easier and reducing the chance of mistakes. I also made sure that the deployment only happened when there were new releases. This whole experience taught me that using tools like GitHub Actions can make our work simpler and less error-prone.