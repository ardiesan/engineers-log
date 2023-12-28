---
layout: post
title: "Fifteenth Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/mtrinidad-week15.png
---
CodiumAI and PHPStan, AI Image Generation, PHPStan with GitHub Actions, and SonarLint

---
## Day 1: CodiumAI and PHPStan

Monday was all about exploring two important tools: CodiumAI and PHPStan. CodiumAI helps generate tests for our app and it could also explain a block of code for us, while PHPStan spots bugs in our code without having to run the app. With PHPStan, we can focus on specific parts of our app, saving time, especially in Laravel where checking the whole app can take a while. 

CodiumAI is handy for generating tests, but they're not always perfect and need some manual tweaks. It's great for understanding code and suggesting tests. Using both PHPStan and CodiumAI together is a game-changer for testing our Laravel app. We can even automate these tests using GitHub workflows, which will save us a lot of time.

---
## Day 2: AI Image Generation

On the second day, we were tasked by our manager to generate an AI image for each reflection entry. I explored various free AI image generation tools, but most didn't create very accurate images, probably because of my prompts.

I tried getimg.ai, which worked well, but it had a limit of 100 credits, allowing only 100 free image generations. It was a fascinating task, showcasing AI's potential. Free versions can produce good images only if the user provides good instructions.
I believe paid AI versions might produce more accurate images, although I haven't tried them yet. This day, I realized how valuable AI is as a tool for developers. Adapting to and making the most of it will be crucial for our work.

---
## Day 3: PHPStan with GitHub Actions

Today revolved around perfecting the GitHub workflows for my Laravel app. I stumbled upon a GitHub action for PHPStan, it is like a code proofreader, and it automatically tidies up and checks my code without actually running the app. It's pretty nifty, but getting the workflows just right? That's a real challenge, trial and error all the way.

I configured my PHPStan GitHub actions to only inspect the directories where I wrote my code. It's not built to snoop around places like the 'vendor' directory in a Laravel project or the entire project where there's a ton of pre-written code. The PHPStan docs made it clear: it's not our job to fix mistakes in code we didn't write, and that just makes sense.

---
## Day 4: SonarLint

The last day of the week brought the anticipation of a long weekend. It was a simple day, mainly finishing up my check-in log. Our new task involved exploring SonarLint, a tool like PHPStan that spots issues leading to bugs and errors. I set it up by installing the SonarLint extension for Visual Studio Code, and unlike PHPStan, it doesn’t need any manual commands to start working. Simply opening a source file reveals the reported issues, highlighted and it will be listed in the 'Problems' panel.

This week taught me a few important things. First off, every tool, like PHPStan and SonarLint, finds mistakes in its way. Second, figuring out GitHub Actions and workflows felt a bit like solving a puzzle, a lot of trial and error. Lastly, I learned that running checks only on our code saves time and makes things simpler.
