---
layout: post
title: "Docker - Introduction"
author: nsagnoy
categories: [ Docker ]
---


In this article, we will tackle the basic concepts, terminologies and tools of docker and how relevant it is to use Docker in software development.

----

Docker is a tool/technology that allows developers to build, test and deploy their applications quickly. With docker, it is possible to run interconnected applications simultaneously and contain them in an isolated environment. It utilizes the concept of **"Containerization"** which is an improved concept of **"Virtualization"** wherein the operating system layer is removed. Allowing applications to run independently from the host operating system and also preventing resource waste.

## Terminologies and/or Tools

- **Docker image** - is an executable file which contains a set of instructions on how a container is built (like a template).
- **Docker container** - is a running instance of a docker image.
- **Dockerfile** - is a text document that serves as a blueprint in building/creating docker images.
- **Docker compose** - is a tool used to contain and run multiple instances of docker images along with its configuration. With this, we won't have to perform "docker run" one by one.
- **Docker run** -