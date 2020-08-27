# Class properties and capabilities

Guidelines help us to create an efficient CLASS, whats next?... An efficient CLASS, without interaction is of no use.

## What happens when an efficient class is build?

An efficient CLASS construction will give you the object, which have all real world object properties.
Also provide us with 4 major principles which make the solution designed an Object Oriented one.

4 major principles are :
1) Encapsulation
2) Abstraction
3) Inheritance
4) Polymorphism

## Encapsulation  
Encapsulation is an idea of bundling data and methods that work on the data within one unit. It is a mechanism of hiding of data implementation by restricting access to public methods. It reduce complexity and increase re-usability.

```java
// Encapsulation
class ProductEncapsulation {
	private String productName;
	private String productId;

        public String getproductName() {
              return productName;
        }

        public String getproductId() {
              return productId;
        }

        public void setproductName(String productName) {
              this.productName = productName;
        }

        public void setproductId(String productId) {
              this.productId = productId;
        }
}

public class ProctuctEncap {

   public static void main(String args[]) {
      ProductEncapsulation encap = new ProductEncapsulation();
      encap.setproductName("Jacket");
      encap.setproductId("9878664335");

      System.out.print("Name : " + encap.getproductName() + " Age : " + encap.getproductId());
   }
}

```
## Abstraction   
Abstraction is about hiding unwanted details while giving out most essential details. It reduce complexity and isolate impact of changes.

```java
// Abstraction example
// It becomes blue print for implementation
// can't instantiate abstract class
abstract class HumanClass{
  abstract void sleep();
  abstract void study();
}
class FatherClass extends HumanClass{
  void sleep(){
    System.out.print("Snore");
  }

  void study(){
    System.out.print("chemistry");
  }
}

public class relation {
  public static void main(String [] args){
    FatherClass myfather = new FatherClass();
    myfather.sleep();

  }
}
```
>HumanClass myHuman = new HumanClass();
relation.java:28: error: HumanClass is abstract; cannot be instantiated
HumanClass myHuman = new HumanClass();
^
1 error

## Inheritance
Inheritance is a mechanism in which one class acquires the property of another class, It will eliminate redundant code.

```java
// Inheritance example.
class FatherClass{
  void sleep(){
    System.out.print("Snore");
  }
}

class ChildClass extends FatherClass{
  void study(){
    System.out.print("Math");
  }
}

public class relation {
  public static void main(String [] args){
    ChildClass myChild = new ChildClass();
    myChild.sleep();
  }
}

```

## Polymorphism  
Polymorphism describes a pattern in object oriented programming in which classes have different functionality while sharing a common interface. It refers to the ability of a variable, function or object to take on multiple forms.

```java
// Polymorphism is the capacity to take on different forms
// Polymorphism with Class Methods
class FatherClass {
  void move(){
    System.out.print("walk");
  }
}

class ChildClass {
  void move(){
    System.out.print("run");
  }
}

public class relation {
  public static void main(String [] args){
    FatherClass myFather = new FatherClass();
    ChildClass myChild = new ChildClass();

    myFather.move();
    myChild.move();
  }
}

```

## What is that our solution gaining by applying 4 principle?

* Encapsulation give the solution a modularity and be more self centered, binding processing function and data together. Everything is capsuled and protected within the boundary of class.

* Abstraction gives Structure and Guidelines to the Solution. Abstraction is not implementation, it just portrays an idea, an idea for sub classes to follow in their implementation.

* Inheritance passes knowledge down and reduce redundant code. It reduces code by gaining insight from the super class.

* Polymorphism provide dynamic behavior to solution, solution can react to the situation in different ways.

## What happens when our solution applies Object oriented principles?

This Enhances the created object in their interaction and operations. The Objects inside solution will acquire capabilities of having different kind of relationship with each other.

1) Association
2) Aggregation
3) Composition

### Association
Association is relationship between two classes where one class utilizes features of another class. A kind of "Has A" relationship...

```java
// Association example
class Manager{
  private String name;
  public Manager(String name){
    this.name = name;
  }

  public String Logon(SwipeCard obj){
    return obj.Swipe(this);
  }

  public String getManagerName(SwipeCard obj){
    return name;
  }
}

class SwipeCard{
  private String cardID;
  public SwipeCard(String cardID){
    this.cardID = cardID;
  }

  public String Swipe(Manager obj){
    return "Login Successful";
  }

  public String swipeCardID(){
    return cardID;
  }
}

public class relation {
  public static void main(String [] args){
    Manager mike = new Manager("Mike");
    SwipeCard ton = new SwipeCard("C0120");
    System.out.println(mike.Logon(ton));
  }
}

```

### Aggregation

Aggregation in Java is a relationship between two classes that is best described as a "has-a" and "whole/part" relationship. Class has an owner and can exist independently.

```java
class Employee{
  private String name;
  private String Address;
  public Employee(String name){
    this.name = name;
  }

  public void getManagerCountry(Address addr){
    System.out.println(addr.getAddressCountry());
  }
  public void setManagerName(String name){
    this.name = name;
  }

  public void getManagerName(){
    System.out.println(name);
  }
}

public class relation {
  public static void main(String [] args){
    Employee mike = new Employee("Mike");
    Address mikeAddr = new Address(55, "New Britain", "Connecticut", "US");

    mike.getManagerName();
    mike.getManagerCountry(mikeAddr);

  }
}

```

### Composition
Composition is the design technique to implement has-a relationship in classes. Rather than inheriting by extending the class, idea is to have the Composition by referencing the object in you new class.


```java
// Composition example
class HumanClass {
  private String name;

  public HumanClass(String name){
    this.name = name;
  }

  public String toString(){
    return name;
  }

}

class DogClass{
  private String name;
  private HumanClass owner;
  public DogClass(String name, HumanClass owner){
    this.name = name;
    this.owner = owner;
  }

  public String toString(){
    return String.format("My name is :%s, My Owner name is :%s", name, owner);
  }
}

public class relation {
  public static void main(String [] args){
    HumanClass mike = new HumanClass("Mike");
    DogClass ton = new DogClass("ton", mike);
  }
}

```

> An object is simply a value or variable that has a method, A method is a function associated with a particular object. An Object Oriented program is the one that uses methods to express the properties and operations on each data structure.

> Difference between Function and Method. A function is a block of organised, reusable code that is used to perform a single, related action. Method is a type of function through which one object communicate with another object. 

## How to gauge the quality of Classes designed?
Idea of class is getting more enhancements and upgrades. With these sophisticated way of defining class, comes with challenge to gauge the quality of the class being created. We definitely need a base to measure the quality of class.

Grady Booch proposes five metrics to measure the quality of classes:

* Coupling
* Cohesion
* Sufficiency
* Completeness
* Primitiveness

## Coupling  

Coupling refers to how strongly a software element is connected to other elements, it's an indication of relationship between the objects.

```
coupling is the degree of interdependence between software modules; a measure of
how closely connected two routines or modules are; the strength of the relationships
between modules.
                                                                  - wikipedia
```
## Cohesion

Cohesion is an indication of how related and focused the responsibilities of an software element are, it's an indication of relationship of elements within the class. Ideal case is to have high internal Cohesion, High cohesion means that the class is focused on what it should be doing, i.e. only methods relating to the intention of the class.

Low Cohesion
```java
class staffMail {
	checkEmail();
	sendEmail();
	printLetter();
}
```
High Cohesion
```java
class staffMail {
	private String emailAddress;

	public setEmailaddr(String emailAddress){
		this.emailAddress = emailAddress;
	}

	public getEmailaddr(){
		return emailAddress;		
	}
}
```
High Cohesion example is clear about intention and more focused.Low Cohesion example is not focused and have additional responsibility.

>  The code inside each Java class must have high internal cohesion, but be as loosely coupled as possible to the code in other Java classes.

## Sufficiency
* Does the class capture enough of the details of the thing being modeled to be useful?
## Completeness
* Does the class capture all of the useful behavior of the thing being modeled to be re-usable?
## Primitiveness
* Does the class capture all of the useful behavior of the thing being modeled to be re-usable?


> Irrespective of any interview or discussion on Object orient programming, you might have come across these question.
> What is the difference between function and a method?
> Why multiple inheritance is not allowed in JAVA?

---------------------------------------------------------------------
# Interface
Now that we understood Class and Class types, lets discuss about communication between the Objects instantiated by the Class. Get introduced to Interface.... 

In general, an interface is a device or a system that unrelated entities use to interact. It defines the rules of communication between two un related objects. 
```
"In object oriented programming, a protocol or interface is a common 
means for unrelated objects to communicate with each other"
                                                         -Wikipedia
```
Interfaces form a contract between the class and the outside world, and this contract is enforced at build time by the compiler.

```java
//Interface
interface Plane {
   public void wings();
   public void engine();
}

//Jet implements the Plane interface
class Jet implements Plane {
   public void wings() {
      System.out.println("2 wings");
   }

   public void engine() {
      System.out.println("wroong")
   }
}

public MyMainClass {
   public static void main(Strings[] args){
      Jet myJet = new Jet();  // create new jet object
      myJet.wings();
      myJet.engine();
   }
}
```

> re visit Interface example
