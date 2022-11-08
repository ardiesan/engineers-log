---
layout: post
title: "An Intern's Guide to Tools and IDE for Software Development"
author: jdayuday
categories:
- internship
- tools
- IDE
---

The process of installation and familiarizing yourself with new tools and IDE during your work can be stressful.
Things may go wrong and right, but we know that if new things arrive, we need to adapt and make some adjustments for ourselves. As my mentor said, "As a software engineer, you should never bind yourself to certain things, especially in technology" Technology change drastically, every quarter, month, and even week things change so fast. So here are some of my experiences in installing and familiarizing myself with new tools and IDE for my internship.


## The First Week

The first week of my internship as a software engineer in fullspeed technologies. The overall experience on my first week was great and enjoyable, on that week me and my co-intern are tasked with different reading materials such as the topics on effective communication and the proper way the report a bug.

In the second week of my internship program, our mentor started giving us simple tasks and introducing us to the different software engineering tools, IDE, and communication software for our daily collaboration.

### Tools, IDE, or Softwares

* Slack - for daily communication for team members.
* **Git and Github** - project source control and managing different source code for a project.
* **VSCODE** - IDE for editing code.
* **Docker** and docker compose - used for creating and manage docker image file and containers.
* **command line** / terminal

All of these tools and IDE were installed using command line interface (CLI), and here are the commands for homebrew.

* **Slack** - `brew install --cask slack`
* **Git and Github** - `brew install git`
* **VSCODE** - `brew install --cask visual-studio-code`
* **Docker** and docker compose - `brew install docker`, `brew install docker-compose`


## The Second Week

We were tasked to install and familiarize all the mentioned tools and IDE above. During the task execution, we slowly discussed the things we need to remember and practice on following standard procedures in taking, asking, and requesting a ticket review.

In the following days, we can accomplish tasks/tickets and tie things together on what exactly the goal of each task is and how it can be connected to the other tools that we are using.

And lastly, we are tasked every friday to create an article about some of our learnings and or about the tasks that we accomplished. We submit the article through a pull request (PR) to a GitHub repository that is specifically for internship. The main goal of the task was not only to create an article out of our learning, the goal of the task is to get us to use the command line (CLI) for cloning, committing, and pushing changes to the GitHub repository, to see if we fully understand git without the fancy GUI.


### CLI, More brew commands

* **MySQL** - `brew install mysql`
* **PhpStorm** - `brew install --cask phpstorm`

### Why Homebrew & CLI Installation

Maybe you have noticed the things that I have installed on my local machine I only use brew commands for the command line for every installation, but why? 

Well, installing using brew or any other package management system. First, it is simple and more efficient rather than using the conventional package installer which may take time to finish and configure. Second, the process of unzipping/extracting download folder. We cannot deny that it is one of the most painful parts of downloading an installer for a certain application, tools, and IDE.

### What About Cask?

Maybe you are wondering what's the difference between `brew install` on this git uses the homebrew package also called "formula/formulae" while `brew install --cask` which runs a GUI for the third-party installer. Between the two brew install is a better choice for installation in general as a "Mac user" because it downloads directly from the Git website.


## Weekly Processing Day

On the last day of our sprint, we are tasked to create another article and make a pull request out of it. It's a good thing I Already took the ticket on Installation of PhpStorm and familiarized it. Instead of using CLI. I did utilize the built-in terminal inside the IDE and practice how to clone a GitHub repository using PhpStorm GUI.

Additionally, I was planning to connect my MySQL docker container to MySQL workbench and PhpStorm. Lastly, we are advised by our mentor to signed our commit for git and github for security and protection.

This is the brew command I used:

* **MySQL workbench** - `brew install --cask mysqlworkbench`
