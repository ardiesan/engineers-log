---
layout: post
title: "Eighteenth Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/mtrinidad-static-dynamic.png
---
This week, I learned about static and dynamic sites. I played around with Jekyll and GitHub Pages to make my static website. I also wrote about the differences between static and dynamic sites. It was a fun mix of learning and doing!

--- 
## Day 1: Understanding Static and Dynamic Sites

On the first day of the 18th week of my internship, I researched static and dynamic websites and the differences between them.

### Static Sites
- **What are They?** Static sites have fixed content that remains unchanged until manually edited. They're simple, fast, and secure, but may require technical skills for content updates.
- **Example:** This very blog you're reading is a static site powered by Jekyll and GitHub Pages.

### Dynamic Sites
- **What are They?** Dynamic sites change content based on user interactions and database updates. They're interactive and flexible but might be slower and more complex to maintain.

### Advantages
- **Static Sites:** Quick loading, fewer security vulnerabilities, and easier hosting and setup.
- **Dynamic Sites:** Interactivity, personalized content, and more straightforward content management.

### Common Static Site Generators
1. **Jekyll:** A widely used generator that turns text into static websites, suitable for blogs or simple sites.
2. **Hugo:** Known for its speed, Hugo creates websites rapidly, ideal for blogs or portfolios.
3. **Gatsby:** It combines React and GraphQL, often used for web apps, pulling dynamic data into static sites.

### Speed Difference
I learned about the speed differences between static and dynamically generated pages. Some pages are better delivered statically, while others are best generated dynamically, either from the server or the client side.

- **Server-Side Pages:** Utilize server-side scripts like PHP.
- **Client-Side Pages:** Managed by JavaScript, including pages using AJAX or React.js for DOM manipulation.

---
## Day 2: Jekyll and Github Pages

Today was pretty straightforward, my task was to research Jekyll and GitHub Pages.

### So, what are Jekyll and Github Pages?

**Jekyll:** Jekyll is a tool that helps you build websites without a lot of complexity. It takes your written content, which is in a specific format, and turns it into a complete, ready-to-go website. It's like a helpful assistant that saves you from doing all the technical stuff so you can focus on what your website looks like and says.

**GitHub Pages:** GitHub Pages is a free service by GitHub where you can put your website so that others can see it on the internet. It's like having a free space to showcase your website without having to pay for hosting or other technical details. GitHub Pages takes what Jekyll creates and makes sure it's accessible to anyone with an internet connection.

**How Jekyll and GitHub Pages Work Together:** When you use Jekyll to build your website, it generates all the necessary files and structures. GitHub Pages then takes these files and displays your website to the world. It's a smooth collaboration, Jekyll does the building, and GitHub Pages does the showing, making it easy for you to share your work without dealing with technical headaches.

In simpler terms, Jekyll helps you create your website, and GitHub Pages gives you a free spot on the internet to display it for everyone to see. It's a teamwork setup that simplifies the process for you.

I'm happy I got the chance to dive into these technologies. Now, I'm excited about creating my static site. I'm thinking of publishing my articles there, making an "About Me" page, and using it as a cool way to show off my skills and projects. It seems like a great tool for building my portfolio. Looking forward to what I can create with it!

---
## Day 3: My First Jekyll Project

Today was quite hands-on, my main tasks starting my Jekyll project, continuing to read about static and dynamic sites, and beginning to write my article on their advantages and disadvantages.

Before diving into the Jekyll project, I had to make sure I had everything needed. According to their documentation, I needed:

- Ruby version **2.5.0** or higher
- RubyGems
- GCC and Make

Creating the project was a simple process:

1. Installed all prerequisites
2. Installed the Jekyll and Bundler gems:
    `gem install jekyll bundler`
3. Created a new Jekyll site at `./myblog`:
    `jekyll new myblog`
4. Changed into the new directory:
    `cd myblog`
5. Built the site and made it available on a local server:
    `bundle exec jekyll serve`
6. Browsed to http://localhost:4000/
    
It may sound like a lot, but it was pretty straightforward!

### Ruby 101

Since Jekyll is written in Ruby, I took a quick look into Ruby basics:

**Gems:** These are like little packages of code you can use in Ruby projects. Jekyll itself is a gem, and many plugins, like jekyll-feed or jekyll-seo-tag, are gems too.

**Gemfile:** Every Jekyll site has a Gemfile, which contains a list of gems your site needs.

**Bundler:** This is a tool that installs all the gems listed in your Gemfile.

Besides working on the Jekyll project, I also spent time researching static and dynamic sites. In fact, I created a separate article titled: Static Sites and Dynamic Sites: A Contrast, where I talked about how these two types of websites are different. If you're interested, you can give it a read!

---
## Day 4: Wrapping Up My Jekyll Week

On my last day this week, I worked on my personal Jekyll project and completed my article about static and dynamic sites. It was a straightforward day. Since I'm new to Jekyll, I rely a lot on its documentation. I find Jekyll to be a cool technology, and I'm surprised I hadn't heard about it until our mentor introduced it to us.

Jekyll is a great tool for making static sites, and what's even better is that you can host them for free. That's what I'm planning to do—create a Jekyll project where I can share my articles, showcase personal projects, and maybe even have an 'about me' page for visitors to get to know me.

What I appreciate about Jekyll is its use of layouts and components, similar to Laravel blade templating. These are stored in our `_layouts` and `_includes` directory. This feature allows us to avoid repeating common code, like a navigation bar, a footer, and a layout. Instead, we create these elements once and easily insert them into our pages, making the whole process more efficient and organized, just like in Laravel.

As the week ended, I worked on my Jekyll project, realizing its simplicity and the cool way it organizes things with layouts and components. It's like arranging building blocks for your website. I'm excited about creating my site and sharing articles, projects, and an 'about me' page. This week taught me a lot and got me thinking creatively about future projects!