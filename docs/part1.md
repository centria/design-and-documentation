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

First we will describe one class and its attributes. Below is the source code for a class called **Person** which has two class attributes name and age.

```cs
public class Person 
{
  private string name;
  private int age;
}
```

In a class diagram a class is represented by a rectangle with the name of the class written on top. A line below the name of the class divides the name from the list of attributes (names and types of the class variables). The attributes are written one attribute per line.

In a class diagram, class attributes are written *"attributeName: attributeType".* **+ before the attribute name means the attribute is public, and - the attribute is private.**

![Person with name and age](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/classdiagram-person-name-age.png)

## Describing class constructor

Below we have the source code for a constructor for our Person class. The constructor gets the name of the person as a parameter.

```cs
public class Person 
{
  private string name;
  private int age;

  public Person(string initialName) 
  {
    this.name = initialName;
    this.age = 0;
  }
}
```

In a class diagram we list the constructor (and all other methods) below the attributes. A line below the attributes list separates it from the method list. Methods are written +/- (debending on the visibility of the method), method name, parameters and their types. The constructor above is written **+Person(initialName:string)**

The parameters are written the same way class attributes were, *"parameterName: parameterType"*.

![Person with name, age and constructor](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/classdiagram-person-name-age-constructor.png)

## Describing class methods

Below we have added a method **PrintPerson()** which returns void to the Person class.

```cs
public class Person 
{
  private string name;
  private int age;

  public Person(string initialName) 
  {
    this.name = initialName;
    this.age = 0;
  }

  public void PrintPerson() 
  {
    Console.WriteLine(this.name + ", age " +   this.age + " years");
  }
}
```

In a class diagram we list all class methods with the constructors -- constructors are listed first and then all class methods. We also write the return type of a method to the class diagram.

![Person with name, age, constructor and print](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/classdiagram-person-name-age-constructor-print.png)

A class diagram describes classes and their attributes, constructors and methods as well as the connections between classes. However a class diagram tells us nothing about the implementation of the constructors or the methods. Therefore a class diagram describes the structure of an object but not its functionality.

For example the method PrintPerson uses the class attributes name and age, but this cannot be seen from the class diagram.

## Connections between classes

In a class diagram, the connections between classes are shown as arrows. The arrows also show the direction of the connection.

Below we have a class Book.

```cs
public class Book 
{
  private string name;
  private string publisher;

  // constructors and methods
}
```

![Book](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/classdiagram-book-name-and-publisher.png)

If we add a variable author, type of which is Person, in the source code the variable is declared like all other class variables.

```cs
public class Book 
{
  private string name;
  private string publisher;
  private Person author;

  // constructors and methods
}
```

In a class diagram variables which refer to other objects are not written with the rest of the class attributes, but are shown as connections between the classes. In the class diagram below we have the classes Person and Book, and the connection between them.

![Book](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/class-diagram-book-person-relation.png)

Class methods are described just like we did before. Below we have added methods **GetAuthors** and **AddAuthor** to the Book class.

```cs
public class Book 
{
  private string name;
  private string publisher;
  private List<Person> authors;

  // constructor would be here


  public List<Person> GetAuthors() 
  {
      return this.authors;
  }

  public void AddAuthor(Person author) 
  {
    this.authors.Add(author);
  }
}
```

![Book](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/book-with-many-authors.png)
