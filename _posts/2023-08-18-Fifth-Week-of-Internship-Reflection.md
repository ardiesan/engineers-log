---
layout: post
title: "Fifth Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/fifthweek.jpeg
---
This week I learned about shell commands, cybersecurity, and Git configurations. Me and my co-intern did code reading, which helped us understand projects better. 

---
## Day 1: JIRA for Efficient Project Management 

#### Understanding JIRA
JIRA is our go-to platform for handling tasks, often referred to as tickets. These tickets represent the different pieces of work that need to be completed within a project. They serve as a way to keep track of our progress and effectively manage the project's development.

#### Tickets and Endpoints
Tickets have specific endpoints, which are essentially like special web addresses. Each endpoint represents a particular task or action that the program knows how to perform. It's like opening a specific door to access a specific room. For instance, /api/v1/users is an endpoint. The term "users" is plural, indicating that it returns a list of users. On the other hand, /api/v1/user is singular, meaning it fetches information about a single user. Endpoints follow a convention. 

####  Estimating Project Work
In JIRA, we use story points to estimate the effort needed for a task. Story points help us estimate the complexity of a task and determine how much time it might take. If a ticket is assigned 8 points or, say, 3 days, it's important to break down why it requires that amount of effort by dividing it into subtasks.
You can also set points for each subtask. Subtasks and their points can provide a clearer picture.

#### Effective Communication
When working with tickets, clear communication is the key. If you encounter an issue or a problem, don't just highlight it; propose a solution as well. And remember, presenting a solution should be done with respect and care, your seniors and managers will listen and might consider your solution if you do this. If you're uncertain about how to approach a task, don't hesitate to do some research and learn from experts. Learning from experts can help us get better. Remember, we grow by learning from those who came before us – "Stand on the shoulders of giants".

---
## Day 2: Unexpected Obstacles and Learning Opportunities

My second day didn't go as planned. The goal was to check out and test our admin ticketing system project, but I encountered an unexpected challenge. To get started, I needed to clone the project's repository, which required installing GitHub CLI. However, this is where the problem came in. Despite my attempts, installing GitHub CLI through homebrew did not work as expected. Even other homebrew commands did not work. Feeling stuck, I reached out to my manager to explain the situation. It was frustrating because I couldn't proceed with the task due to these technical difficulties.

I decided to explore another path. Instead of installing GitHub CLI, I decided to check out the project directly through the GitHub website. While it wasn't the original plan, it was a workaround that allowed me to continue engaging with the project. My manager's suggestion to update my macOS was a step towards resolving the issue, so I initiated the update and patiently waited for it to complete. During this time, I turned to my phone to explore and learn about two topics: Laravel Sail and PSR-12.

One valuable lesson I've learned from this experience is the importance of being resourceful. When facing difficulties, it's crucial to think and use the tools and options that are available. While I couldn't access the project in the way I initially intended, I found a way to keep moving forward and make the most of the situation. This supports the idea that in the world of software development, adaptability and resourcefulness are key attributes we need to practice. I also learned to expect the unexpected. Despite planning, things might not always go as planned. Adaptability is key. When unexpected challenges happen, it's important to remember that flexibility is a nice trait to have. We can't always predict task blockers, but we can control how we respond to them. When we encounter a problem, we shouldn't hesitate to ask for guidance. It's alright to ask for help when we find ourselves in a tough spot. Seeking guidance from those with more experience can lead to effective solutions and valuable learning opportunities. We should always remember that we are not alone in our journey, and seeking assistance is a sign of strength, not weakness.

---
## Day 3: Shell Commands and Networking Basics

On my third day of internship, I got to know some stuff about shell commands and how computer networks work. Shell commands are like magic words you tell the computer to get things done, and one trick I learned is using the "tab" key to make it easier and quicker.

We talked about commands like "uname -a," which is like asking the computer about itself, and "docker exec -it <container-name> /bin/bash," which lets you get inside a docker container. There's also "arch" that tells you about the computer's architecture, and "cat /etc/os-release" that gives you information about the computer's operating system. When it comes to places on the computer, we learned about paths. "cd ~" is like saying "take me home,". There's also a way to see what ports are open on a computer using commands like "lsof" and "netstat."

#### Ports and Addresses in Networking
In networking, ports and addresses play a crucial role in communication. Here are some key points about them:

Ports:
- Port 80 is used for HTTP, which is the protocol for browsing websites.
- Port 443 is for HTTPS, a secure version of HTTP
- Port 22 is designated for SSH and SFTP 
- Port 53 is assigned to DNS 

Addresses:
- The IP address 0.0.0.0 acts as a listener for all ports
- The IP address 127.0.0.1 is often referred to as the home address, there's no place like 127.0.0.1
- The IP address 192.168.1.1 is the router address. Connecting to it doesn't mean you're directly connected to the internet; rather, it signifies your connection to a router within your local network.

#### Understanding User Roles in the Shell
When working within the shell, you can identify the type of user based on the prompt symbol:

- If you see a `$` symbol, it indicates you're a regular user. This means you need to use the `sudo` command to install software or perform privileged operations.
- On the other hand, if the prompt displays a `#` symbol, you're operating as the root user. Root users have the privilege to install software and perform tasks without needing `sudo`.
- It's important to note that installing software is a privilege and not all users should have this ability. This helps maintain system security.

However, the reliability of the prompt symbol isn't reliable. Sometimes the prompt may be customized which could lead to misinterpretation. Therefore, while the prompt symbol provides an initial indication, it's wise to rely on other contexts as well when determining user roles within the shell.

#### Cybersecurity
In cybersecurity, there are conventions and patterns to follow. Cybersecurity vulnerabilities often arise from incorrect implementations and not following the established patterns. Becoming proficient in cybersecurity takes time and dedication, much like becoming skilled in software development.

#### Learning in Software Development

In the world of software development, there's no one-size-fits-all device or operating system that is supreme. The choice of tools depends on the developer's willingness to learn and explore. As developers, we make the most of what we have, focusing on developing our skills rather than focusing on specific devices or systems.

Similar to how there's no "best" programming language. Each language has its strengths and is suited for different tasks. Popularity alone doesn't determine it's the best. Instead, a language's fit for a particular purpose matters most. Embracing these differences is essential to becoming a well-rounded developer. After all, true developers understand that there's no "best" programming language, device, and operating system in the world of software development.

---
## Day 4: Git Configuration and Code Reading

On this week's fourth day of internship, our mentor taught us some important concepts in Git. We discussed the usage of git config --global and git config --local, which are essential commands for configuring Git settings on different levels. This knowledge is important as it ensures consistency and accuracy when dealing with multiple projects.

Additionally, we learned about the significance of signing Git commits. By signing commits, we add a layer of security and authenticity to our work, ensuring that the changes we make are verified. This helps make our work safe and trusted.

Later in the day, we engaged in a session of code reading. We had the opportunity to read the code behind the admin ticketing system, which we will be collaborating on in the future. Code reading is a crucial skill that allows us to understand projects, it will be for effective collaboration and development.
