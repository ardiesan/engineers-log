---
layout: post
title: "Tales of the 16th Week Intern"
author: raya-ay
categories: 
- internship
# image: assets/images/anthony/16th-week.png
---

Now that I have finally finished making my Jekyll project, this week was dedicated to deploying the project online using GitHub pages and implementing an action workflow for it.

---


# Wednesday (2023-11-29)
---

So this day would finally be the day where I would deploy the project using GitHub pages. The last time I deployed using GitHub pages was back when I was in my first year in 2019. It was a simple static website which is like a gallery for wallpapers for desktop and mobile screens.

Just like the GitHub workflows folder, GitHub also looks out for certain named entities, in this case, it is not a file, but a branch. If a gh-pages branch is present, Github knows that it can make its website and deploy it within its own server. So after watching the short tutorial on GitHub pages, I was successfully able to have my blog up and running on a live server.

At the end of the day, I caught up on my latest weekly reflection after not having finished the ones two weeks prior.

# Friday (2023-12-01)
---

During our daily standup meeting, after my fellow interns and I said what we had done and what we planned to do, our supervisor guided us on instead of having our action be run on every push on a certain branch, what we could do instead is to apply version tagging to our Git pushes.

What version tagging does is that a tag is associated with a push these could be a version tag like "v2.\*" or "v1.0". If the workflow is looking for a certain tag when a push is made to a branch and if that push associated has the corresponding tag together with it, the workflow will start operating. 
