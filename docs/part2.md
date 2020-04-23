---
title: "Part 2 - ER Models and Sequence Diagrams"
permalink: /part2/
nav_order: 2
published: true
---

# ER Diagrams

An **entity-relationship model** describes interralated items of interest in a specific domain. A basic ER model is composed of entity types and specifies relationships between those entities. In software engineering, the ER model can be used to describe for example business models, but also data models or software structures.

ER models are not part of the UML standard, but are still quite often used. They are used for example conceptualizing a software, before actually implementing said software. According to their name, the ER diagrams **DO NOT** describe the inner functions of entities, but merely the relations between them.

Let us use one of our previous class diagrams as an example, and change that into an ER diagram.

![Person with name and age](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/classdiagram-person-name-age.png)

Starting off small, let us have the class "Person" as an ER diagram.

![ER Person with name and age](https://github.com/centria/design-and-documentation/raw/master/assets/images/part2/er_person.png)

In our diagram, we have an **Entity** called **Person**, described with a rectungular shape. The Entity has two **Attributes**, described with elliptical shapes. The entity name, as well as the attributes, are written as **singular nouns**.

For a more complex example, let's use

![Book](https://github.com/centria/design-and-documentation/raw/master/assets/images/part1/class-diagram-book-person-relation.png)


![ER Person writes book](https://github.com/centria/design-and-documentation/raw/master/assets/images/part2/er_person_book.png)

Now we can see, that our "author" has changed to "writes". The relationship between the two is still the same, but in ER, the relationships are written as **verbs**. These are read from left to right, as in "Person writes a book".

Just like in class diagrams, ER diagrams can also used to describe cardinalities. Let's take our Book and Person, but now with more than one relationship:

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

As our book now has *0..N* (zero or more) authors, we want to indicate this in our ER, as well. To do this, there are multiple notations. We are now using [**Crow's foot notation**](https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model):


![ER Person writes book](https://github.com/centria/design-and-documentation/raw/master/assets/images/part2/er_persons_books.png)









You can create ER diagrams with for example [**https://erdplus.com/standalone**](https://erdplus.com/standalone).

# Sequence Diagrams

Here will be even more.

You can create Sequence diagrams with for example [**https://sequencediagram.org/**](https://sequencediagram.org/).