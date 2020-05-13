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

We shall be looking at this step as its own later in this course, as we will discuss software architecture, so let's not go deeper into this at the moment.

### Design the details.

Next step would be designing the details of the software. What kind of data structures do we need? How should our software function, or what kind of an user interface should it have? How is our data controlled, what are the security features?

All these questions should be answered, if possible, during the design process. As it is crucial for a programmer to understand the basics of design, it is equally important for the designer to understand the basics of programming. With knowledge of what is reasonable to implement (nothing is impossible, something might just require a lot of time and money), a good designer can create roadmap for the programmers, which to follow.

## Design Principles

Designing software has few quidelines, or *principles*, which most of the designs follow. These principles are not the universal truth, and there are multiple versions of these, but this is one list, which has been in use since 1990's and has evolved since. They were originated in this book: [201 principles of software development](https://dl.acm.org/doi/book/10.5555/203406) and are also listed here: [Wikipedia](https://en.wikipedia.org/wiki/Software_design#Overview)

* **The design process should not suffer from "tunnel vision."** A good designer should consider alternative approaches, judging each based on the requirements of the problem, the resources available to do the job.
* **The design should be traceable to the analysis model.** Because a single element of the design model can often be traced back to multiple requirements, it is necessary to have a means for tracking how requirements have been satisfied by the design model.

* **The design should not reinvent the wheel.** Systems are constructed using a set of design patterns, many of which have likely been encountered before. These patterns should always be chosen as an alternative to reinvention. Time is short and resources are limited; design time should be invested in representing (truly new) ideas by integrating patterns that already exist (when applicable).

* **The design should "minimize the intellectual distance" between the software and the problem as it exists in the real world.** That is, the structure of the software design should, whenever possible, mimic the structure of the problem domain.

* **The design should exhibit uniformity and integration.** A design is uniform if it appears fully coherent. In order to achieve this outcome, rules of style and format should be defined for a design team before design work begins. A design is integrated if care is taken in defining interfaces between design components.

* **The design should be structured to accommodate change.** The design concepts discussed in the next section enable a design to achieve this principle.

* **The design should be structured to degrade gently, even when aberrant data, events, or operating conditions are encountered.** Well-designed software should never "bomb"; it should be designed to accommodate unusual circumstances, and if it must terminate processing, it should do so in a graceful manner.

* **Design is not coding, coding is not design.** Even when detailed procedural designs are created for program components, the level of abstraction of the design model is higher than the source code. The only design decisions made at the coding level should address the small implementation details that enable the procedural design to be coded.

* **The design should be assessed for quality as it is being created, not after the fact.** A variety of design concepts and design measures are available to assist the designer in assessing quality throughout the development process.

* **The design should be reviewed to minimize conceptual (semantic) errors.** There is sometimes a tendency to focus on minutiae when the design is reviewed, missing the forest for the trees. A design team should ensure that major conceptual elements of the design (omissions, ambiguity, inconsistency) have been addressed before worrying about the syntax of the design model.


## Design Concepts

## Design Patterns


