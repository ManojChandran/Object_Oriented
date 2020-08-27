# Building a Class

Once the CLASS and OBJECT is defined, we extend our work to improve it. Try to deep dive into CLASS, its properties and interactions. Also, we will discuss security concept in Object Oriented Programming and how we can achive it.

> Things to think on:</br>
> Real life object hide its composition and make, they just display the Attributes and Behavior. Certain times they don't display or convey the reason behind their Attributes and Behavior. This might be part of their security and data hiding.</br>
>
> Software entity also has the attain the same, How its realized in our Software solution?</br>

# Access Modifiers

While describing class and its signature, we discussed about access modifiers. These access modifiers can be applied to class, method and data types. Based on these access modifiers data hiding or access controll is achived between objects.

`Private`: The access level of a private modifier is only within the class. It cannot be accessed from outside the class.</br>
`Default`: The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.</br>
`Protected`: The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.</br>
`Public`: The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.</br>

# Class types

Now that we have learned about declartion of class, lets explore types avilable. 

Yes!!!...  what are the type of classes we can create?

### Concrete class
A simple class which can be instantiated, extended....etc. One which is normal.
```java
public class Plane {
   public Plane() {

   }

   public void setSpeed(int speed) {
      this.speed = speed;
   }
}
```
### Inner class - group your class
An Inner class is a class within the class, mostly use to group a couple of classes together.
```java
public class OuterClass{
   class InnerClass{
      // only inner class are allowed to be static in Java.
   }
}
```
### Abstract class - not allowed to instantiate
An Abstract class is the one, which is not allowed to instantiate. Without instatntiating, no objects are created.
```java
public class GraphicObject {
   // declare fields
   abstract void draw(); // Abstract method, automatically makes the class as Abstract.
}
```
### Final class - not allowed to inherit
A Final class is the one, which is not allowed to extend. Without extending, no inheritens possible.
```java
final class MyObject {
   // methods and fields
}
```
### Static class - not allowed to inherit nor instantiate
A Static class is the one, which is not allowed to instantiate or inherit. 
```java
public class OuterClass{
   static class IamStaticClass{
      // only inner class are allowed to be static in Java.
   }
}
```
> Things to think on:</br>
> Now that we have learned to create class, Is there any guidelines to create a class?

# Efficient class

Industry came up with guidelines to create an efficient class, which is key for any solution.
First step towards Object Orientation, is to design an efficient class.

## Why we need an efficient CLASS?

Idea of writing a good code is to have certain properties. A good code should be,

* Easy to Read and Understand
* Easy to Upgrade and Maintainable
* Easy to Extend and reuse Components

To achieve this, we need to start with base building block "CLASS". By creating an efficient class "CLASS", we are creating strong base to build a big building.

>Above criteria seems simple and logical...But
>Being simple is a noble pursuit of any design and trying to make something simple is hard.- Anonymous.

## How can we build an efficient class?
Defining a class in a design, developer should consider multiple factors.

1) Class should provide rigidity to design, changes in class should not effect many other parts.
2) Shouldn't make design fragile, things should not break in unrelated places.
3) Should Stop reuse of code outside of its original context.

Considering these above criteria, Uncle Bob proposed solid principle. He requested developers to follow the principle, to create an efficient Class.

```
The theory of SOLID principles was introduced by Martin in his 2000 paper Design Principles
and Design Patterns, although the SOLID acronym was introduced later by Michael Feathers.
                                                                  - Wikipedia

  SOLID stands for
   S - Single responsibility Principle
   O - Open Closed Principle
   L - Liskov Substitution Principle
   I - Interface Segregation Principle
   D - Dependency Inversion Principle
```

### Single Responsibility Principle
* A class should have one and only one reason to changes.

For every other enhancement, if we are forced to touch the class! then the class needs refactoring. Big problem in touching the class is, its impact on objects created from it and their interactions. High possibility of introducing bugs or functionality changes.

### Open Closed Principle
* Software entities should be open for extension, but closed for modification.

Software entities include Classes, modules, method ...etc, We should be able to extend its behavior. "Closed for modification" simply means code remains unchanged.

### Liskov Substitution Principle
* Sub types must be substitutable for their base type.

We should be able to substitue base class objects with child class objects and this process should not alter the behaviour/ characteristics of program.

### Interface Segregation Principle
* Clients should not be forced to depend upon interface that they do not use.

The dependency of one class to another, should depend on the smallest possible interface. Idea is to reduce interface pollution.

### Dependency Inversion Principle
* Depends on abstractions (interfaces), not on concrete classes.



```
Interface pollution is about creating large interfaces or grabbing more Unrelated Methods.

Signs of Interface Pollution 
   - Classes have empty method Implementation
   - Method Implementations throw UnsupportedOperationException 
   - Method Implementations return default/ dummy values
```