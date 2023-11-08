---
layout: post
title: "Fourth week of Internship: Reflection"
author: jwapano
categories: 
- internship
image: assets/images/wapano-fourth-week.jpg
---
During the fourth week of my internship, I experienced significant growth and development. I'm thrilled to share that we were finally assigned the task of modifying and rectifying inconsistencies within specific modules of the fst-admin-ticket-system application. Here's a brief reflection on my experiences.

## Fourth Week Reflection:

### Day 1: Identifying and Resolving Inconsistencies
Today, we were assigned a task to search for inconsistencies in the application. If we come across any inconsistencies, we post them in the internship channel, describe the issues, and make a proposal for changes. Afterward, we wait for approval from our mentor. Once we receive the approval, we proceed to make the necessary modifications. I was experiencing both nervousness and excitement simultaneously.

I successfully pinpointed an inconsistency in the user management module. Upon investigating, I discovered that when editing a user's role from "SUPER_ADMIN" to "LEAD" within the module, the department drop-down menu continues to display the default value "NULL" despite the role change. This display inconsistency could potentially lead to accidental errors, such as saving a user's role as "LEAD" without assigning the appropriate department. Such errors could have negative impacts on their operations. By the end of the day, I had managed to report and address this issue.

### Day 2: Learning Opportunity: First Encounter with JIRA and Bug Ticket Creation

After receiving feedback on our inconsistency report yesterday, today's task was to transition it onto the JIRA application. My objective was to create a "Bug" issue within the Internship PH '23 project, complete with a descriptive title and a detailed set of reproduction steps. Unfortunately, I was initially unable to access the project due to a permission issue, so I reached out to my mentor for assistance. I was concerned about falling behind my fellow interns who had already started working on their assignments while I was delayed. However, despite the setback, I found the experience to be valuable as it was my first time using JIRA. By the end of the day, I successfully created the bug ticket, fixed the issue, and submitted a pull request. Overall, I am satisfied with how it turned out.

### Day 3: Collaborative Bug-Hunting and Ticket Creation

Today, our mentor instructed us to focus on finding another bug and creating a corresponding JIRA ticket for it. The task involved assigning the ticket that i have created to my fellow interns. Collaboratively, my co-interns and I engaged in brainstorming sessions to enhance and address bugs in the fst-admin-ticket-system application. Our exploration led us to pinpoint specific modules with bugs that required to be fixed. Consequently, we successfully created tickets and assigned them to the team.

In my own bug ticket report, I identified an issue where the width of the profile section within the sidebar exceeds the appropriate boundaries when the webpage is resized by at least 40% from left to right. This inconsistency in display can potentially disrupt the user experience while navigating the application. 

The bug ticket assigned to me required fixing an issue where the dashboard failed to display any data in the recent updates table when selecting 'ALL' from its drop-down query. Furthermore, the default value for the statuses was incorrectly set to 'NEW' instead of 'ALL.' After some work, I successfully resolved the problem and ensured that the drop-down menu for 'ALL' now functions correctly."

The collaborative effort was both enjoyable and productive. It enabled us to generate ideas more efficiently, fostering a positive environment for teamwork and innovation.














