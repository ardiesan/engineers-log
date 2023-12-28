---
layout: post
title: "Sixth Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/sixthweek.jpeg
---
This week I learned about shell commands, cybersecurity, and Git configurations. Me and my co-intern did code reading, which helped us understand projects better. 

---
## Day 1: Exploring Git: Branching and Stashing

#### Branching for Organized Development
In Git, branching allows us to work on different parts of a project without affecting the main codebase. We learned how to switch to a different branch using the `git checkout` command. By giving a name to the branch, we can track it and work on specific tasks without mixing everything up.

For instance:

- `git checkout raya-ay` switches to the "raya-ay" branch.
- `git checkout -b exercise-on/raya-ay` creates and switches to a new branch named "exercise-on/raya-ay".
- `git branch` shows what branch you are currently in.

Our mentor also taught us about the word "upstream" – the place where our code is stored when committing. To make changes, we follow a process. First, we use `git fetch --all` to get a local copy of all changes from the remote. Fetching doesn't immediately bring the source code into our local directory, we still need to perform a pull. After fetching, a `git pull origin raya-ay` brings the changes into our branch.

####  Detailed and Verified Commits
A major takeaway was enhancing our commit messages. Adding more details and descriptions helps in tracking changes. Git logs allow us to review these changes. We emphasized the importance of honesty – version control systems can track everything, so accuracy matters.

Additionally, we learned two ways to verify Git commits:

1. Attaching a signature to configuration.
2. Editing commits from the web interface. Though the web interface shows the signature is from the web, it's preferable to use the command line interface.

#### Simplified Development
Git makes software development much more manageable. With branching, organized development is possible, allowing us to work on different parts without causing chaos. Committing with a good message ensures clarity. By learning these fundamental Git concepts, we will be more effective and organized.

#### Analyzing Changes with `git diff`
Git can show differences between versions through the `git diff` command. This command provides a visual representation of changes, highlighting which lines were added and which were removed. When using tools like Visual Studio Code, the + and - symbols help us quickly identify additions and deletions.

#### `git stash`
When conflicts arise, a solution emerges in the form of Git stash. We dived into the commands that let us stash our changes and effectively remove and apply the stashed changes. Although mastering this technique may require some diligent study, its potential to circumvent conflicts is invaluable.

---
## Day 2: Middleware, Model and Controller

When conflicts arise, a solution emerges in the form of Git stash. We dived into the commands that let us stash our changes and effectively remove and apply the stashed changes. Although mastering this technique may require some diligent study, its potential to circumvent conflicts is invaluable. 

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
