# Object and Class

Every idea has its significance, when the solutions it can offer is high. Once the idea "Object" was born, everybody worked towards applying it. First and foremost thing to do, is to define the idea. 

## What are Objects and Classes?
An Object in real world will have attributes (color, texture,..) and behavior(scroll, bend..). In computer world, Object is a package of both data(attribute) and procedures (behavior) that operate on that data. When we define the object, we will end up creating a "CLASS".

```java
// Simple human class.
class Human {
   String sex;      // attribute, which signifies Data
   int age;
   float height, weight;

   void walks() {    // behavior, which signifies operations that can be done on data
	    System.out.println("walks with Two legs");
   }

   void talks() {
	    System.out.println("Talks many language");
   }
}
```
# Class declaration 
Lets demstify the class, let's start with declaring a class in java. See the below example.

```java
private class Human {
   String sex;      
   int age;
   float height, weight;     // Class body
}
```
CLASS declaration constitutes following parts,
* Modifier - defines access privillege of the class.
* class keyword - communicates to compiler following piece of code, represents class definition.
* Class name - defines the name of the class.
* Class body - definition of class itself.

> note: above description is true for any language you learn, these four parts constitute a class.

# Object creation

We clearly understood class defintion, now its time to create an Object. In JAVA, we use "new" keyword.

```java
class Human {
   String sex;      //attribute
   int age;
   float height, weight;

   void walks() {    // behavior
	    System.out.println("walks with two legs");
   }

   void talks() {
	    System.out.println("Talks many language");
   }
}

public class myHuman{
   public static void main(String args[]){
      // new keyword will create object men of type Human
      Human men = new Human();
      men.walks();
   }
}
output:
walks with two legs
```
Clear understanding of following line `Human men = new Human();` is essential for our understanding and grasp the ideas. </br>

Literal meaning : We are creating object named `men` of type `Human` using key word `new` by calling `Human()` class. </br>
Real meaning : System allocates memory for Object with name `men` and of type `Human`.

> Things to think on : </br>
> 1) what is this "Human()" method which new operator is calling? </br>
> 2) We haven't defined "Human()" method, where did it came from? </br>

# Constructor

During our chapter 1 discussion, we talked about the STATE of an OBJECT, any real world entity has a state. Consider a person walking in rain, he will get wet and by time, he might get cold. Now person is in wet and cold state, he might have started dry and warm state from home. Similarly, software objects have state and during interaction with other objects, it will change. These state has important part in decision making of software entities. We learned to define OBJECT using class, learned antomy of a class and instantiate it with `new` to create an OBJECT. Now our big question is...

`How we can set the state of an object?`

Let me introduce `Constructor`, every class contains a costructor and get invoked to create an OBJECT. Constructor can be called as a special method that get's called every time, when we create an OBJECT using `new` keyword. Same constructor method is used to set the state of an OBJECT. 

Constructor: The one method which construct the OBJECT for you.

* Compiler Implicitly build constructor, Programmer can explicitly define constructor a class.
* Constructor method will or should have same name as class name.
* Our `new` operator calls constructor method to create an OBJECT.
* Constructor will get executed, when object is instantiated.

```java
class Human {
   Human () { // constructor body

   }
}
```

#### Constructor types

Constructor methods are created by default by compiler, we use the same method to create the object. Object oriented programming language allow you to define constructor and there are different types of constructor.

##### Default Constructor

Default constructors are the one which gets created implicitly by compiler. 
```java
public class Human {
   int age; //attribute
   float height, weight;

   public static void main(String args[]){
      // default constructor is called to create object
	   Human men = new Human();
   }
}
```
##### No-args Constructor

No-args constructors are explicit constructor methods declared without parameters.
```java
public class Human {
   int age; //attribute
   float height, weight;
   
   Human() {
   	this.age = 16;
   }

   public static void main(String args[]){
      // No-args explicit constructor
	   Human men = new Human();
	   System.out.println(men.age); // print 16
   }
}
```

##### Parametrized Constructor

Parametrized constructors are explicit constructor methods declared with parameters.
```java
public class Human {
   int age; //attribute
   float height, weight;
   
   Human(int age) {
   	this.age = age; // recieve and set the age of created object
   }

   public static void main(String args[]){
       // Parametrized explicit constructor
	    Human men = new Human(30);
	    System.out.println(men.age);
   }
}
```
> Things to think on: </br>
> How do we refer the OBJECT inside Class? </br>
> What "this" keyword used in constructor? </br>

# Magic of "this"

`this` is the keyword used to refer the OBJECT, refer the below example. Output value printed for `this` and `men` object are same, this the proof for reference.

```java
public class Human {
   int age;          
   float height, weight;
   
   Human() {
   	System.out.println("this reference = " + this);
   }

   public static void main(String args[]){
      // No-args explicit constructor
	   Human men = new Human();
	   System.out.println("object reference = " + men);
   }
}
output:
this reference = Human@24d46ca6
object reference = Human@24d46ca6
```
> Note :`this` is used in Java and Javascript, Python uses `self` keyword.
> Idea is to refer the OBJECT inside class, to assign or set value to the OBJECT attributes.

# Conclusion
Class is a blue print of the object, attributes are the data and methods were its behavior. Interface makes sure proper communication between the classes

The efficiency and design of the class will, improves our solution. Success of our software solution, depends on

* How "Object" is defined with a "Class"?
* How interactions between "Object" happens?


> Things to think on : </br>
> General understanding : Real life entity (eg: Bench) -> Create a blue print (class Bench) -> Instatiate the class, create Object.</br>
>
> General Observation : Real life entity wear and tear by time.</br>
>
> Question: Does Object created from the class (Blue print of the real life entity) wear and tear or get damaged. </br>
>
> Note: Its clear about Object life cycle, "new" will create the Object" -> Object stays in Memory -> dies with program execution completion or program exit.</br>
>
> Wear and tear is different from this.</br>
