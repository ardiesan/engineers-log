---
layout: post
title: "Tales of the 17th Week Intern"
author: raya-ay
categories: 
- internship
# image: assets/images/anthony/16th-week.png
---

My project is finally up a running using GitHub pages, but seeing how others brought their project to their site has left me unfullfilled with how I implemented mine, so this week was spent on deploying the project into our personal site in ronins.site, which would slightly require more configuration than using the GitHub pages method, which is automated by GitHub.

---

# Monday (2023-12-04)
---

The other interns decided to have their personal blogs be run in the ronins and I decided to follow suit. It was quite the task because although I was able to connect to the remote server using SSH via VSCode in the past, it did not do the same when I attempted it again. I really don't know the solution because I've tried all the options and then tried it again but then suddenly it worked. I was not able to tell which solution helped solve the problem. So what I did instead was to use my trusty good old reliable Command Line Interface.

To prepare for continuous deployment I prepared an action workflow, which would deploy whatever was pushed from the main branch to the remote server. In order to do that, I would have to set up my variables such as where my remote server is, what I would like to transfer, its SSH private key, and others. It is good practice to keep such confidential values hidden, so I configured repository secrets for the project, provided by GitHub. These secrets are for my 1.) local directory, 2.) deployment directory, 3.) SSH private key, 4.) username, 5.) server/host.

# Wednesday (2023-12-06)
---

Previously, I was successfully able to deploy my blog from my GitHub repository to the remote server using SFTP, the other interns used rsync, but I wanted to try a different method. 

After successfully implementing sftp with the secrets variables I have configured I moved on to having my site having the blog open by default.

I recall back to when I made my first web application, which was about Pokemon, in order the remote server to open and use the index.php file by default, I had to configure my .htaccess file to have my public directory as the baseurl. All the necessary files for my blog site were found in the "\_sites" folder. What I planned to do is to change the code from

```
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteRule ^(.*)$ public/$1 [L]
</IfModule>
```

to
```
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteRule ^(.*)$ _site/$1 [L]
</IfModule>
```

After making my changes, I broke the website, then reverted it back to public and there is was functional again. I couldn't figure out what was the use but since I knew that me and my fellow interns will be seeing each other in the office on our next workday, Monday, I'll ask them on how they implemented their blog to the server.
