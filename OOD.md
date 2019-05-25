# [Design - OOD](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Design-OOD)  

__Qualified__


## Abstraction
Abstraction - Implementation hiding.  

Abstraction is providing a generalization.  
Its main goal is to handle complexity by hiding unnecessary details from the user. That enables the user to implement more complex logic on top of the provided abstraction without understanding or even thinking about all the hidden complexity.  
The process of abstraction in Java is used to hide certain details and only show the essential features of the object. In other words, it deals with the outside view of an object (interface).  

## Encapsulation
Encapsulation - Information hiding.  

Encapsulation is hiding the implementation details.  
Encapsulation refers to the state of objects - objects encapsulate their state and hide it from the outside; outside users of the class interact with it through its methods, but cannot access the classes state directly.  


## Inheritance vs. Aggregation
In the 'normal' cases a simple question is enough to find out if we need inheritance or aggregation.  

* If The new class is more or less as the original class. Use inheritance. The new class is now a subclass of the original class.  
* If the new class must have the original class. Use aggregation. The new class has now the original class as a member.

However, there is a big gray area. So we need several other tricks.  

*  If we have used inheritance (or we plan to use it) but we only use part of the interface, or we are forced to override a lot of functionality to keep the correlation logical. Then we have a big nasty smell that indicates that we had to use aggregation.
*  If we have used aggregation (or we plan to use it) but we find out we need to copy almost all of the functionality. Then we have a smell that points in the direction of inheritance.

## Modularity
Modules from Java 9  
Encapsulation is binding the data and behaviors together in a single unit. Also it is a language mechanism for restricting access to some components(this can be achieved by access modifiers like private,protected etc.)  

## Polymorphism
Ability to present the same interface for differing underlying forms (data types).  
Polymorphism is when you can treat an object as a generic version of something, but when you access it, the code determines which exact type it is and calls the associated code.  

## Types vs. Classes
A type is an interface.  
An object's implementation is defined by its class. 

An object's class defines how the object is implemented .The class defines object's internal state and the implementation of its operations.  

In contrast, an object's type only refers to its interface - a set of requests to which it can respond.  

An object can have many types, and objects of different classes can have the same type.  

## Abstraction Qualities (cohesion, coupling, etc)

https://atomicobject.com/resources/oo-programming/oo-quality 

* Coupling
How closely do classes rely on each other?  
Inheritance makes for strong coupling (generally a bad thing) 
but takes advantage of the re-use of an abstraction (generally a good thing).  

* Cohesion
How tied together are the state and behavior of a class?  
Does the abstraction model a cohesive, related, integrated thing in the problem space?  

* Sufficiency
Does the class capture enough of the details of the thing being modeled to be useful?  

* Completeness
Does the class capture all of the useful behavior of the thing being modeled to be re-usable?  
What about future users (reusers) of the class?  
How much more time does it take to provide completeness? Is it worth it?  

* Primitiveness
Do all the behaviors of the class satisfy the condition that they can only be implemented by accessing the state of the class directly?  
If a method can be written strictly in terms of other methods in the class, it isn't primitive.  


## Separation of concerns principle
Is a design principle for separating a computer program into distinct sections, so that each section addresses a separate concern.  

Separation of concerns as applied to three different perspectives of software architecture:
* Functions/Methods/Algorithms
* Things/Classes/Objects
* Modules/Components/Sub-systems/Packages

Why bother:
* At the level of Functions, they write Spaghetti Code
* At the level of Things, they write God Classes/Objects
* At the level of the entire architecture of their systems, they write Monoliths

## Single responsibility principle
The single responsibility principle is a computer programming principle that states that every module, class, or function should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class.  

Robert C. Martin expresses the principle as, "A class should have only one reason to change,"  


__Competent__

## GoF Design Patterns


## Architectural Patterns: Layered Architecture


## Architectural Patterns: MVC


## Architectural Patterns: IoC


## SOLID principles


## Anti-patterns
