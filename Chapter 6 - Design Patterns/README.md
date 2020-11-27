# Design Pattern

Now the stage is set and we are ready for big leap. We have quality Objects and Perfect guidelines to implement it. We started building maintainable code with next generation programming language, but re-usability is still a concern and every time we end up re-inventing the wheel.

With Object Oriented design principle in hand, their implementation is big thing. Proper implementation will provide us with maintainable and re-usable code.

Known principles are :

* Encapsulate what varies.
* Favor Object Composition over Class Inheritance.
* Program to Interface, not to implementation.
* Depend on Abstraction, do not depend on concrete class.
* Strive for loosely coupled design between object that interact.

# How to implement Object Oriented design principles?

In the 1994 a mile stone book came in software engineering, it was called Design Pattern and it was work of four authors, later known as Gang of Four.

> Design Patterns: Elements of Reusable Object-Oriented Software (1994) is a software engineering book describing software design patterns. The book was written by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides, with a foreword by Grady Booch. The book is divided into two parts, with the first two chapters exploring the capabilities and pitfalls of object-oriented programming, and the remaining chapters describing 23 classic software design patterns.
>                                                                            - Wikipedia

23 Patterns where identified and categorized, these were general Repeatable/ Proven solution to a commonly occurring problem in software design. Design patterns are classified into three main category based on the type of probelm they solve.

Original GoF Categorization

>  Creational - process of creation of Objects from classes
>  Structural - process of arranging or composing Objects and Classes
>  Behavioral - process of communication/ interaction between Objects

## Creational
Creational design patterns are design patterns that deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

## Structural
Structural design patterns are design patterns that ease the design by identifying a simple way to realize relationships among entities.

## Behavioral
Behavioral patterns are concerned with the assignment of responsibilities between objects, or, encapsulating behavior in an object and delegating requests to it

## The Catalog of Design Patterns

Singleton - Ensure a class only has one instance, and provide a global point of access to it.

Observer - Defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and updated automatically

Abstract Factory - Provide an interface for creating families of related or dependent objects without specifying their concrete classes.

Decorator Pattern - Attaches additional responsibilities to an object dynamically. Decorator provides a flexible alternative to sub-classing for extending functionality.

Factory Method Pattern - Defines an interface for creating an object, but lets sub classes decide which class to instantiate. It lets a class defer instantiation to subclass

Command - Encapsulate a request as an object, thereby letting you parameterize clients with different requests, queue or log requests, and support undoable operations.

> Thinks to Think on: </br>
> Now that we have learned about the rules and guidelines, what about reponsibilities?

# GRASP
General Responsibility Assignment Software Patterns, abbreviated GRASP, consist of guidelines for assigning responsibility to classes and objects in object-oriented design. 

Responsibility - A contract or obligation that a class/ module/ component must accomplish.

## Expert 
Given a resposibility, What a `class` must accomplish?
## Creator
Who must istantiate a `object`?
## Low Cohesion
How to minimize dependencies between `class`'s?
## High Cohesion
How to design cohisive `class`?
## Controller
Given a event layer (UI) and a business layer, Who has the responsibility of recieve the request from the UI layer?
## Polymorphism
How to act differently depending on object class?
## Pure Fabrication
How to assign responsibility, if applying the expert principle decreases cohesion and increase coupling?
## Indirection
How to assign responsibility in order to remove coupling between two component?
## Controller Variation
How to design in such a way that changes on classes, modules and systems doesn't effect dependent components?


Once you get hold on these Design Patterns, you are ready to solve mysteries and go beyond. Ultimately, solution is also an Object which has a meaning now .....
