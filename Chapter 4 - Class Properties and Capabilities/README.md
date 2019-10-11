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

```python
# Encapsulation
class ProductEncapsulation(object):
    """docstring ProdEncapsulation."""

    def __init__(self):
        self.__productName = 't-shirt'
        self.__brandCode = '871628736777'

    def getProductname(self):
        return self.__productName

    def getbradCode(self):
        return self.__brandCode

def main():
    Item = ProductEncapsulation()
    print(Item.getProductname())
    print(Item.getbradCode())

if __name__ == '__main__':
    main()

Output
t-shirt
871628736777

```

## Abstraction   
Abstraction is about hiding unwanted details while giving out most essential details. It reduce complexity and isolate impact of changes.

```python
# Abstraction example
# It becomes blue print for implementation
# can't instantiate abstract class
from abc import ABC, abstractmethod # ABC = Abstract Base Classes
class abstarctLandAnimal(ABC):
    """docstring for abstarctLandAnimal."""
    def __init__(self):
        super().__init__()    

    @abstractmethod
    def walk(self):
        pass

    @abstractmethod
    def talk(self):
        pass

class Duck(abstarctLandAnimal):
    """docstring for Duck."""

    def __init__(self):
        super().__init__()
        self.name = 'duck'

    def walk(self):
        print('duck walks')
    def talk(self):
        print('duck quaks')

def main():
    d1 = Duck()
    d1.walk()
    d1.talk()

if __name__ == '__main__':
    main()

```

## Inheritance
Inheritance is a mechanism in which one class acquires the property of another class, It will eliminate redundant code.

```python
# Inheritance example.
class MyFatherClass(object):
    def __init__(self):
        print('snore')

class ChildClass(MyFatherClass):
    def __init__(self):
        super().__init__()

def main():
    d1 = ChildClass() # child inherits snoring from father.

if __name__ == '__main__':
    main()

Output
snore

```

## Polymorphism  
Polymorphism describes a pattern in object oriented programming in which classes have different functionality while sharing a common interface. It refers to the ability of a variable, function or object to take on multiple forms.

```python
# Polymorphism is the capacity to take on different forms
# Polymorphism with Class Methods
class Add(object):
    """docstring for Add."""

    def operation(self, x, y):
        self.x = x
        self.y = y
        return (self.x + self.y)

class Sub(object):
    """docstring for Sub."""

    def operation(self, x, y):
        self.x = x
        self.y = y
        return (self.x - self.y)

def main():
    A = Add()
    S = Sub()

    for resultof in (A, S):
        print(resultof.operation(5,3))

if __name__ == '__main__':
    main()

Output
8
2

```

## What is that solution gaining by applying the 4 principle?

* Encapsulation give the solution a modularity and be more self centered, binding processing function and data together.

* Abstraction gives Structure and Guidelines to the Solution. Abstraction is not implementation, it just portray an idea, by that guide the sub classes to follow the implementation.

* Inheritance passes knowledge down and reduce redundant code. It reduces code by gaining insight from the super class.

* Polymorphism provide dynamic behavior to solution, solution can react to the situation in different ways.

## What happens when our solution applies Object oriented principles?

This Enhances the created object in their interaction and operations. The Objects inside solution will acquire capabilities mentioned below

1) Association
2) Aggregation
3) Composition
4) Dependency
