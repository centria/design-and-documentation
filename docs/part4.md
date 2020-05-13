---
title: "Part 4 - Software Design"
permalink: /part4/
nav_order: 4
published: true
---

# Software Design

*"Software design is the process by which an agent creates a specification of a software artifact, intended to accomplish goals, using a set of primitive components and subject to constraints. Software design may refer to either 'all the activity involved in conceptualizing, framing, implementing, commissioning, and ultimately modifying complex systems' or 'the activity following requirements specification and before programming, as in a stylized software engineering process.'*

*Software design usually involves problem solving and planning a software solution. This includes both a low-level component and algorithm design and a high-level, architecture design."* [**Wikipedia**](https://en.wikipedia.org/wiki/Software_design)

We shall concentrate most on the high-level architecure design on this course. Designing is quite similar to what we have done with our documentation part, except rather than having a software to draw our documentation from, we first do the design on documentation level, after which we implement the actual software.

In this part, we will have a look at a few key concepts of software design. The aspects of design are not by any means a comprehensive list, and design in itself is a whole part of our industry. It is crucial, however, that you understand at least some of the basics, as design is the driving force in proper software production.

## Design Process

Design process can be seen as a sequence of steps, where the designer describes all the aspects of the software. There is not a single process guideline which every designer could follow, but the end result should always be the same: a well designed software, which can be implemented as intended, based on said design.

Usually we begin our process with customer requirements, i.e. what is desired of the software. We can see this as the problem setting, and our first step.

* Analyze the problem.

Before we can start anything else for our design, we have to analyze, what is required of the final product. What are the key features of the software, what are the caveats, and so on. Let's follow an example product, let's say a simple webpage, like *Facebook*.

What is required of a *Facebook*? The customer could describe it as a social media platform, where people can connect with each other, message each other directly, tell each other stories on personal or other people's "walls", share pictures, have groups with each other, organize events, sell items... Ok, not really a simple webpage, but a good starting point for our problem.

We should start by taking the problem into small parts, what does the software consist of:
* Social media platform
* Ability to connect with other people
* Messaging application
* And so on, and so on.

All this should be well documented as part of our design. When we have all the components available, we can start the same process for each component. What is required from for example a *Messaging application*?

* Ability to log in (and out)
* Contact other people
  * Contact list?
* Send and receive messages
  * Write messages
* Etc, etc, etc.

After we have done this to all our components, we have a pretty clear idea, what the software should do.

## Design Principles

## Design Concepts

## Design Patterns


