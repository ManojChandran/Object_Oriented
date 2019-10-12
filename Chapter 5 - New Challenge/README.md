# New Challenge

Road to Object Oriented Programming was open and many of us came up with new languages to code in Object Oriented way. Adding on to this, we introduced many techniques and tweak's with the language.

  1) Access Modifiers to protect the class.
  2) Constructors to initialize the class.
  3) Interfaces to enhance Abstraction of class.
  4) Static to stop object creation.
  5) Final to stop class mutation.
  6) Type

### Access Modifiers

* Private: The access level of a private modifier is only within the class. It cannot be accessed from outside the class.
* Default: The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.
* Protected: The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.
* Public: The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.

### Constructors

Constructor is a block of code that initializes the newly created object

```java
// Constructor example
class MyClass{
   //This is the constructor
   MyClass(){
     System.out.print("I am initializing the newly created object");
   }
}
public class ObjectInitialization {
  public static void main(String [] args){
    MyClass constr = new MyClass();
  }
}
```

### Interface

Interface is an agreement.

```java
interface HumanClass{
  public void sleep();
  public void study();
}
class FatherClass implements HumanClass{
  public void sleep(){
    System.out.print("Snore");
  }

  public void study(){
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

## Static
## Final
## Type


Half of the us started believing, knowing an object oriented principle and applying them will get them good code. Road became congested with implementation of these ideas, We started getting traffic jam. Consistently the promise of reuse and maintainable code was broken.

## What was the new challenge?

With acquired power and features, we started solving bigger issues. Later time, we started enhancing the solutions. It took less time for us to understand that, code has become increasingly complex. So complex, that upgrade is becoming very hard. There were times when we need to rewrite the entire code, re architect it.

Simple, Good and maintainable code still an impossible target to achieve.....

## What are the basic principle to write a maintainable code?

There were extensive study and analysis done on techniques to achieve this. On gradual study we arrived at OOP principles which will helped us to simplify things. Basic OOP design principles to follow while designing the solution are as explained below.

* Encapsulate what varies.
* Favor Composition over Inheritance.
* Program to Interface, not to implementation.
* Depend on Abstraction, do not depend on concrete class.
* Strive for loosely coupled design between object that interact.

## How to gauge the quality of Class?
Grady Booch proposes five metrics to measure the quality of classes:

* Coupling
* Cohesion
* Sufficiency
* Completeness
* Primitiveness
