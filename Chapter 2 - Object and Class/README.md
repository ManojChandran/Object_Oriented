# Object and Class

Every idea has its significance, when the solutions it can offer is high. Once the idea "Object" was born, everybody worked towards to apply it. First and foremost thing to do, is to define the idea.  

## What are Objects and Classes?
An Object in real world will have attributes (color, texture,..) and behavior(scroll, bend..). In computer world, Object is a package of both data(attribute) and procedures (behavior) that operate on that data. When we define the object, we will end up creating a "CLASS".

```java
// Simple dog class.
public class Dog {
   String breed;  // attribute
   int age;
   String color;

   void bark() {    // behavior
	    System.out.println("Bow Bow");
   }

   void happy() {
	    System.out.println("Spins Tail");
   }
}
```
# Class declaration 
Lets start with declaring a class in java, see the below example.

```java
public class Student {
   int id;
   String name;       // Class body
}
```
Declaration constitutes following parts,
* Modifier  
* class keyword 
* Class name 
* Class body 

# Class types

Now that we have learned about declartion of class, lets explore types avilable. 

Yes!!!...  what type of classes we can create?

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
### Inner class - group your class
An Inner class is a class within the class, mostly use to group a couple of classes together.
```java
public class OuterClass{
   class InnerClass{
      // only inner class are allowed to be static in Java.
   }
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

# Conclusion
Class is a blue print of the object, attributes are the data and methods were its behavior. The efficiency and design of the class will, improves our solution. Success of our software solution, depends on

* How "Object" is defined with a "Class"?
* How interactions between "Object" happens?
