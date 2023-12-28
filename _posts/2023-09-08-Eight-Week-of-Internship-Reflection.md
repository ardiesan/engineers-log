---
layout: post
title: "Eight Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/eightweek.jpeg
---
SSH and SCP Exploration, Ticket Etiquette, Ticket Handling, A Valuable Lesson in Handling a Ticket

---
## Day 1: SSH and SCP Exploration

Today, we talked about how to report bugs in our admin ticketing system, which we'll do in JIRA. Our manager told us the right way to do it. When we find a bug, we should not just say, "Hey, there's a problem!" We should also suggest how to fix it. This is important because it shows we're not just complaining, we're thinking about how to make our system better. After this chat, we went back to our previous bug reports on JIRA. I learned that when making a bug report, the title should describe the issue, not the solution. So, I fixed my report title and added a proposed solution in the description. Also, if we need to change a report, we shouldn't delete it because that looks strange. We should just edit it. Lastly, before starting to address a bug report or a ticket, it's smart to ask questions and verify. This way, we will not have to bother the reporter again with more questions, which saves time.

In the afternoon, we had an interesting session with our mentor. They introduced us to something called SSH, which stands for Secure Shell.

#### What is SSH and why do we use it?
SSH, or Secure Shell is a network protocol that lets us securely access and control computers or servers over a network. We use it to remotely manage systems, execute commands, transfer files, and ensure our communications are private and protected from unauthorized access. It's like a secure key to unlock the door to another computer.

I had heard of SSH before, but I didn't know how it worked until our manager gave us a lesson. He showed us how to use SSH to connect to a server, It was pretty neat, and he used his server to demonstrate it to us.

#### Public Keys and Private Keys
In SSH, we have two special keys the private and public keys. Think of private keys like a secret key that opens the door to your computer or server. It's a secret, so you never share it with anyone. Now, your public key is like a lock that matches your secret key. You can share it freely, and others can use it to talk to your computer or server, but they can't open the door with it. You can find these keys in your home directory, in a folder called `~/.ssh`. You can easily identify which is a public key because it has a `.pub` at the end, while the private key doesn't have any extension.

Before we can enter a server using SSH, we need to prove who we are. For our practice, we gave our manager our public keys. He put them in a file called `~/.ssh/authorized_keys` on his server. With our public keys there, the server recognizes us, and we become like friends. Now we can access it securely. The private key is our identity, and it matches with our public key. After SSH, we also talked about SCP or Secure Copy Protocol.

To connect to a server using SSH, you can use the following command:

`ssh username@servername` or `ssh username@ip_address`

Replace `username` with your username on the server, and `servername` or `ip_address` with the server's domain name or its IP address.

#### What is SCP and why do we use it?
SCP, or Secure Copy Protocol is a way to copy files securely between computers over a network. We use it to send and receive files while ensuring they remain safe from unauthorized access. It's like a trusted courier service for our files. 

The `scp` command is used to securely copy files and directories between two computers over an SSH connection.

`scp <source> <destination>`

- `source` is the file or directory you want to copy from your local machine or another remote server.
- `destination` is where you want to copy the file or directory, which can be on your local machine or a remote server.

Example:

1. Copy a file from your local machine to a remote server:

`scp /path/to/local/file username@servername:/path/to/destination/`

2. Copy a file from a remote server to your local machine:

`scp username@servername:/path/to/remote/file /path/to/destination/`

#### SSH and SCP Exercise
Later in the afternoon, we had an exciting task. We were given a challenge, to connect our Mac computers with our Android phones through SSH, and then connect these Android phones to our manager's server. We had just 15 minutes to complete this challenge, and honestly, at the start, I had doubts about finishing it in time. Still, I decided to give it a shot.

Our first step was to install Termux on our Android phones. Then, we had to grant permission for our MacBooks to connect to Termux via SSH, and also allow Termux to access our manager's server through SSH. This wasn't all, we needed to use SCP to copy our Mac's public key into Termux and Termux's public key into our manager's server.

As expected, I didn't complete everything within the 15-minute timeframe, and neither could my fellow interns. But our manager was understanding and let us finish the exercise. Along the way, we ran into various errors, which made it a bit stressful. However, when we finally succeeded, it felt very rewarding. To wrap up the day, we treated ourselves to some delicious batchoy.

---
## Day 2: Ticket Etiquette

This day was a bit tricky for me because I had to take a half-day off. I needed to attend an afternoon class that was suddenly rescheduled, and it conflicted with my internship schedule. It made me feel bad because I didn't want to fall behind in my internship.

The good thing is that this class only happens once a week. So, I won't miss too much, and I can keep up with my internship work. Sometimes, unexpected changes happen, and we need to adapt.

During our daily standup, our mentor shared some important insights about ticket handling. When we complete a ticket or task, we should request a review in our Slack channel. However, this request should follow a specific format for clarity, just like how we follow conventions in programming languages. It's not enough to create a pull request; we must also inform the reviewer or team lead in our channel. Additionally, there should always be a discussion for a ticket in JIRA. This helps us clarify and verify things properly. Ticket discussions also have their conventions. We shouldn't just write everything randomly; we should format it for easy reading by the reviewer or lead. Following these practices ensures effective communication and collaboration within the team.

---
## Day 3: Ticket Handling

Today was a bit different because my fellow interns were attending their classes, and I was the only one in the office during the morning. It felt a little quiet without them. I used this time on a ticket that my fellow intern had assigned to me the day before. The task was quite straightforward, I needed to add a CSS attribute to a specific element in our project. Once I finished the task, I submitted a pull request to get my changes reviewed. I also informed our mentor about the request in our Slack channel. It's essential to keep everyone in the loop. Additionally, I updated the ticket in JIRA to let the reporter know that I had made the change they requested. This day taught me the importance of clear communication and staying organized. Even when working alone, it's vital to keep everyone informed about your progress and updates on tasks. 

---
## Day 4: A Valuable Lesson in Handling a Ticket

Today's stand-up meeting with our mentor taught me something crucial. I encountered a ticket that needed fixing, but I approached it differently because I had trouble finding the right CSS code. Instead, I used a JavaScript solution. However, my mentor pointed out an important thing I missed. I didn't think about what would happen if someone turned off JavaScript in their web browser. Unlike CSS, JavaScript can be turned off, which would make my solution useless. Our mentor emphasized the need to assess and verify our approach before diving into a ticket.

Our main job for the day was to review the entire admin ticketing system to find issues that affect how it works, not just how it looks. Before we could work on these issues, we had to tell our mentor about them. This day taught me that solving problems in software development isn't just about finding a solution; it's about finding the right solution that works in all situations. 



