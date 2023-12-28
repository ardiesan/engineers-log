---
layout: post
title: "A Monthly Retrospective"
author: raya-ay
categories: 
- internship
image: assets/images/anthony/6th-week.png
---

Looking back, it is getting close to two months since I started my internship here. It has been a very fruitfly experience so far although I may be biased since this is the path that I took, but I don't think I would be able to do this much if I applied to any other company. I have gotten a lot of insight into what it means to be working in this globalized industry. Here's a summary of what my experiences are so far.

---

## Effective Communication
---

Effective communication is vital to ensuring everything goes smoothly. In reporting bugs, it is necessary to make sure that the other party understands what you are talking about and make sure that you are both on the same page. There may be issues in communications, these issues could be the result of there not being enough clarity on stating what to problem is, and perhaps there is no mention of how to reproduce the bug that is being issued. Maybe there is no clear guideline on how to fix the problem that is being talked about.

To solve this communication gap, one would have to put themselves in the perspective of the other person, would they be able to understand what you are saying, with zero context? No matter how redundant it may be, make sure that you can drive the point across, to promote a more harmonious work environment.


## Friendship Branch
---

Usually, when working on a project, each person would be working on their task and feature, which means that they will be working on an isolated branch with no interference with another branch to prevent complications such as affecting each other's code. But what if the feature is a task too big for a single person to handle? Then it would require more people to work on the said feature. This would mean that the users assigned to that task would have to be on the same branch. This scenario was the basis of the exercise that I and my fellow interns have done. Our task was to work on a single file in which we would make an article on a topic we all agreed upon. We then understand what happens if the file we have in our system is not up to date with the file that has been pushed to the branch. As well as how we were able to avoid messing up each other's inputs

---

## Stop Bugging Me
---

My fellow interns and I were tasked to locate, identify, and report the bugs we found in a project, as well as make a proposal on how to solve the issue. There were numerous visual bugs that we noticed as we had noticed and the next step we had to take was to report them through a ticket in Jira. In the ticket, we were required to thoroughly describe the bug, enumerate the steps on how to reproduce the bug, as well as suggest a proposal on how to resolve the issue.

This also acts as an application of my previous reflection, about effective communication. Although it may be a process that one, who has just been introduced to, sees as time-consuming. I reflected on that aspect and came to realize that bug reporting is a necessary step in the process to ensure that we adhere to the conventions and standards of this industry.


## Public Key Infrastructure
---

__**Public Key Infrastructure**__ (PKI) or Public-Private Key pairs. It is a system that uses cryptographic public keys that are connected to a digital certificate, which authenticates the device or user sending the digital communication. It protects and authenticates communications between servers and users. The Secure Shell (SSH) utilizes this concept as a network protocol that gives users, particularly system administrators, a secure way to access a computer over an unsecured network. Public & Private key pairs are used together to encrypt and decrypt information. If anyone other than the owner of the private key tries to decrypt the information using the public key, the information will be unreadable. This is for increased security as it prevents unauthorized users from accessing sensitive information.

We did a short exercise on how to SSH to a website via the Macbook. Afterward was the real challenge, what we had to do was SSH from our Macbook into our phones and then, from our phones, we would SSH to the same website mentioned before. It proved to be a real challenge because we didn't know how to place our public keys in the system we SSH'ed into. After a grueling 4 hours, we succeeded in the task and we no longer needed to include our private keys and had no prompt to input the password since our device is recognized through the public key we added to the authorized keys of the system.


## Into the Live(wire)light
---

__**Livewire**__ is a full-stack framework for Laravel that makes building dynamic interfaces simple. It renders the initial component output with the page (like a Blade include). When an interaction occurs, Livewire makes an AJAX request to the server with the updated data. This would result in only the component to be re-rendered.

The others and I were tasked with researching Livewire, which is a framework that was promoted to be easier and less complicated than other similar frameworks such as Vue and React. I started a new project and followed the documentation on how to make a component, along with watching a few tutorials that explored the functionalities of Livewire and its utilizations. Though I aim to do more complex projects in the future to further improve my understanding of its features, aside from that, it would also help me on Laravel as a whole and not only on singular components. I would like to make a whole project from scratch, from making migrations, controllers, and views to handling routes and such.