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

In a class diagram a class is represented by a rectangle with the name of the class written on top. A line below the name of the class divides the name from the list of attributes (names and types of the class variables). The attributes are written one attribute per line.

In a class diagram, class attributes are written "attributeName: attributeType". + before the attribute name means the attribute is public, and - the attribute is private.

![Person with name and age](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/classdiagram-person-name-age.png)

## Describing class constructor

Below we have the source code for a constructor for our Person class. The constructor gets the name of the person as a parameter.

```cs
public class Person {
  private string name;
  private int age;

  public Person(string initialName) {
      this.name = initialName;
      this.age = 0;
  }
}
```

![Person with name, age and constructor](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/classdiagram-person-name-age-constructor.png)
