---
title: "Exercises"
permalink: /exercises/
nav_order: 7
published: true
---

# Exercises

## Part 1

* Return these exercises as an email, by 28.4.2020 at 23:59:59. Create **one** PDF (or docs or something, preferably pdf), where you have all the answers. **ONLY ONE FILE IS ACCEPTED AS RETURN!**

* In the end, you should have **one document**, with **five diagrams**/pictures.

* You can use any of the tools mentioned in the material.

### Exercise 1

* Draw a class diagram that represents the following code, and save it in your return document:

```cs
public class Person
{
  private string name;
  private int age;

  public Person(string initialName) {
    this.age = 0;
    this.name =  initialName;
  }
}
```

### Exercise 2

* Draw a class diagram that represents the following code, and save it in your return document, *as another picture*:

```cs
public class Person
{
  private string name;
  private int age;

  public Person(string initialName)
  {
    this.age = 0;
    this.name = initialName;
  }

  public void PrintPerson()
  {
    Console.WriteLine(this.name + ", age " + this.age + " years");
  }

  public void GrowOlder()
  {
    this.age = this.age + 1;
  }
}
```

### Exercise 3

* Draw a class diagram that represents the following code, and save it in your return document, *as another picture*:

```cs
public class ClockHand
{
  public int value { get; set; }
  public int limit { get; set; }

  public ClockHand(int limit)
  {
    this.limit = limit;
    this.value = 0;
  }

  public void Advance()
  {
    this.value = this.value + 1;

    if (this.value >= this.limit)
    {
      this.value = 0;
    }
  }

  public override string ToString()
  {
    if (this.value < 10)
    {
      return "0" + this.value;
    }

    return "" + this.value;
  }
}
```

### Exercise 4

* Draw a class diagram that represents the following code, and save it in your return document, *as another picture*.

**NOTICE!** This class has relation to ClockHand. In your diagram, also include the diagram for ClockHand, and their relation!

```cs
public class Clock
{
  private ClockHand hours;
  private ClockHand minutes;
  private ClockHand seconds;

  public Clock()
  {
    this.hours = new ClockHand(24);
    this.minutes = new ClockHand(60);
    this.seconds = new ClockHand(60);
  }

  public void Advance()
  {
    this.seconds.Advance();

    if (this.seconds.value == 0)
    {
      this.minutes.Advance();

      if (this.minutes.value == 0)
      {
        this.hours.Advance();
      }
    }
  }

  public override string ToString()
  {
    return hours + ":" + minutes + ":" + seconds;
  }
}
```

### Exercise 5

* Draw a class diagram that represents the following code, with relations, and save it in your return document, *as another picture*.

```cs
public interface IStorable
{
  double Weight();
}
```

```cs
public class CD : IStorable
{
  public string artist;
  public string name;
  public double weight;
  public int year;
  public CD(string artist, string name, int year)
  {
    this.artist = artist;
    this.name = name;
    this.weight = 0.1;
    this.year = year;
  }

  public double Weight()
  {
    return this.weight;
  }

  public override string ToString()
  {
    return this.artist + " - " + this.name + " (" + this.year + ")";
  }
}
```

```cs
public class Book : IStorable
{
  public string author;
  public string name;
  public double weight;
  public Book(string author, string name, double weight)
  {
    this.author = author;
    this.name = name;
    this.weight = weight;
  }

  public double Weight()
  {
    return this.weight;
  }

  public override string ToString()
  {
    return this.author + ": " + this.name;
  }
}
```

```cs
public class ChocolateBar : IStorable
{
  // Because C#'s automatically generated default constructor is enough,
  // we don't need a constructor

  public double Weight()
  {
    return 0.2;
  }

  public override string ToString()
  {
    return "Candybar, weight: " + Weight();
  }
}
```


```cs
public class Factory
{
  public IStorable ProduceNew()
  {
    Random ticket = new Random();
    // increase the range by one
    int number = ticket.Next(0, 5);

    if (number == 0)
    {
      return new CD("Pink Floyd", "Dark Side of the Moon", 1973);
    }
    else if (number == 1)
    {
      return new CD("Wigwam", "Nuclear Nightclub", 1975);
    }
    else if (number == 2)
    {
      return new Book("Robert Martin", "Clean Code", 1);
    }
    else if (number == 3)
    {
      return new Book("Kent Beck", "Test Driven Development", 0.7);
    }
    else
    {
      return new ChocolateBar();
    }
  }
}
```

```cs
public class Packer
{
  private Factory factory;

  public Packer()
  {
    this.factory = new Factory();
  }

  public List<IStorable> GiveAListOfThings()
  {
    List<IStorable> list = new List<IStorable>();

    int i = 0;
    while (i < 10)
    {
      IStorable newThing = factory.ProduceNew();
      list.add(newThing);

      i = i + 1;
    }

    return list;
  }
}
```

## Part 2

* Return these exercises as an email, by 5.5.2020 at 23:59:59. Create **one** PDF (or docs or something, preferably pdf), where you have all the answers. **ONLY ONE FILE IS ACCEPTED AS RETURN!**

* In the end, you should have **one document** with **four diagrams**.

* You can create ER diagrams with for example [**https://erdplus.com/standalone**](https://erdplus.com/standalone).

* You can create Sequence diagrams with for example [**https://sequencediagram.org/**](https://sequencediagram.org/).

* You can create Sequence diagrams with for example [**https://draw.io**](https://draw.io)

* If you feel more comfortable with other tools, you are welcome to use those as well, these are only examples.

### Exercise 1

Draw an ER diagram for the following class:

```cs
public class Person
{
  private string name;
  private int age;

  public Person(string initialName)
  {
    this.age = 0;
    this.name = initialName;
  }

  public void PrintPerson()
  {
    Console.WriteLine(this.name + ", age " + this.age + " years");
  }

  public void GrowOlder()
  {
    this.age = this.age + 1;
  }
}
```


### Exercise 2

Create an ER diagram for the following classes: 

```cs
public class ClockHand
{
  public int value { get; set; }
  public int limit { get; set; }

  public ClockHand(int limit)
  {
    this.limit = limit;
    this.value = 0;
  }

  public void Advance()
  {
    this.value = this.value + 1;

    if (this.value >= this.limit)
    {
      this.value = 0;
    }
  }

  public override string ToString()
  {
    if (this.value < 10)
    {
      return "0" + this.value;
    }

    return "" + this.value;
  }
}
```

```cs
public class Clock
{
  private ClockHand hours;
  private ClockHand minutes;
  private ClockHand seconds;

  public Clock()
  {
    this.hours = new ClockHand(24);
    this.minutes = new ClockHand(60);
    this.seconds = new ClockHand(60);
  }

  public void Advance()
  {
    this.seconds.Advance();

    if (this.seconds.value == 0)
    {
      this.minutes.Advance();

      if (this.minutes.value == 0)
      {
        this.hours.Advance();
      }
    }
  }

  public override string ToString()
  {
    return hours + ":" + minutes + ":" + seconds;
  }
}
```

Remember to put in the relation!

### Exercise 3

Consider the **Clock** and **ClockHand** above. Using this Main:

```cs
static void Main(string[] args)
{
  Clock clock = new Clock();

  while (true)
  {
    Console.WriteLine(clock);
    clock.Advance();
  }
}
```

Create a sequence diagram.

NOTICE! This will create an endless loop, so your loop does not have a break point.

### Exercise 4

Consider the following code:

```cs
using System;

public class Account 
{
  public double balance { get; set; }
  private string owner;

  public Account(string owner, double balance) 
  {
      this.balance = balance;
      this.owner = owner;
  }

  public void Deposit(double amount) 
  {
      this.balance = this.balance + amount;
  }

  public void Withdrawal(double amount) 
  {
      this.balance = this.balance - amount;
  }

  public override string ToString()
  {
    return this.owner + " balance: " + this.balance;
  }
}
```

Code in the Main:

```cs
using System;

class Program
{
  public static void Main(string[] args)
  {
    Account heikkisAccount = new Account("Heikki's account", 100.00);
    Account heikkisSwissAccount = new Account("Heikki's account in Switzerland", 1000000.00);

    Console.WriteLine("Intial state");
    Console.WriteLine(heikkisAccount);
    Console.WriteLine(heikkisSwissAccount);

    heikkisAccount.Withdrawal(20);
    Console.WriteLine("The balance of Heikki's account is now: " + heikkisAccount.balance);
    heikkisSwissAccount.Deposit(200);
    Console.WriteLine("The balance of Heikki's other account is now: " + heikkisSwissAccount.balance);

    Console.WriteLine("End state");
    Console.WriteLine(heikkisAccount);
    Console.WriteLine(heikkisSwissAccount);
  }
}
```

Draw a sequence diagram of what happens in the main.