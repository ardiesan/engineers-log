---
layout: post
title: "Fifth week of Internship: Reflection"
author: jwapano
categories: 
- internship
image: assets/images/wapano-fifth-week.jpg
---
In my fifth week of internship, my fellow interns and I collaborated to tackle various issues in the admin ticketing system. We were able to successfully find and fix the problems at hand. Additionally, we delved into the topic of SSH and gained a deeper understanding of it. Allow me to share what we accomplished during this time.

## Fifth Week Reflection:

### Day 1: A Day of Learning: Bugs, SSH, and Unexpected Challenges

Today was the first time I experienced a very busy day as an intern at this company. It was indeed a long day but filled with valuable knowledge. Here's how my day went:

In the morning, our mentor discussed how to properly write a bug report and emphasized the importance of following a standardized format to make it more professional. He also mentioned that when reporting a bug, we should not only identify the problem but also provide a solution. Consequently, my fellow interns and I discussed and agreed upon an appropriate format/template for bug reporting. After our discussion, we proceeded to update our tickets in JIRA and provided proposed solutions.

Once we had completed updating our tickets, we delved into the topic of SSH (Secure Shell). The main goal of this session was to set up and deploy a basic Laravel application. Our mentor explained the significance of SSH in software development and its various uses. SSH is crucial in web development because it offers secure remote access to servers, enabling developers to manage, transfer files, and deploy applications safely. Additionally, it supports database management, tunneling, and automation, enhancing security and efficiency in web development tasks.

We also discussed PKI, which stands for "Public Key Infrastructure." PKI is designed to ensure secure communication, authentication, and data integrity in various online environments, including web applications, email systems, and secure network communication. During this discussion, we focused specifically on public keys and private keys. SSH relies on a pair of keys for authentication and encryption. It is one of the essential steps in securely authenticating machines.

1. **Public Key**: This key is shared openly and placed on the server you want to access securely. It's like giving someone a lock without the key, and they can only open it if they have the matching key. It's safe to share your public key.

2. **Private Key**: This key is kept secret and securely stored on your computer or device. It's the key that unlocks the lock mentioned above. Never share your private key, as it grants access to your server or system.

When you connect to a server, your computer uses your private key to prove that it holds the corresponding public key, which is already on the server. If the server recognizes your public key and verifies your private key, it grants you access without needing a password, making the connection more secure and convenient.

Our mentor taught us how to generate and locate both the public and private SSH keys on our machines by executing the following commands in the terminal:
- To generate a key pair for SSH authentication: `ssh-keygen -t ed25519`
- To locate the private key: `cat ~/.ssh/id_ed25519`
- To locate the public key: `cat ~/.ssh/id_ed25519.pub`"

He also demonstrated how it works and later created a temporary user account on his server, allowing us to SSH into the server using our laptops for hands-on practice. To connect to a server via SSH terminal, here's the syntax: `ssh -i {private-key} {username}@{server-name/ip-address}`. However, there was a twist: after accessing the server, we had to transfer files between our local machines and the remote server using SCP (Secure Copy Protocol). SCP is a network protocol used for securely transferring files between hosts over an SSH connection. Our mentor introduced us to the basic syntax of the SCP command, which is `scp -i {private-key} {source} {dest}`. Initially, it was challenging, but in the end, I completed the exercise and transferred an HTML file. 

In the afternoon, we proceeded to learn more about SSH, but this time it was different. This time, we will be using two devices: our Mac laptops and our smartphones. For smartphones, we needed to install F-Droid and Termux to use the terminal. He presented us with a 15-minute challenge: SSH from our laptop to our phone and from our phone to the server, with authorized keys set up. This configuration allows the devices to connect without needing a password, making the connection more secure and convenient. As a reward for completing the challenge, he offered us free access to the remote server and provided each of us with personal accounts, granting database access for deploying applications and storing files, which we can access from anywhere.

At first, we were very hesitant because the morning exercise had taken us a lot of time to configure, and we were not confident that 15 minutes would be enough. However, for the sake of the learning experience, we accepted the challenge. Our mentor provided us with the steps for configuration, but as first-timers, it was very difficult and confusing. During the early phase of the challenge, I wasn't able to SSH from my laptop to my phone due to some blockers. To SSH from the laptop to the phone, both devices had to be connected to the same router. There were three Wi-Fi connections in the building, and two of them didn't work, so it was a trial-and-error method. Eventually, I was able to establish an SSH connection, but it took me a lot of time to figure things out. Another challenging procedure that hindered my progress was generating both private and public keys because I forgot to execute `ssh-keygen -t ed25519` on my phone using Termux, leading to more confusion. Additionally, I ended up using the SCP method instead of simply copying and pasting the public keys to the `authorized_keys` file. In the end, it was not a 15-minute challenge because we ended up running overtime. However, overall, it was a really fun experience, and I learned a lot. I'm very thankful to have had this experience.



### Day 2: Streamlining SSH Configuration and Resolving Localization Bugs in fst-admin-ticket-system

After completing the SSH tasks and challenges on the previous working day, I tested and verified the changes I made in the SSH configuration. The authorized keys are now functioning as intended. Whenever I attempt an SSH connection from my laptop to my phone and from my phone to the remote server, it no longer prompts me for a password; instead, it asks for the passphrase. This is a positive outcome.

Following this, I proceeded with my tasks for the day, which included identifying bugs in the fst-admin-ticket-system. I successfully located a bug in the Japanese Localization related to the Pending button. The issue arises when the text is too long, causing it to break and get cut off onto a new line. To address this, I created a bug ticket in JIRA and assigned it to my fellow interns for resolution.

Additionally, one of my fellow interns assigned me a bug related to the dashboard. The problem was that the tables were overflowing their container. In the end, I managed to fix this bug, created a pull request, and submitted a review request in the internship channel.

### Day 3: Prioritizing Functional Issues: Identifying Inconsistencies and Bugs in the Application

My fellow interns and I are continuing to work on identifying inconsistencies and bugs in the application. However, for today, we will be prioritizing functional issues, rather than cosmetic or display inconsistencies. Furthermore, our mentor will review the ticket before we commence our work to make sure that our tickets are effective.