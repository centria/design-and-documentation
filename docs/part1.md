---
title: "Part 1 - Class Diagrams"
permalink: /part1/
nav_order: 1
published: true
---

# Class Diagrams

A class diagram is a diagram used in designing and modeling software to describe classes and their relationships. Class diagrams enable us to model software in high level of abstraction and without having to look at the source code.

Classes in a class diagram correspond with classes in the source code. The diagram shows the names and attributes of the classes, connections between the classes and sometimes also the methods of the classes.

Next we will get familiar with creating and reading class diagrams using [**UML**](https://en.wikipedia.org/wiki/Unified_Modeling_Language). Using an unified modeling language ensures that class diagrams drawn by different people can be read and understood by everyone familiar with the language.

## Describing class and class attributes

First we will describe one class and its attributes. Below is the source code for a class called Person which has two class attributes name and age.

```cs
public class Person {
    private string name;
    private int age;
}
```