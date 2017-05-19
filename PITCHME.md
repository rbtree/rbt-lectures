#HSLIDE

## Software Design Patterns
#### Bojan Radovanovic

---

### Design Patterns are...

In software engineering, a software design pattern is a **general reusable solution to a commonly occurring problem** within a given context in software design. (Wikipedia)

---

### Design Patterns are...

It is a **description or template for how to solve a problem** that can be used in many different situations. Design patterns are **formalized best practices** that the programmer can use to solve common problems when designing an application or system. (Wikipedia)

---

### Design Patterns are not...

It is not a **finished design** that can be transformed directly into source or machine code. (Wikipedia)

---

### History of Design Patterns

Patterns originated as an **architectural concept** by [Christopher Alexander](https://en.wikipedia.org/wiki/Christopher_Alexander) (1977/79) - architect and author of [A Pattern Language: Towns, Buildings, Construction](https://en.wikipedia.org/wiki/A_Pattern_Language). (Wikipedia)

![Christopher Alexander](https://qph.ec.quoracdn.net/main-qimg-67fdf1509c381971a4c1816dfdfaf251.webp =250x)

---

### History of Design Patterns

In 1987, [Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck) and [Ward Cunningham](https://en.wikipedia.org/wiki/Ward_Cunningham) began experimenting with the idea of applying patterns to programming – specifically pattern languages – and presented their results at the [OOPSLA](https://en.wikipedia.org/wiki/OOPSLA) conference that year. (Wikipedia)

---

### Gang of Four (GoF)

Design patterns gained popularity in computer science after the book [Design Patterns: Elements of Reusable Object-Oriented Software](https://en.wikipedia.org/wiki/Design_Patterns_(book)) was published in 1994 by the so-called "Gang of Four" (Gamma et al.), which is frequently abbreviated as "GoF". (Wikipedia)

![GoF](https://qph.ec.quoracdn.net/main-qimg-31cfec54edf396a5f0f526e823edb2e7.webp)

---

### Benefits of Design Patterns

First, they provide you with a **way to solve issues** related to software development using a **proven solution**. The solution facilitates the development of highly cohesive modules with minimal coupling. They **isolate the variability** that may exist in the system requirements, making the overall system **easier to understand and maintain**. (developer.com)

+++

### Benefits of Design Patterns

Second, design patterns make **communication between designers more efficient**. Software professionals can immediately picture the high-level design in their heads when they refer the name of the pattern used to solve a particular issue when discussing system design. (developer.com)

---

### Classification

There are three basic kinds of design patterns:
* **Creational**
* **Structural**
* **Behavioral**

---

### Creational Design Patterns

Creational patterns **provide instantiation mechanisms**, making it easier to create objects in a way that suits the situation.

+++

### Creational Design Patterns

* **Abstract Factory** - Creates an instance of several families of classes
* **Builder** - Separates object construction from its representation
* **Factory Method** - Creates an instance of several derived classes

+++

### Creational Design Patterns

* **Object Pool** - Avoid expensive acquisition and release of resources by recycling objects that are no longer in use
* **Prototype** - A fully initialized instance to be copied or cloned
* **Singleton** - A class of which only a single instance can exist

---

### Structural Design Patterns

Structural patterns generally **deal with relationships between entities**, making it easier for these entities to work together.

+++

### Structural Design Patterns

* **Adapter** - Match interfaces of different classes
* **Bridge** - Separates an object’s interface from its implementation
* **Composite** - A tree structure of simple and composite objects
* **Decorator** - Add responsibilities to objects dynamically

+++

### Structural Design Patterns

* **Facade** - A single class that represents an entire subsystem
* **Flyweight** - A fine-grained instance used for efficient sharing
* **Private Class Data** - Restricts accessor/mutator access
* **Proxy** - An object representing another object

---

### Behavioral Design Patterns

Behavioral patterns are **used in communications between entities** and make it easier and more flexible for these entities to communicate.

+++

### Behavioral Design Patterns

* **Chain of responsibility** - A way of passing a request between a chain of objects
* **Command** - Encapsulate a command request as an object
* **Interpreter** - A way to include language elements in a program
* **Iterator** - Sequentially access the elements of a collection

+++

### Behavioral Design Patterns

* **Mediator** - Defines simplified communication between classes
* **Memento** - Capture and restore an object's internal state
* **Null Object** - Designed to act as a default value of an object
* **Observer** - A way of notifying change to a number of classes

+++

### Behavioral Design Patterns

* **State** - Alter an object's behavior when its state changes
* **Strategy** - Encapsulates an algorithm inside a class
* **Template method** - Defer the exact steps of an algorithm to a subclass
* **Visitor** - Defines a new operation to a class without change