# Introduction

Evolving complex systems and new challenges are making life of coders, a hell. Industry is thriving for efficient and optimized code, it is evident by increasing complexity of problems and solutions. To tackle this, we coders has to keep up with changing terrain. This is not possible all times, most of the time coder is pushed to provide "fix" than actually addressing the issue. Urgency pushes coders to compromise and his or her life a hell....

Possible solution is to go back to basics, refresh our understandings of core principle and strong basics in writing code. When we are clear about our path, travel will be easy. Clarity will be achieved when We understand the evolution of programming in general and what led to new programming concepts.

This book attempt to refresh the basics and provide a clear picture for beginners to start with. We want new programmers to start asking questions, question which give clarrity on two things....
```
Why we code?
Why we code like this?
```
## Let's talk about CODE

Let's start our journey with basic question....
```
What is CODE?
Why we CODE?
```
Human civilization evolved every day and with each step in evolution, complex questions blocked them in their journey. A need for companion to assit us, was felt in every step and luckily!!!...we found one to help us in desperate times, Machines !!!!!

Initially Machine was assisting us, in the form of small tools and gradually evolved with us. It evolved into a complex ones, one which can remember. 

Additional benefits of Machine...
* Can repeat task N number of time.
* Can do it in high Precision.
* Can do it with less Fatigue.

Evolution of machines which can remember, fascinated us and we devoted ourselves to improve them. Primary enhancement of a Machine which can remember is to make it undertand `What needs to be remembered?`. By remembering, Machine know what to do when requested the assisstance. We as a civilization, extended our relationship with machine by introducing language to speak with them. Machines started understanding our instructions with language we decided to communicate with them, thus we started writing it down as `CODE`.

We write CODE to make our machine understand `what to remember?`. CODE is a set of instruction written down for the same.

## Everything has a beginning

Day by day our need to solve problem and its complexity increased, simultaneously we needed more powerful and intelligent machines to assist. We started solving real world problems and at times break our backs to make the machine understand our request. Size and Complexity of the code we write was directly proportionate to the complexity of the program. Large code written to solve particular set of problems are called Software (One which run on the Hardware, physical machine).

Problems around us, where big and very much from the real world!!!
Problems, needed real world thoughts and solutions. Real world is full of objects and their solutions is also related with it. Communicating the real world issue to machine was a complex thing to do, output entirely depends on how well we describe issue to machine. 

Bigger problems, we can achive it by braking down the problem and take a step by step approach towards solution. First form of break down happened in the form of Procedure (function). 

We started doing `structured approach` in programming, which is about decomposition. Problems were boken down into smaller ones and started resolving one by one. These `procedure` have specific, defined input and provide output in defined format. Extended the break down to the level of Modules, one Modules for one operation and gradually they helped in reuse of code. Modules were written for each type of requirement and started calling them as function calls.

More and more `procedure` (functions) where created, solutions became complicated and hard to maintain. Functions, sub functions, sub sub functions....more over not representing real world entities.

Structured programming have following problem : 
* Decomposition by functions 
  Fucntional decomposition defines structure and boundary, Fuction couldn't handle the security contraints of the data handled. (Functions cannot determine the access privillege of Data getting handled.)
* Functions cannot hold state, most system decisions are taken on the state of the entity.
  (Consider a real world scenario where you say hello to one person, response will depend on the state
   or impact of his previous interaction. If you are calling a function, it will process the request 
   and always give same type of response. There won't be any kind of impact of previous interactions. But most of our real life decisions are made or taken considering the state of the entity.)
* High memory requirement
  (Every time program A calls Program B, Program A current settings and state has to be stacked for processing Program B. While comming back from Program B, we need to restore the Program A)

Discussion heated up, on finding a new approach to solve the problem. An efficient approach to address all entities and their associated interaction in real world, realize it in program world. 

Mean while two programmers from the Norwegian Computing Center in Oslo, Norway had different thought. Ole-John Dahl and Kristen Nygaard at the Norwegian Computing Center in Oslo, Norway. Both working with ALGOL, knocked up an idea. 

Idea :- Local variable are stored in stack and Local variables of function are stored in special "function stack frame". Additionally there are option to declare functions which were also stored in stack. Ole-John and Kristen thought of moving "function stack frame" from stack to Heap. In this case, sub functions and calling functions can still operate on the function's local variables. We don't have to distroy function local variables every time we come out of function.

Idea actually removed the "Stacking" of the calling program. Calling program "A" and variables are active, called program "B" has access to operate on them. ALso, called program "B" can access the fields declared in "A". This opened up an idea of writing program by defining feilds and function acting upon the fields together. This collection of fields and function is called an `OBJECT`.

> Things to think on:
> OK, we can have variables and called function together in memory, Also those functions can access variables.
> What is that we are achieving by clubing Variables and Functions with access to the variables defined with it?

# Lets define a real world Object....
```
OBJECT - Any thing that has state and exhibit behavior
```

How do you represent `OBJECT` in digital world? </br>
By defining state as attributes and behavior as function, this definition is called `CLASS`. Coding solutions by defining `CLASS`, creating `OBJECT` and controlling interaction between the `OBJECTs` are called Object Oriented programing.

Now that we learned little bit of history and the idea to create "OBJECT", let's take our next step....

## Object Oriented Programming
Let's start again by asking with question...
```
What is Object Oriented Programming?
```

Just refer to what Wikipedia has to say...

```
Object-oriented programming is a programming paradigm based on the concept
of "objects", which can contain data, in the form of fields, and code, in
the form of procedures. A feature of objects is an object's procedures that
can access and often modify the data fields of the object with which they
are  associated.                                                                             
                                                          - Wikipedia
```
yeah, I got it. To understand this, we need to start our journey. 

Hope we asnwered two question.</br>
why we code? </br>
why we code like this?
