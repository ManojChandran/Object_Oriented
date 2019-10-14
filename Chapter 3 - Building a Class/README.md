# Building a Class

Once the CLASS and OBJECT is defined, we extend our work to improve it. Industry came up with guidelines to create an efficient class, which is key for any solution.

First step towards Object Orientation, is to design an efficient class.

## How can we build an efficient class?
Defining a class in a design, developer should have multiple factors in consideration.

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
### Open Closed Principle
* Software entities should be open for extension, but closed for modification.
### Liskov Substitution Principle
* Sub types must be substitutable for their base type.
### Interface Segregation Principle
* The dependency of one class to another, should depend on the smallest possible interface.
### Dependency Inversion Principle
* Depends on abstractions (interfaces), not on concrete classes.
