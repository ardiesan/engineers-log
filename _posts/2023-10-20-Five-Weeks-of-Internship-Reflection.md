---
layout: post
title: "Five Weeks of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/fiveweekinternship.jpeg
---

In my 5-week internship journey, I started by learning Middleware, WebSockets, and tackled deployment challenges. It involved debugging, teamwork, and researching monthly report plugins. It was about automation and GitHub Actions. I explored connectivity with Reverse SSH and "Poor Man's VPN" while also experiencing GitHub Workflows. My journey was a rich mix of learning, deploying, collaborating, automating, and exploring new technologies.

---
## Learning About Middleware, Websockets, and Framework Upgrades

On the first day of the week, I continued my learning journey with middleware and got introduced to WebSockets, something new for me. Our mentor shared some really useful insights about project frameworks. They explained that in the software world, it's not always necessary to upgrade or update a project's framework. If it's still working well and meeting the project's needs, there might not be an immediate reason to make changes. It's essential to think about the time and resources required for these updates. Our mentor also treated us to coffee, we used this time to summarize our weekly reflections. It was a nice experience, even though I had to leave early for a class. This day taught me that in software development, it's not just about technical skills but also about making thoughtful decisions regarding project upgrades.

## Applying Middleware Learnings and Deployment Challenges

This day was quite interesting. We were given a task to put our Middleware knowledge to the test by applying it to our basic apps and then deploying them to a server. I was able to use Middleware effectively. I implemented a Google sign-in feature in my basic note-taking app. Additionally, I added a Middleware function that checks if a user is signed in. If they aren't, they won't be allowed to access the homepage. However, I did face a minor issue while configuring the redirect URL after a successful login. Thankfully, I quickly figured out how to fix it. When it came to deploying the app on the server, things got a bit tricky. I successfully copied my project files to the server, but I accidentally placed them in the wrong directory. So, they weren't where they should be. Another challenge I encountered was not being able to run a database migration locally to the remote database, despite having the correct database information in the environment variables. I suspected that my Macbook might not have the proper permissions to perform database actions. So, I decided that once I successfully deploy the app on the server, I'll run the migration there. This day taught me that applying what we learn in real projects can be both rewarding and challenging. It's all part of the learning process in software development.

## Deployment Challenges and PHP Version Mismatch

On this day, my focus was solely on deploying my application on the server. However, I ran into a task blocker while trying to execute some PHP commands on the server. The error message was pretty straightforward: "Your Composer dependencies require a PHP version >= 8.1.0, but you are running 7.4.30." This error clarified the issue - my project required PHP version 8.1, while the server was running PHP version 7.4.30. It was a classic version mismatch. After some investigation, I discovered that the server had multiple PHP versions available. So, I made the necessary adjustments to ensure my project used the PHP version it needed. With that sorted out, I was able to successfully migrate my tables to the remote database. This experience reminded me that deployment can be a tricky process, and sometimes has unexpected challenges.

## Deploying Laravel App

Today, I focused on learning how to deploy Laravel apps on a server. We, the interns ran into a small issue, we couldn't access our projects through our domain directly. We had to specify the public folder in the URL. This happened because the public folder contains the vital index.php file, which is the starting point for our Laravel app. Our mentor shared an article that helped us solve this problem. By following the article's instructions, we fixed the issue, ensuring smooth access to our deployed Laravel app. This day taught me that understanding project structure and deployment is crucial for effective web application deployment.

---
## Deploying and Debugging

Today, I took another shot at deploying my application on the server using SCP (Secure Copy Protocol). I realized that compressing my project files made the transfer process to the server smooth and efficient. In addition to deployment, I encountered an error in my Laravel application, the "invalid redirect_url" error in Google Sign-In. However, I quickly diagnosed the issue, it was a simple misconfiguration in the .env file. This experience signifies the importance of reading documentation thoroughly and paying attention to the smallest details. This day was a reminder that deployment and debugging skills, combined with attention to detail, are essential assets for any software developer.

## Teamwork in Software Development

Today, our task was to achieve something new, connecting our VSCode to the server via SSH for remote development. It was a bit of a surprise, and we, the interns, tackled it together. However, we ran into issues getting connected at first.

Thankfully, one of my fellow interns found a simple solution hidden within VSCode's settings. With his help, I managed to establish a connection to the server. This experience highlighted the significance of teamwork in software development, together, we were able to overcome the challenge.

In our daily stand-up meeting, our mentor also gave us an important lesson. He emphasized the necessity of posting our daily stand-up reports in our Slack channel, even though we'd already discussed them in our virtual meeting. This serves as documentation, ensuring that we can revisit and review the information as needed. It's a practice that emphasizes the value of preserving information for future reference.

## Researching Laravel Plugins for Generating Monthly Reports

Today, my task was to search for Laravel plugins that could help in generating monthly reports for our ticketing system. These reports would summarize tasks and tickets created, completed, unfinished, and carried over from the previous month. I found three valuable plugins: Laravel Excel, Laravel PDF, and Laravel Charts for Visualization. These plugins are tools we can add to your software to make it do specific tasks more easily. In this case, they'd help create and display the monthly reports, making our ticketing system even more powerful. Today's task also reminded me of the importance of researching, it's a key skill in software development.

## Regular Expressions

Today, our mentor introduced us to something new called Regular Expressions, or simply regex. At first glance, regex looks like a jumble of letters, numbers, and symbols that doesn't make much sense. But our mentor broke it down and started with the basics. He gave us a cool challenge, using regex to validate an email. It was like solving a puzzle, even though regex seemed tough and intimidating at first, I found it oddly satisfying. It was like learning a secret language that can do incredible things.
I got so hooked on regex that I practiced it after our exercise. I believe mastering regex will be a valuable skill in my software development journey. It's like having a superpower to handle and manipulate text effectively.

---
## Choosing the Right Format for Monthly Reports: PDF vs. Excel

This day, I had a task - recommending a Laravel plugin for generating monthly reports in our admin ticketing system. Our mentor joined us, and we discussed the options. At first, I suggested using Laravel Excel because I thought Excel files were common for monthly reports. However, our mentor explained the downsides of using Excel. You see, Excel files are easy to change, which isn't good for report security. On the other hand, PDFs are like digital paper. Once you create one, it's tough for others to change it. This means our report stays just as we made it. With Excel, anyone could change the numbers or data without us knowing. But PDFs have another advantage. They look the same on different devices and systems. So, no matter who views our report, it'll always have the same layout and look. Excel files can sometimes look different on various computers, which can be a problem. In summary, PDFs are like secure snapshots of our report, while Excel gives more flexibility but also opens the door to unwanted changes. During our stand-up, our mentor reminded us to always double-check tickets. An isolated ticket might still be related to others, so cooperation with other teams is essential.

## Exploring Moment.js and Cron Jobs

This day, our task was to check out Moment.js, which is a popular tool for working with dates and times in JavaScript. It helps parse, validate, manipulate, and display dates and times. Additionally, our mentor gave me an extra task. I needed to catch up on cron jobs, something my fellow interns had already looked into. My goal was to figure out how cron jobs could be useful. So, I explored cron jobs, and I practiced using them on our remote server. I did a task that my fellow interns had done the week before that is to create a bash script to dump a MySQL database and save it in .tgz format. The catch was that it needed to be scheduled to run weekly and monthly using cron jobs. I hadn't worked with bash scripting before, so I did some research. Turns out, it's pretty handy because it can automate tasks, making them easier. Moreover, I learned that cron jobs have loads of other uses. We can use them to generate monthly reports, send those reports out, schedule automatic updates, run security scans, back up databases, and much more. After diving into cron jobs, I went on to read up on Moment.js.

## Learning Laravel Events and Automating Backups

Today, I focused on understanding Laravel Events and how they work in our admin ticketing system. These events help us organize and simplify our code, making it more manageable, testable, and readable. After studying Laravel events, I tackled another task. I created a bash script to back up my app directory in a tgz format. I set up a weekly cron job to do this every Saturday. I also wrote a local bash script to download the application and database backups. This task wasn't easy, and I encountered several challenges. But I persisted, learned, and eventually succeeded. It was a fulfilling experience.
One key takeaway was realizing that we can automate backups in the server, making it easy to store them in a safe location for future recovery.

---
## Exploring use cases for cron jobs and fixing my rsync script 
    
This day, I explored different applications of cron jobs. I was surprised to learn that these scheduled tasks could be used for far more than just backups. The world of cron jobs showed me opportunities for a wide array of tasks, like automated updates and report generation. This new knowledge broadened my knowledge of the use of cron jobs.

After exploring the different applications of cron jobs, I faced a challenge with my rsync script. This script is responsible for synchronizing backup files between the server and my local machine, handling both my application and database backups. The issue was puzzling, my rsync script executes when triggered manually, but it failed to execute within a cron job. I realized that I needed to include my SSH identity key or private key in the rsync command, a detail my mentor taught me. However, my mentor still spotted issues in my rsync script, and let me figure the remaining issues out. This situation made me aware of the importance of self-reliance and problem-solving. In the world of software development, one should not depend on others but actively engage in the process of understanding and resolving issues. With this, I successfully addressed the issue, and my rsync script now is functioning well.

## Exploring GitHub Actions and Workflows

Today, I continued my learning on GitHub actions, workflows, and CI/CD. These topics might be a bit unfamiliar, but I'm genuinely excited to learn about them. I believe that knowing these areas is crucial for any software developer. During this day, I had the opportunity to explore the existing workflows in the admin ticketing system. Our mentor told us to find the specific branch in the GitHub repository containing the workflow.

It wasn't the easiest task to locate this branch, but I eventually discovered it by navigating to the Actions tab within the GitHub repository. There, I found the branch that held the workflow file. I noticed numerous workflow runs within the admin ticketing system, such as the process of copying the repository to the GCP-VM. It struck me that GitHub actions and workflows might have a learning curve, but I'm determined to learn these features. I look forward to learning more about GitHub actions and workflows, and I'm eager to apply this new knowledge in my work.

## Applying GitHub Actions and Workflows

Today was a day filled with excitement as I tried out what I've been learning about GitHub Actions and workflows. These things can be pretty complex, but I was determined to use them in my project. GitHub Actions aren't exactly a walk in the park, they're a bit trickier than they seem.

My goal was to set up something called continuous deployment for my app. That means whenever I or someone else pushes or combines changes in the 'prod' branch, those changes would go to the server all by themselves automatically. Here's the catch, I hit a roadblock. My workflow was fetching the changes just fine, but it wasn't merging them. I still had to manually merge the changes on the server. So, I decided to keep working on this problem the next day. Even though things didn't go perfectly, I'm not giving up. This journey is all about learning, experimenting, and solving problems. It's a bit like a rollercoaster, full of ups and downs, but in the end, it's pretty exciting.

## Exploring Reverse SSH and Poor Man's VPN

Today, my task was to study and explore two intriguing topics: Reverse SSH and Poor Man's VPN. Our manager introduced these concepts, which were entirely new to me. Starting with Reverse SSH, in simple terms, is like turning the usual way you connect to a computer or a server. Instead of a computer connecting to a server, it's the server initiating a connection to a computer. It's handy when the computer you want to reach is behind a firewall or not easily accessible from the internet. Reverse SSH creates a secure tunnel for the server to get into the computer, like a secret passage, allowing you to control or access the computer even if it's not directly reachable.

Following this, I read about the "Poor Man's VPN." It turns out this is a clever method of using SSH as a straightforward VPN without the need for expensive equipment or software. Essentially, it provides basic VPN features using free and available tools like SSH without any additional costs. This newfound knowledge was quite exciting, as it offered a cheap way to gain VPN-like capabilities using tools that are accessible like SSH.

---
## Sharing My Local Admin Ticketing System via Ngrok

On the first day of my fourteenth week of internship, my main task was to practice GitHub workflows. However, my manager gave us an interesting job. We had to install Ngrok and use it to share our local ticketing system with our fellow interns. This task sounded pretty simple, so I gave it a try.

I began by executing the command `ngrok http 8000`, which was the port where my local admin ticketing system resided. The process proceeded smoothly, however, a twist emerged. The ticketing system had a Google login feature utilizing OAuth, initially configured by the previous intern. This meant I needed to set up my own OAuth credentials, including my `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` for my local version of the ticketing system.

Another thing to note was that the URL provided by Ngrok was temporary. So, I had to keep changing the app URL in my environment variables and the redirect URL in my Google Console. It was a bit tricky, but I managed to get everything working. In the end, I successfully shared my ticketing system with my fellow interns. They could access it, and they even used Google login, just like I wanted.

## Testing "Poor Man's VPN"

Today's tasks were quite straightforward. I focused on exploring something called "Poor Man's VPN" using SSH. This involves creating an SSH tunnel to connect to a server, in this case, the Ronins server. This was an interesting experience as I had never worked with SSH tunnels before.

To set up the tunnel, I configured my laptop's network settings by enabling a Socks proxy. This essentially acts as a gateway for my connection. After everything was set up, I verified the connection by visiting a website, [whatismyipaddress.com](http://whatismyipaddress.com/). To my surprise, it showed a different internet service provider and country, New Dream Network and the United States, respectively. This indicated that my connection was going through a different route. It was a pretty cool test, and it demonstrated the effectiveness of "Poor Man's VPN".

Additionally, I provided my manager with an update on my progress with GitHub Actions and Workflows. It's important to keep everyone informed of our progress on a task. 

## GitHub Workflows: A Success Story

Today, I got back into GitHub Actions and Workflows with determination. I was keen on resolving an issue that had been bothering me, my workflow does not deploy code changes on the server as correctly.

To find a solution, I did some research. As it turns out, I could use a simple `git pull` command to pull changes to my repository using a GitHub token. To keep this sensitive token safe, I stored it in my repository's secrets. With the token secured, I integrated this script into my workflow, and to my surprise, it worked fine. Seeing my workflow working correctly was highly satisfying, and I couldn't help but feel a sense of accomplishment.

This experience made me more determined to explore GitHub Action and Workflows. I believe there's a lot more to uncover and I'm excited to learn more.

## Codium AI with VSCode and Github Workflows

Today was all about improving my workflow with a new addition, continuous integration. This time, the workflow executes when there's a pull request on the prod branch. It's like an extra layer of quality checks before the code gets merged.

I also explored Codium AI, a tool that works with Visual Studio and GitHub workflows. What it does is pretty cool, it analyzes your code and automatically generates meaningful tests to catch any bugs. These tests help ensure your software is reliable and correct. What's even better, Codium AI can handle all programming languages, which makes our lives easier. AI is really like a super smart assistant that can help us in many ways. But there's something important to remember, AI can't take the place of a real, human programmer. It's just like having a helpful tool but it can't do everything on its own. So, we should use AI to make our work easier and better. AI and humans can work together to do amazing things.

---


