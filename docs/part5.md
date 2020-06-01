---
title: "Part 5 - Software Architecture"
permalink: /part5/
nav_order: 5
published: true
---


# Software Architecture

As the name suggests, *software architecture* is the fundamental structure and planning of a software. Regardless of the software, they are always comprised of different parts and elements, which have relations between each other.

You can compare software architecture to real life building architecture, and you won't be far off: To create something we must first design it, and create the blueprints. Software architecture is thus a central idea of software design.

There are several levels to software architecture, and in this part we will be looking at a few of them. We shall also examine some architecture styles and patterns of interest.

## Why Software Architecture?

The idea and reason behind software architecture is to have the fundamentals in place, before we start implementing our software. With proper architecture, we can make better...

* Structural options
  * It is different to architect a space shuttle, than it is a mobile app
* Stakeholder communication
  * Good architectural model can i.e. help the customer understand what is created
* Cost estimation, and especially reduction
  * Understanding arhcitecture helps understand where to implement the software
* Risk management
  * "Well designed is halfway done"

## How Software Architecture?

Just like any design, software architecture is a process, which has been refined over the years. At the moment, we could say there are four major steps in architecture design:

* **Architecture Analysis**

The first part of the process helps uis understand the environment of the software we are designing. This includes planning of non-functional requirements, such as reliability, efficiency, security, but also functional requirements, or the planning of the actual software structure.

* **Architecture Synthesis**

The first step of actual creation. After our analysis, we will start to create our software. It will begin as a small version in the beginning, possibly even just being a structure in the environment.

* **Architecture Evaluation**

As we continue our development, we also have to continue our architectural work. We have to keep evaluating the software at its current state, and how well it fits the requirements created at the original analysis. If our analysis was done well, at this point we can notice if we are missing something, or if we have indeed completed some parts of our software already.

* **Architecture Evolution**

Not to be mixed with the previous part. When evaluating, we examine the software, but with evolution, we examine the architecture model we have. Does it still answer our original problem? What if the customer wants new features, what does that do to the architecture?

## Architectural Patterns

Just like design patterns, *architectural patterns* are reusable, general solutions to common problems. The patterns are used to solve issues such as computer hardware limitations (*how much memory can we use?*), availability (*how often can we close our system for maintenance, for example?*) and what do we do with our data (*what kind of database and where?*).

Let's look at some of the most interesting architectural styles and patterns:
[**https://en.wikipedia.org/wiki/Software_architecture#Architectural_styles_and_patterns**](https://en.wikipedia.org/wiki/Software_architecture#Architectural_styles_and_patterns) and another listing here: [**https://en.wikipedia.org/wiki/List_of_software_architecture_styles_and_patterns**](https://en.wikipedia.org/wiki/List_of_software_architecture_styles_and_patterns). After you've had enough, return to this site.

Look into (at least):
* Monolithic application
* Layered application
* Event-driven
* Client-server
* Peer-to-Peer
* REST
* Cloud computing patterns

As you might have noticed, there are quite a few similarities between *architecture patterns* with *design patterns*. We can actually compare them with this handy chart: [**https://en.wikipedia.org/wiki/Architectural_pattern#Examples**](https://en.wikipedia.org/wiki/Architectural_pattern#Examples). Once again, return here once you're done.

## Architecture Erosion and Recovery

Not always everything goes as planned, and there is a noticeable difference between the architecture created at the analysis, and the software we have actually implemented. This difference is called *erosion*. The erosion can be caused by not following our architecture to the point, changes in the customer requirements but not doing the architectural evolution, and so on.

To fix our erosion, we have to use *architecture recovery*. This recovery is often done with *reverse engineering*, or examining the software to reconstruct the architecture it has, rather than relying on the one we have documented.

## Architecture Design Documents

When we create architecture designs, we usually start with a very rough scetch, for example to a white board in a meeting with a customer. From that, we develop the next step and start creating the actual architectural documentation. But what kind of documents do we want to produce?

As usual, there is several ways of creating the documentation. One way is to do it with charts, which explain for example the relations (such as ER diagrams) and data flow (flow charts or database charts). On the other hand, we could create lengthy written documentation, covering all the details, entities and their relations... Diagrams start to sound almost interesting at this point.

All the diagrams we have done so far, have been leading us to architecture: With the diagrams, we can do all the steps required for software architecture, from the analysis to the very end, when we have evaluated and evolved our documentation to match the software, and vice versa.

## Tools of the trade

There are several tools on how to create architecture diagrams. Most of them are not free of charge, but you can also use the familiar tools:

* [**Draw.io**](https://draw.io) is a all-around drawing tool, where you can create multiple different kinds of diagrams. It might take a while to learn how to get everything point in the correct direction, but once mastered, an uncanny tool for documentation. It has built-in specifics for some environments, such as Amazon Web Services (AWS), so building architecture diagrams is quite easy. 

* If you are already more familiar with other tools, of prefer for example [**LucidChart**](https://lucidchart.com/), you are more than welcome to use your tools of choice.

[**You can find the exercises here**](
https://centria.github.io/design-and-documentation/exercises/#part-5)