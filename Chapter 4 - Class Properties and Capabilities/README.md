# Class properties and capabilities

Guidelines help us to create an efficient CLASS, whats next?... An efficient CLASS, without interaction is of no use. By defining class and instantiating it, we create Object.

## What happens when an efficient class is created?

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

/*	HumanClass myHuman = new HumanClass();
		relation.java:28: error: HumanClass is abstract; cannot be instantiated
    HumanClass myHuman = new HumanClass();
                         ^
		1 error */
  }
}
```

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

## What is that our solution gaining by applying the 4 principle?

* Encapsulation give the solution a modularity and be more self centered, binding processing function and data together. Everything is capsuled and protected within the boundary of class.

* Abstraction gives Structure and Guidelines to the Solution. Abstraction is not implementation, it just portrays an idea, by that idea the sub classes to follow the implementation.

* Inheritance passes knowledge down and reduce redundant code. It reduces code by gaining insight from the super class.

* Polymorphism provide dynamic behavior to solution, solution can react to the situation in different ways.

## What happens when our solution applies Object oriented principles?

This Enhances the created object in their interaction and operations. The Objects inside solution will acquire capabilities mentioned below

1) Association
2) Aggregation
3) Composition
4) Dependency
