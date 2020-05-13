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

We will look into the process and parts of software design, and what it can consist of, when talking about larger software products. In the simplest form, a software design can be a single chart, which describes the key components and their relations. In this part, how ever, we will be looking at a bit more complex software.

## Design Process

Design process can be seen as a sequence of steps, where the designer describes all the aspects of the software. There is not a single process guideline which every designer could follow, but the end result should always be the same: a well designed software, which can be implemented as intended, based on said design.

Usually we begin our process with customer requirements, i.e. what is desired of the software. We can see this as the problem setting, and our first step.

### Analyze the problem.

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

After we have done this to all our components, we have a pretty clear idea, what the software should do. After this, we can move on to our next step.

### Design the system interface.

In this step of the software design, we are looking at who is the software for? What platform should it run on? How should it be used? Let's look into these questions briefly.

* Who is the software for?

If we keep our *Facebook* example in mind, a short answer would be, "for everyone". But targeting a software for everyone is usually not an option, but we rather have to choose an angle. Originally, Facebook was targeted for Mark Zuckerberg's school and class mates. It evolved from this to be a platform for everyone. We as designers should also keep in mind our target demographic. 

A more suitable target audience could be, for example "individuals persons, who have regular access to internet". This narrows down our demographic by about 90% already, as internet is not as available everywhere, as it is in Finland, for example. Another demographic we ruled out was also "companies". Even though they are a target of *Facebook* as advertisers, the majority demographic is still individual people.

* What platform should it run on?

Nowadays answer to this is also usually "on every platform", as more and more applications are based on web pages, rather than being desktop solutions. Once again, "every platform" is too vague, but we need to narrow it down for our design specification. We are now designing still on system level, which means we have to take into consideration the differences between different types of systems.

"Mobile devices, such as Android and iOS devices" would be a good criteria for a mobile application, and "browsers, such as Chrome and Opera" could be another criteria. The difference is, how ever, that most probably the interface for these two criteria are completely different: It is quite different to write code to run on an Android phone, than to produce a web page.

* How should it be used?

On system level, this is an important question. For our example, design features such as "touchscreen compatible" are relevant. But let's go away from our Facebook for a while, and have a bit different view.

On average, a modern car has on estimate 25 to 50 different processing units, or "computers". All of these require software for the car to run smoothly. In this kind of a scenario, the interface becomes quite clear: The software for steering has to be able to handle the steering, and the interface for it is the steering components. At the same time, another software would be handling the headlights, for example.

It is crucial to understand, what kind of software we are designing, and where it is going to be used. If we blindly start creating software without proper documentation, that could end up into a disaster. From this, we get to our next step.

### Design the arcitecture.

Software architecture is the basic blueprint of all the software. It describes the different components of the software on high level, and their relation with each other. It is also used to detail the responsibilities and interactions between the components, and keep track of the interfaces they provide.

Let's get back to Facebook.

## Design Principles

## Design Concepts

## Design Patterns


