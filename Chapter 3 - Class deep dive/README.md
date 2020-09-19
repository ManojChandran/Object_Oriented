# Class Deep dive

Once the CLASS and OBJECT is defined, we extend our work to improve it. Let's take a deep dive into CLASS, its types and interactions. Also, we will discuss security concept in Object Oriented Programming and how we can achive it.

> Things to think on:</br>
> Real life object hide its composition and make, they just display the Attributes and Behavior. Certain times they don't display or convey the reason behind their Attributes and Behavior. This might be part of their security and data hiding.</br>
>
> Software entity also has the attain the same, How its realized in our Software solution?</br>

# Scope

Additional concept which boosted Object Oriented Proraming, is all our solutions are in and around handling DATA. Data is put in memory and operation are carried out with refering them with a name (Programing term is variable). Object Oriented Programming paradigm, emphasis is more on data than application logic. Data handling, representation and protection are all given more importance. This is achived by a concept called `scope`.

```
Scope refers to the visibility of variables and methods in one part of a program to another part of that program. 
```

try this out...
```java
public class Men {
   public static void main(String args[]){
	   {
	   int x = 5;
      }
      System.out.println(x);
   }
}
```

> Things to Think on: </br>
> Can we access or refer object oriented entities by name in each every place in program? </br>
> What determines the visiblity these entities?

# Modifiers

All the CLASS we defined and OBJECT created, has an association of name. The name is used to refer these entities in different parts of the program. 

Modifiers are keywords which alters the access and visibility of the definitions, there are two types of Modifiers...

 * Access Modifiers
 * Non-Access Modifiers

## Access Modifiers

While describing class and its signature, we discussed about access modifiers. These access modifiers can be applied to class, method and data types. Based on these access modifiers data hiding or access controll is achived between objects.

```
Access modifiers in JAVA specifies the accessibility or scope of fields, methods, constructors or class.
```

`Private` : The access level of a private modifier is only within the class. It cannot be accessed from outside the class.</br>
`Default` : The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.</br>
`Protected` : The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.</br>
`Public` : The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.</br>

## Non-access Modifiers

Access modifiers deals with the visibility of the variable, methods and class. Non-access modifiers deals with defining the operations done on them.

`Static` modifier for creating class methods and variables.</br>
`Final` modifier for finalizing the implementations of classes, methods, and variables.</br>
`Abstract` modifier for creating abstract classes and methods.</br>

# Class types

Now that we have learned about declartion of class, lets explore types avilable. 

Yes!!!...  what are the type of classes we can create?

## Concrete class
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
## Inner class - group your class
An Inner class is a class within the class, mostly use to group a couple of classes together.
```java
public class OuterClass{
   class InnerClass{
      // only inner class are allowed to be static in Java.
   }
}
```
## Abstract class - not allowed to instantiate
An Abstract class is the one, which is not allowed to instantiate. Without instatntiating, no objects are created.
```java
public class GraphicObject {
   // declare fields
   abstract void draw(); // Abstract method, automatically makes the class as Abstract.
}
```
## Final class - not allowed to inherit
A Final class is the one, which is not allowed to extend. Without extending, no inheritens possible.
```java
final class MyObject {
   // methods and fields
}
```
## Static class - not allowed to inherit nor instantiate
A Static class is the one, which is not allowed to instantiate or inherit. 
```java
public class OuterClass{
   static class IamStaticClass{
      // only inner class are allowed to be static in Java.
   }
}
```
> Things to think on:</br>
> What is this INHERITANCE heritance we are talking about?

# Interface
Now that we understood Class and Class types, lets discuss about communication between the Objects instantiated by the Class. Communication between two entities depend on the protocol of communication, guidelines set or a contract defined. Similarly communication between the Objects instantiated by the class, also need to set a protocol. Let's get introduced to Interface.... 

In general, an interface is a device or a system that unrelated entities use to interact. It defines the rules of communication between two un related objects. 
```
"In object oriented programming, a protocol or interface is a common 
means for unrelated objects to communicate with each other"
                                                         -Wikipedia
```
Interfaces form a contract between the class and the outside world, and this contract is enforced at build time by the compiler.

```java
// define interface
interface piereadwrite {
	public char Read();
	public void Write(char in); 
}

// piport implements readwrite interface
class Port implements piereadwrite {
       char dataIn;
       char dataOut;

	public char Read() {
	        this.dataOut = this.dataIn;
		return this.dataOut;
	}
	
	public void Write(char dataIn) {
		this.dataIn = dataIn;
		System.out.println("Write :"+ this.dataIn);
	}	
}

public class MyPie {
	public static void main(String[] args){
	     Port piPort = new Port();
     	     piPort.Write('A');
     	     System.out.println("Read :"+ piPort.Read());
	}
}
```

In the above example, Interface `piereadwrite` defines the signature for Read and Write method without its implemenatation. Its created a standard, who ever wants to create a pie object will have to implement to the port with read write signature. 

## Interface pollution
Sometimes over doing things will cause issue!!!!
Even though Interface is a good thing, over doing it will get you `Interface pollution'. It is about creating large interfaces or grabbing more Unrelated Methods.

below mentioned are signs of Interface Pollution
   - Classes have empty method Implementation
   - Method Implementations throw UnsupportedOperationException 
   - Method Implementations return default/ dummy values

> Things to think on:</br>
> Yes, we know about class...what else?
> Is there any guidelines to create a class?

# Efficient class

Industry came up with guidelines to create an efficient class, which is key for any solution.
First step towards Object Orientation, is to design an efficient class.

## Why we need an efficient CLASS?

Often software application written fails with follwoing three issues, which will cause maintnenance and enhancement hard.

* RIGIDITY - Every change made will effect many other parts, making it a huge task.
* FRAGILITY - Things start breaking in unrelated parts of the application.
* IMMOBILITY - Cannot re-use the code outside of its original context.

Idea of writing a good code is to have certain properties. A good code should be,

* Easy to Read and Understand
* Easy to Upgrade and Maintain
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



