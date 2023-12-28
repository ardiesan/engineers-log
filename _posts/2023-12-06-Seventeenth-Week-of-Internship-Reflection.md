---
layout: post
title: "Reflecting on the Seventeenth Week of My Internship"
author: jwapano
categories: 
- internship
image: assets/images/wapano-seventeenth-week.png
---

Over the span of three days, I delved into GitHub Version Tagging, comprehending its significance as a snapshot of a project at a specific point. 

## Seventeenth Week Reflection:

### Day 1: Exploring GitHub Version Tagging

Today, our task is to explore GitHub Version Tagging. Version tagging, in essence, serves as a snapshot of a project at a specific point in time. It freezes the dynamic nature of code, encapsulating the collective efforts, decisions, and innovations of a development team. In this digital collection of versions, each tag is a carefully crafted display, showcasing the evolution and maturity of the codebase.

Here's a basic overview of how version tagging works on GitHub:

Create a Release:

Releases on GitHub are a way to package and deliver software to users. You can create a release by going to the "Releases" tab in your GitHub repository and clicking on "Draft a new release."

Tagging the Release:

When you create a release, you have the option to associate it with a Git tag. A tag is a reference to a specific commit in your repository's history. It's like a snapshot of your code at a particular point in time.

Version Numbering:

It's common to use semantic versioning (SemVer) for version numbers. Semantic versioning typically follows the format of MAJOR.MINOR.PATCH. Each component of the version number has a specific meaning:

- MAJOR: Increments for incompatible API changes.
- MINOR: Increments for backward-compatible new features.
- PATCH: Increments for backward-compatible bug fixes.

Changelog:

When creating a release, you can include a changelog or release notes. This is a summary of what changes have been made in this version. It helps users understand what to expect and what might have changed.

Tagging via Command Line:

You can also create tags directly from the command line using git tag followed by the version number, and then push the tags to GitHub using git push --tags.

Example using command line:

- `git tag -a v1.0.0 -m "Release version 1.0.0"`
- `git push origin v1.0.0`



### Day 2: Version Tagging with GitHub Workflows

After exploring version tagging, my task is to try and implement it into my Laravel and Jekyll applications and automate the process using GitHub Workflows, which I find very challenging. I encountered numerous errors while working on this task, but with the collaboration of me and my fellow interns, we are making progress.

### Day 3: Automated Release workflow

Today, I successfully implemented an automated release workflow for my Jekyll and Laravel applications. This achievement highlights the value of efficient workflows in software development, enhancing productivity and delivery speed. I am thankful for the opportunity to learn and apply these valuable skills.
