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

> Design Patterns: </br>
> Elements of Reusable Object-Oriented Software (1994) is a software engineering book describing software design patterns. The book was written by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides, with a foreword by Grady Booch. The book is divided into two parts, with the first two chapters exploring the capabilities and pitfalls of object-oriented programming, and the remaining chapters describing 23 classic software design patterns. </br>
>                                                           - Wikipedia

23 Patterns where identified and categorized, these were general Repeatable/ Proven solution to a commonly occurring problem in software design. Design patterns are classified into three main category based on the type of probelm they solve.

Original GoF Categorization

>  Creational - process of creation of Objects from classes </br>
>  Structural - process of arranging or composing Objects and Classes </br>
>  Behavioral - process of communication/ interaction between Objects </br>

## Creational
Creational design patterns are design patterns that deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

* Singleton - Ensure a class only has one instance, and provide a global point of access to it.

* Builder - The exercise of creating complex types can be simplified by piecewise object constuction made up of several sub-objects.

* Prototype - Create new objects from the 'skeleton' of an existing object, they reiterate the existing design and boosting performance.

* Abstract Factory - Provide an interface for creating families of related or dependent objects without specifying their concrete classes.

* Dependency Injection - A class accepts the objects, it requires from an injector instead of creating the objects directly.

* Object Pool - Avoid expensive acquisition and release of resources by recycling objects that are no longer in use. 

## Structural
Structural design patterns are design patterns that ease the design by identifying a simple way to realize relationships among entities.

* Module - Group several related elements, such as classes, singletons, methods, globally used, into a single conceptual entity.

* Facade - Provide a unified interface to a set of interfaces in a subsystem. Facade defines a higher-level interface that makes the subsystem easier to use.

* Bridge - Decouple an abstraction from its implementation allowing the two to vary independently.

* Adapter - Convert the interface of a class into another interface clients expect. An adapter lets classes work together that could not otherwise because of incompatible interfaces. The enterprise integration pattern equivalent is the translator.

## Behavioral
Behavioral patterns are concerned with the assignment of responsibilities between objects, or, encapsulating behavior in an object and delegating requests to it

* State - Allow an object to alter its behavior when its internal state changes. The object will appear to change its class.

* Observer (Publish/Subscribe) - Define a one-to-many dependency between objects where a state change in one object results in all its dependents being notified and updated automatically.

* Strategy - Define a family of algorithms, encapsulate each one, and make them interchangeable. Strategy lets the algorithm vary independently from clients that use it.

> Thinks to Think on: </br>
> We have great discussion about Object, classes and their interactions. We understood how to create, use and communicate objects. 
> What about reponsibilities of these Object?

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
