# Introduction

Evolving complex systems and new challenges, are making life hell for coders. The industry thriving for efficient and optimized code, it is evident by increasing complexity of problems and solutions. To tackle this, we coders has to keep up with changing terrain. This is not possible all times, most of the time coder is pushed to provide "fix" than actually addressing the issue. Urgency makes coders life hell....

Solution is to go back to basics, refresh our understandings of core principle and strong basics in writing code. When we are clear about our path, travel will be easy. Clarity will be achieved when We  understand the evolution of programming in general and what led to new programming concepts.

This book attempt to refresh the basics and provide a clear picture for beginners to start with. Concentrate more on evolution, trying to explain them.

## What is Object Oriented Programming?

Just refer to what Wikipedia has to say...

```
Object-oriented programming is a programming paradigm based on the concept
of "objects", which can contain data, in the form of fields, and code, in
the form of procedures. A feature of objects is an object's procedures that
can access and often modify the data fields of the object with which they
are  associated.                                                                             
                                                          - Wikipedia
```
yeah, I got it. To understand this, we need start our journey. 
A journey to understand why we code? why we code like this?

## Everything has a beginning

Human civilization evolved every day and with each step in evolution, complex questions blocked them in their journey. A need for companion was felt in every step and luckily!!!...we found one to help us in desperate times, Machines !!!!!

Initially it was in the form of small tools and gradually evolved with us, it evolved into a complex ones. World of machine fascinated us and we devoted ourselves to the machines of their working. Day by day our need to solve problem and its complexity increased, simultaneously need for more powerful and intelligent machine increased. We as a civilization, extended our relationship with machine by introducing language to speak with them. Machines started understand our instructions with language we decided to communicate with them, thus Software came into existence.

We started solving real world problems and at times break our backs to make the machine understand it.

Those problems, needed real world thoughts and solutions. Real world is full of objects and their solutions is also related with it. Communicating the real world issue to machine was a complex thing to do, out entirely depends on how well we describe issue to machine. 

Problems around us, where big and very much from the real world!!!

Bigger problems, we can achive it by braking down the problem and take a step by step approach towards solution. First form of break down happened in the form of Procedure (function). Problems were boken down into smaller ones and started resolving one by one. These `procedure` have specific, defined input and provide output in defined format. More and more `procedure` (functions) where created, solutions became complicated and hard to maintain. Functions, sub functions, sub sub functions....more over not representing real world entities.

```
Funtions have following problem : 
1) High memory consumption, because of stacking the details of calling program 
2) Functions cannot determine the access privillege of Data getting handled. 
3) Functions cannot hold state, most system decisions are taken on the state of the entity.
   Consider a real world scenario where you say hello to one person, response will depend on the state
   or impact of his previous interaction. If you are calling a function, it will process the request 
   and always give same type of response. There won't be any kind of impact of previous interactions.
4) Fuction couldn't guarantee data security or abstraction.

   But most of our real life decisions are made or taken considering the state of the entity.
```

Discussion heated up, on finding a new approach to solve the problem. An efficient approach to address all entities and their associated interaction in real world, realize it in program world. Suddenly there was a revelation "our problems in real world are with OBJECTS, solutions are really their interactions".

# Lets define the Object....
```
OBJECT - Any thing that has state and exhibit behavior
```

How do you represent it in digital world?
By defining state as attributes and behavior as function.

Now that we learned little bit of history and the idea to create "OBJECT", let's take our next step....

#

> Things to Think on:</br>
> Who discovered Object Oriented programming? </br>
> Ole-John Dahl and Kristen Nygaard at the Norwegian Computing Center in Oslo, Norway. Both working with ALGOL, knocked up with an idea. </br>
> IDEA : Local variable are stored in stack and Local variables of function are stored in special "function stack frame". Additionally there are option to declare functions which were also stored in stack. Ole-John and Kristen thought of moving "function stack frame" from stack to Heap. In this case, sub functions and calling functions can still operate on the function's local variables. We don't have to distroy function local variables every time we come out of function.