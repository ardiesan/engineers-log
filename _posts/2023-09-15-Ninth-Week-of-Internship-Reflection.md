---
layout: post
title: "Ninth Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/ninthweek.jpeg
---
GitHub Pull Requests and Best Practices, Exploring Laravel Livewire, A Day of Laravel Livewire and SSH, and Middleware 

---
## Day 1: GitHub Pull Requests and Best Practices

My first day this week was quite educational. Our manager shared an important lesson about GitHub pull requests. It's essential to include the link to the related Jira ticket in the pull request description. Equally important, the Jira ticket should have a link back to the GitHub pull request.

In the course of the day, I made changes to two of my tickets. The first involved converting a JavaScript function into a CSS media query. I realized that I didn't consider a crucial factor, that some users might disable JavaScript in their browsers, making my solution ineffective. This taught me the importance of considering various scenarios when making code changes.

The second ticket involved moving an inline CSS attribute directly into the CSS file. This change not only improved code readability but also followed best practices by separating styles from the page itself.

Additionally, I learned about draft pull requests. These are handy when you need to make further changes to your work before it's ready for review. I converted my first ticket's pull request into a draft initially because I needed to make some adjustments. Later, I changed it back to a regular pull request once I was satisfied with the changes. This practice ensures that reviewers see the most up-to-date work and can also track our progress on a certain task. 

---
## Day 2: Exploring Laravel Livewire

On the second day of this week, I started learning about a technology that is new to me that is called Laravel Livewire which our manager had introduced the day before. Sadly, I couldn't dive into it then as I had to leave the office early for a class.

Before this, I had never heard of Laravel Livewire. In simple terms, it's a tool that helps us build dynamic web applications in Laravel, a popular PHP framework. It felt somewhat like ReactJS because you can make components, put components inside other components, create full-page components, and send data between them.

So, I started by installing Livewire into my local copy of the admin-ticketing-system. Then, I did some simple exercises from the documentation. These exercises covered creating components, nesting them, making full-page components, rendering components, and handling events and actions. It was a day of exploration and learning, and I look forward to learning more about Laravel Livewire.

---
## Day 3: A Day of Laravel Livewire and SSH

My day was pretty straightforward. I continued my journey into Laravel Livewire, a new technology to me, and refreshed my memory on SSH, something that we discussed a week ago.

Our manager had introduced us to SSH the previous week. Today, I revisited it. I repeated the exercise where I connected my MacBook to my Termux SSH server and then established a connection between the Termux SSH server to our manager's server.

I took the time to read the SSH documentation, where I came across familiar commands like ssh-keygen, ssh-add, and scp, which our manager had previously introduced. It was a day of continuing to explore Laravel Livewire and revisiting SSH, and I look forward to learning more about these topics.

---
## Day 4: Middleware

Today, our goal was to discover middleware, understand its purpose, figure out what belongs to it and what doesn't, and explore the different types of middleware.

### What is a Middleware?
Middleware is like a security guard or a filter for your web application. It sits between the user's request and the application's response and can perform tasks like checking if a user is logged in, validating data, or adding headers to responses. It helps manage and control the flow of data and actions in your web application, ensuring things happen in the right order and with the right conditions.

To create a new Middleware in our Laravel project, we can execute the command:
````
php artisan make:middleware MyNewMiddleware
````
This command will place a new `MyNewMiddleware` class within our `app/Http/Middleware` directory.

**These are a few uses of Middleware:**

- **Authentication:** Middleware can check if a user is logged in or has the right permissions to access certain parts of a website or application. If not, it can redirect them to a login page or deny access.
    
- **Input Validation:** It can validate the data coming from a user to ensure it's safe and meets certain criteria before it's processed.

**Things that we can put in a Middleware:**

- **Logic:** Middleware needs a specific purpose or task to perform. For example, it might check if a user is authenticated.
    
- **Configuration:** Middleware often comes with configuration options. For example, you can configure it to redirect to a specific page if authentication fails.
    

**Things that are not needed in a Middleware:**

- **Database Access:** Middleware should not directly interact with a database. That's typically the job of controllers or models in Laravel.
    
- **View Rendering:** Middleware doesn't render views for the user. It's focused on processing the request and response.


### Types of Middleware

**Global Middleware**: Global middleware is like a rule that applies to every part of your website, no matter which page or action you're on. It's like having a security check at the entrance of a building that everyone must pass through. For example, you can use global middleware to ensure that all users are logged in before they can access any part of your website.

**Route Middleware**: Route middleware is more like specific rules for certain parts of your website. It's like additional security checks or filters that only apply to certain pages or actions. For example, you might use route middleware to make sure only administrators can access the admin panel of your website, while regular users can't.



