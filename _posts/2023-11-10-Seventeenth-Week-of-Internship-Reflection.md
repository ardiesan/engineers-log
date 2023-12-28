---
layout: post
title: "Seventeenth Week of Internship: A Reflection"
author: mtrinidad
categories: 
- internship
image: assets/images/mtrinidad-week17.png
---
This week was a mix of learning about Laravel routing and grappling with design in my app. I got better insights into how Git can work across different repositories, and its decentralized nature allows for personal setups and syncing copies by fetching changes from others. In the world of Ruby, I explored gems, handy packages extending Ruby's capabilities, and tools like RubyGems and Bundler that simplify managing dependencies. Jekyll, a static site generator, caught my eye for creating websites and hosting via GitHub Pages.

---
## Laravel Routing and Design Struggles

First day of the week, I continued to work on my Laravel app and dedicated time to reading the Laravel documentation on routing. It was a valuable read, and I immediately put what I learned into practice by implementing grouped routes. I also made some changes to the app’s design. Designing isn’t my strongest suit, and it's a bit challenging for me. But I know that with time, I’ll get better at it. I tweaked the dark mode and light mode on my app, playing around with transition delays and colors. The day taught me that learning takes time, especially when it comes to things that aren't my forte, like design. But each small adjustment I make is a step toward improving and learning.

---
## Efficient Editing: Grammarly Integration in VSCode

This week, one task stood out. I hunted down grammar and spelling errors in my reflection entries. Initially, I thought doing this manually using a web tool like Grammarly would be quite time-consuming. However, I discovered a better way—I could install Grammarly as an extension directly in my VSCode. It didn’t work immediately, so I dived into the documentation. Turns out, I needed to tweak the configuration to enable checking of markdown files in a specific directory, and that did the trick!

---
## Toast UI Editor Integration

My mentor recommended a game-changing plugin for my Laravel app, a markdown editor called Toast UI Editor. Integrating it was fantastic. I did not know such a plugin existed. I'm grateful for my manager's suggestion. Now, my Laravel app has a cool markdown editor. To ensure the markdown appears beautifully on my website, I also installed Tailwind Typography for markdown rendering.

---
## Ruby Development Environment

### Ruby

Ruby is the programming language itself. It has a clean and elegant syntax, making it easy to read and write code. In a Ruby project, a gem is a package or library. Gems are similar to packages or libraries in other programming languages. We can use gems to extend the functionality of our Ruby applications. The Ruby community has a vast collection of gems available, which can be easily installed and managed using a package manager called "RubyGems". 

### RubyGems

RubyGems is a package manager for Ruby that allows us to install, manage, and distribute Ruby gems. We can use the `gem` command-line tool to interact with RubyGems. For example, we can install gems, list installed gems, and update them using this tool. It simplifies the process of adding third-party libraries and components to our Ruby projects.

### Bundler

Bundler is a tool used to manage project dependencies in Ruby applications. It ensures that our project uses the correct versions of gems and their dependencies. We define your gem dependencies in a `Gemfile` in our project directory, and Bundler takes care of installing the specified gem versions and their dependencies.

### Jekyll

Jekyll is a static site generator written in Ruby. It allows us to build websites by transforming plain text files (often written in Markdown) into static HTML pages. Jekyll is popular for creating blogs, documentation sites, and other content-based websites. It provides templates and themes to make site creation and maintenance easier. Jekyll and Bundler are gems, that can be installed using RubyGems.

### Hosting Jekyll

We can host our  Jekyll static website on GitHub Pages. GitHub Pages is powered by Jekyll so we can easily deploy our static site for free and with a custom domain name.

---
## The Distributed Nature of Git

Git is quite flexible, allowing commits to different repositories even if they don't share the same history. Using the `git config --local --list` command helps us to see the URL of the remote origin. Configuring the local copy to consider two remotes is a way to manage multiple sources. One of Git's distinctive features is its decentralization. This means that with tools like Ngrok, we can essentially become the Git server, empowering each of us to have our setups for committing. With decentralization, we can synchronize our copy by fetching changes from others' repositories. Decentralization in Git means that each person working on a project has a local copy of the entire project's history and can work independently without constantly needing to connect to a central server. They can make changes, commit them, and merge them with others' work locally before pushing those changes to a shared repository.

