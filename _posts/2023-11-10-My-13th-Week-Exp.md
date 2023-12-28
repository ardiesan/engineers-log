---
layout: post
title: "Tales of the 13th Week Intern"
author: raya-ay
categories: 
- internship
# image: assets/images/anthony/13th-week.png
---

You may notice the gap between this reflection and the previous and and it was due to the "weeklong" weekend I had due to all saint's day and all soul's day. This week was spent familiarizing myself with Ruby and studying the nature of a decentralized Git workflow

---

## Monday (2023-11-06)
---

The day started with being tasked with attempting to run our engineer's log locally on our Macbooks. I assumed it would only be a task that could be done in a few seconds, just follow the instructions and type `Jekyll serve` and I thought we would be all good. But it proved to be quite a challenge, things weren't as simple as we wanted them to be. There were issues with write permission and things along those lines, so we attempted to override it by including the `sudo` keyword. But that did not solve the issue.

After intensively reading the forums online the issue was due to the default ruby installation of Mac and what was recommended to do is to use some form of ruby version control. This task was easy to do because I had a similar experience with Python where I had to change my environment so that it would only have the modules that I needed.

Afterward, I successfully ran the engineer's log on my device.


## Wednesday (2023-11-08)
---

Going back to my previous task, it involved using Gem and Gemfiles, which is like a package manager for Ruby with prebuilt code made by other people which is equivalent to the Node.js of Javascript and the Composer of PHP.

With that in mind, I decided to spend the day exploring and researching Ruby.

In the latter half of the day, I explored the concept of Git having a decentralized workflow. As it turns out, from the words of another developer, Git is both (and neither).

*Git is centralized* in the sense that anyone with a clone of a particular repository is theoretically "equal" to any other developer with a clone of the same repo. One of the main reasons this approach is used is to allow any developer to continue their work without the need to always be connected to a centralized master server. If you have your complete copy, and it's "equal" to any other, you can develop against it and sync up later.

*Git is decentralized* in which, surprisingly, mainly for the same reason given above. One of the core concepts is that there is no need for a "main" server. The problem with that is, that in many situations (like a software engineer for a large company), there is a need to have a centralized master.

## Friday (2023-11-10)
---

Lastly, for this week, I have continued reading about git decentralization.

With that being my only task, I reflected on when I first joined this company and there our manager demonstrated to us how our pushed articles from the PR were added to the engineer's log and the interns and I noticed how it went live instantly, all he did was approved our PRs and we could see our articles online already. With the knowledge I have, I now understand how that was possible, it was with the combination of GitHub actions, the CICD workflow, and Jekyll. So then I tasked myself with figuring out how to implement that process so that I may use that myself in the future