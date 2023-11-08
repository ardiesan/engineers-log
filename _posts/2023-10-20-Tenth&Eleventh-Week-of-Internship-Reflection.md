---
layout: post
title: "Reflecting on the Tenth and Eleventh Week of My Internship"
author: jwapano
categories: 
- internship
image: assets/images/wapano-tenth-week.jpg
---


## Tenth Week Reflection:

### Day 1: Remote Server File Fetching

This task was a significant step in my learning journey. By crafting the shell script to automate backup retrieval, I deepened my understanding of scripting and server operations. This script seamlessly brings archived .tgz backups from the remote server to my local machine. With the cron job scheduled for every Saturday at midnight, it not only streamlines our processes but also serves as a valuable lesson in the power of automation in improving efficiency and expanding my technical skills.

### Day 2: Exploring GitHub Workflows & CICD

Today, we're shifting our focus to Github Workflows & Actions and diving into the world of Continuous Integration and Continuous Deployment (CICD).

The experience of automating backup retrieval has taught me the value of automation. Now, as I explore Github Workflows & Actions, I'm excited to see how this knowledge can apply to software development, making our processes more efficient.

CICD is an interesting concept, promising to streamline software development and deployment. It's a natural progression from my previous task, and I can't wait to see how it improves the quality of our projects.

### Day 3: Exploring the 'Poor Man's VPN' and Reverse SSH

Today, we received an assignment to delve into Reverse SSH and the 'Poor Man's VPN' concept. The 'Poor Man's VPN' represents a DIY solution enabling users to remotely access their home networks, bolstering online privacy without the expense of traditional VPN services. Reverse SSH is a technique that securely connects a remote computer to a local network, typically positioned behind a firewall. It grants remote access and resource management from a distance, with the connection initiated from the remote end, making it invaluable for remote administration and troubleshooting. A notable example is NGROK.

In the afternoon, our mentor also discussed the Document Object Model (DOM), which was an enlightening experience. It served as a valuable refresher and deepened my understanding of the topic.

## Eleventh Week Reflection:

## Day 1 Reverse SSH: Ngrok

Last week, we were assigned to conduct research about reverse SSH. Today, our task is to use ngrok and expose the fst-admin-ticket-system application to our fellow interns for access. However, we encountered a blocker along the way - we couldn't gain access to the Google OAuth login cloud since it was deployed via reverse SSH. To solve this issue, we created a new one to use for our OAuth. We modified some codes and in the end, we successfully configured it.

## Day 2 GitHub Actions and Workflow

Today, I configured continuous development using GitHub Actions and workflows to automatically synchronize the 'main' branch with the 'production (jwapano.ronins.site)' branch whenever changes are pushed to 'main.' Here's a summary of the steps I took for this exercise:

1. Created a repo and cloned my remote server: jwapano.ronins.site.
2. Created two branches: 'main' and 'production.'
3. Set up a custom workflow by navigating to the 'Actions' tab in the GitHub repository.
4. Created a 'deploy.yml' file and added the necessary code within the '.github/workflows/' directory.
   
Configuring this exercise posed some challenges due to permission errors. It took me some time to realize that I needed to generate a personal access token, add it as a secret variable, and use it to resolve this issue and make the workflow function correctly. After several attempts, I was able to successfully ran the workflow.

## Day 3 Codium AI

Today marks my first encounter with Codium AI, and I must say it has already proven to be incredibly useful when it comes to creating test cases for my project. The platform's ability to analyze code, docstrings, and comments, and then generate relevant and accurate test suggestions in less than a minute, is truly remarkable. It's a valuable tool for developers, and I am eager to explore its potential further in the future.