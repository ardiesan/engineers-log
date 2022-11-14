---
layout: post
title: "What is a Pull Request, the Process, and Why"
author: nsagnoy
categories:
- internship
- git
- github
- pull request
image: assets/images/pr-request-process-why-01.jpeg
---

The use of **pull request** has been a standard in software development. Its biggest benefit is that it presents an opportunity for a **code review** which is a crucial process in source code management. 

**So, what is a pull request?** 

A pull request, or referred to as **merge request**, is a functionality/feature in GitHub that allows a developer to notify other project collaborators about the pushed changes to a branch in a repository, requesting for these changes to be compared/reviewed and eventually be approved to merge to a base branch. It is mostly a transaction between member and team/project lead or any assigned reviewer to review the code and discuss any potential changes to the code before applying it. This is a vital step in source code management because it provides a layer of protection to the source code.

Now that we have defined a "Pull Request", it is important that we know its core purpose. With that, we need to first know what a **Code Review** is about and its benefits.

## What and Benefits of Code Review

To simply put, **Code Review** is an approach in software development wherein fellow developers of a project checks each other's code. Which helps in eliminating typos or mistakes, provide enhancements, and enables team collaboration. Although this process can be viewed as tedious and time-consuming, performing code review is beneficial to maintaining the quality of the code and how it can be improved. Below is an illustration of how a code review works.

<img src="{{ site.baseurl }}/assets/images/code_review.svg" alt="code review process" width="800px">

As shown above, a developer makes code, test's it and then submits/pushes it for a code review. In the code review stage, when an issue or mistake is detected, fixes and changes will be requested back to the developer. This cycle will continue until all issues are solved and finally the code is pushed to the code base. Same process happens with pull request which we will also tackle in this article. 

**Here are other benefits of Code Review:**

- Knowledge is shared among the team 
- Limits Risks and Error Detection
- Ensures and Improves code quality
- Helps with familiarity of the project


## Dos and Don'ts in Pull Request

1. You have to remember that in Git, you cannot create a pull request if you are pushing commits in the main branch. If you do this, the changes will automatically be merged to the main code which is not ideal. So, create a new branch and code there.
2. Always practice to make smaller pull request. Doing this will give you higher chance of having it approved and also lower review time. Not to mention, it also minimizes the review work of the reviewer.
3. Write meaningful/descriptive/useful titles and descriptions for your pull request. This is very helpful especially towards the reviewers. A good PR title and description guides the reviewer through the code which saves a lot of time in code review. 
4. When committing your changes make sure to give descriptive and meaningful commit messages. This is important for tracking commit logs.
5. When changes are requested, they will be conveyed in comment form. Reply to them if needed. 
6. When your pull request is approved and changes are merge to the base branch, please practice to delete the branch you used and checkout to the main/base branch.
7. Last but not the least, never forget to review your work and make sure everything is ready before creating a pull request. So that you can avoid creating unnecessary pull requests that might waste your reviewers time and effort.

## Pull Request - Create and Process

1. To create a Pull Request in GitHub is simple and straightforward. Once you have pushed your local commits to the remote repository, go to the GitHub website and open your repository. A highlighted container will appear. 
   
   <img src="{{ site.baseurl }}/assets/images/pull_request_cont.png" alt="pull request" width="800px"> <br />
   Click "Compare & Pull Request".

   If no highlighted container appears. You can simply go to "Pull Requests" and click "New pull request".

   <img src="{{ site.baseurl }}/assets/images/new_pull_request.png" alt="new pull request" width="800px">

   Note: Make sure you select the correct base and compare branch for the pull request.

   <img src="{{ site.baseurl }}/assets/images/select_branch.png" alt="select branch" width="800px">
   

2. A pull request form will appear. Again, as suggested in the "Dos and Don'ts", give descriptive/meaningful title and description of the request.

   <img src="{{ site.baseurl }}/assets/images/pr_form.png" alt="pull request form" width="800px">

   When you have filled out the form, simply click "Create Pull Request" and you are done.


3. Once it is created, it is open for discussion and modifications.

   
4. The assigned reviewer will then review the code. They can give feedback or request modifications/changes which are added in as comments near the code line.

   <img src="{{ site.baseurl }}/assets/images/comments.png" alt="pull request comments" width="800px">


5. The developer will resolve these issues and replies to the reviewer. This cycle will continue until all issues are addressed/resolved.


6. Once all discussions/issues are resolved, the code will then be merged to the base branch selected when the pull request was created.


## Conclusion

-------

Pull requests are built to facilitate code review and team collaboration in a project. Developers can request review from their colleagues and exchange knowledge from each other on how to improve one's work (vice versa). With this, code quality is ensured and/or enhanced. And at the same time, developers can learn and develop their skills further. 
