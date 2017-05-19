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

<img src="https://qph.ec.quoracdn.net/main-qimg-67fdf1509c381971a4c1816dfdfaf251.webp" alt="Christopher Alexander" width="300">

---

### History of Design Patterns

In 1987, [Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck) and [Ward Cunningham](https://en.wikipedia.org/wiki/Ward_Cunningham) began experimenting with the idea of applying patterns to programming – specifically pattern languages – and presented their results at the [OOPSLA](https://en.wikipedia.org/wiki/OOPSLA) conference that year. (Wikipedia)

---

### Gang of Four (GoF)

Design patterns gained popularity in computer science after the book [Design Patterns: Elements of Reusable Object-Oriented Software](https://en.wikipedia.org/wiki/Design_Patterns_(book)) was published in 1994 by the so-called "Gang of Four" (Gamma et al.), which is frequently abbreviated as "GoF". (Wikipedia)

<img src="https://qph.ec.quoracdn.net/main-qimg-31cfec54edf396a5f0f526e823edb2e7.webp" alt="GoF" width="400">

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

---

### Abstract Factory Design Pattern

#### Definition

Provide an interface for creating families of related or dependent objects without specifying their concrete classes.

+++

### Abstract Factory Design Pattern

#### UML class diagram

![Abstract Factory - UML class diagram](http://www.dofactory.com/images/diagrams/net/abstract.gif)

+++

### Abstract Factory Design Pattern

#### Participants

* **AbstractFactory  (ContinentFactory)** - declares an interface for operations that create abstract products
* **ConcreteFactory   (AfricaFactory, AmericaFactory)** - implements the operations to create concrete product objects
* **AbstractProduct   (Herbivore, Carnivore)** - declares an interface for a type of product object
+++

### Abstract Factory Design Pattern

#### Participants

* **Product  (Wildebeest, Lion, Bison, Wolf)** - defines a product object to be created by the corresponding concrete factory; implements the AbstractProduct interface
* **Client  (AnimalWorld)** - uses interfaces declared by AbstractFactory and AbstractProduct classes

+++

### Abstract Factory Design Pattern

#### Example

This pattern is found in the sheet metal stamping equipment used in the manufacture of Japanese automobiles. The stamping equipment is an Abstract Factory which creates auto body parts. The same machinery is used to stamp right hand doors, left hand doors, right front fenders, left front fenders, hoods, etc. for different models of cars. Through the use of rollers to change the stamping dies, the concrete classes produced by the machinery can be changed within three minutes.

+++

### Abstract Factory Design Pattern

#### Example

![Abstract Factory - Example](https://sourcemaking.com/files/v2/content/patterns/Abstract_Factory_example1.svg)

---

### Builder Design Pattern

#### Definition

Separate the construction of a complex object from its representation so that the same construction process can create different representations.

+++

### Builder Design Pattern

#### UML class diagram

![Builder - UML class diagram](http://www.dofactory.com/images/diagrams/net/builder.gif)

+++

### Builder Design Pattern

#### Participants

* **Builder  (VehicleBuilder)** - specifies an abstract interface for creating parts of a Product object
* **ConcreteBuilder  (MotorCycleBuilder, CarBuilder, ScooterBuilder)** - constructs and assembles parts of the product by implementing the Builder interface; defines and keeps track of the representation it creates; provides an interface for retrieving the product

+++

### Builder Design Pattern

#### Participants

* **Director  (Shop)** - constructs an object using the Builder interface
* **Product  (Vehicle)** - represents the complex object under construction. ConcreteBuilder builds the product's internal representation and defines the process by which it's assembled; includes classes that define the constituent parts, including interfaces for assembling the parts into the final result

+++

### Builder Design Pattern

#### Example

This pattern is used by fast food restaurants to construct children's meals. Children's meals typically consist of a main item, a side item, a drink, and a toy (e.g., a hamburger, fries, Coke, and toy dinosaur). Note that there can be variation in the content of the children's meal, but the construction process is the same. Whether a customer orders a hamburger, cheeseburger, or chicken, the process is the same. The employee at the counter directs the crew to assemble a main item, side item, and toy. These items are then placed in a bag. The drink is placed in a cup and remains outside of the bag. This same process is used at competing restaurants.

+++

### Builder Design Pattern

#### Example

![Builder - Example](https://sourcemaking.com/files/v2/content/patterns/Builder_example1.svg)

---

### Factory Method Design Pattern

#### Definition

Define an interface for creating an object, but let subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses.

+++

### Factory Method Design Pattern

#### UML class diagram

![Factory Method - UML class diagram](http://www.dofactory.com/images/diagrams/net/factory.gif)

+++

### Factory Method Design Pattern

#### Participants

* **Product  (Page)** - defines the interface of objects the factory method creates
* **ConcreteProduct  (SkillsPage, EducationPage, ExperiencePage)** - implements the Product interface

+++

### Factory Method Design Pattern

#### Participants

* **Creator  (Document)** - declares the factory method, which returns an object of type Product. Creator may also define a default implementation of the factory method that returns a default ConcreteProduct object; may call the factory method to create a Product object
* **ConcreteCreator  (Report, Resume)** - overrides the factory method to return an instance of a ConcreteProduct

+++

### Factory Method Design Pattern

#### Example

Manufacturers of plastic toys process plastic molding powder, and inject the plastic into molds of the desired shapes. The class of toy (car, action figure, etc.) is determined by the mold.

+++

### Factory Method Design Pattern

#### Example

![Factory Method - Example](https://sourcemaking.com/files/v2/content/patterns/Factory_Method_example1.svg)

---

### Prototype Design Pattern

#### Definition

Specify the kind of objects to create using a prototypical instance, and create new objects by copying this prototype.

+++

### Prototype Design Pattern

#### UML class diagram

![Prototype - UML class diagram](http://www.dofactory.com/images/diagrams/net/prototype.gif)

+++

### Prototype Design Pattern

#### Participants

* **Prototype  (ColorPrototype)** - declares an interface for cloning itself
* **ConcretePrototype  (Color)** - implements an operation for cloning itself
* **Client  (ColorManager)** - creates a new object by asking a prototype to clone itself

+++

### Prototype Design Pattern

#### Example

The mitotic division of a cell - resulting in two identical cells - is an example of a prototype that plays an active role in copying itself and thus, demonstrates the Prototype pattern. When a cell splits, two cells of identical genotype result. In other words, the cell clones itself.

+++

### Prototype Design Pattern

#### Example

![Prototype - Example](https://sourcemaking.com/files/v2/content/patterns/Prototype_example1.svg)

---

### Singleton Design Pattern

#### Definition

Ensure a class has only one instance and provide a global point of access to it.

+++

### Singleton Design Pattern

#### UML class diagram

![Singleton - UML class diagram](http://www.dofactory.com/images/diagrams/net/singleton.gif)

+++

### Singleton Design Pattern

#### Participants

* **Singleton   (LoadBalancer)** - defines an Instance operation that lets clients access its unique instance. Instance is a class operation; responsible for creating and maintaining its own unique instance

+++

### Singleton Design Pattern

#### Example

The office of the President of the United States is a Singleton. The United States Constitution specifies the means by which a president is elected, limits the term of office, and defines the order of succession. As a result, there can be at most one active president at any given time. Regardless of the personal identity of the active president, the title, "The President of the United States" is a global point of access that identifies the person in the office.

+++

### Singleton Design Pattern

#### Example

![Singleton - Example](https://sourcemaking.com/files/v2/content/patterns/Singleton_example1.svg)