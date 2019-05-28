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

In computer programming, cohesion refers to the degree to which the elements inside a module belong together. In one sense, it is a measure of the strength of relationship between the methods and data of a class and some unifying purpose or concept served by that class. In another sense, it is a measure of the strength of relationship between the class’s methods and data themselves.

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


## [Architectural Patterns: MVC](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)

https://blogs.msdn.microsoft.com/erwinvandervalk/2009/08/14/the-difference-between-model-view-viewmodel-and-other-separated-presentation-patterns/  
Translation:  
https://habr.com/ru/company/mobileup/blog/313538/  

MVC architectural pattern follows an elementary idea – we must separate the responsibilities in any application on the following basis:

* Model: Handles data and business logic.
* View: Presents the data to the user whenever asked for.
* Controller: Entertains user requests and fetch necessary resources.

What are those Models, Views and Controllers:

### Model 
The model typically is the data of your application and the logic to retrieve and persist that data. Often, this is a domain model that can be based on a database or the results from web services. In some cases, that domain model maps perfectly to what you see on the screen, but in other cases it has to be adapted, aggregated or extended to be usable.  

### View 
The View was responsible for drawing the UI on the screen. Without windows or controls, that meant drawing, boxes, buttons, input fields, etc on the screen. The View can also monitor the model and display any data in it or update itself if the data changes.

### Controller 
The controller is responsible for handling the User Input and then updating the Model or the View. So if the user is interacts with the application, IE: presses a button on the keyboard, moves the mouse, the controller is notified of that user gesture and decides what to do with it. Maybe it should update the view, maybe it should update the model.   

Goals of MVC:
* Simultaneous development
* Code reuse

Advantages:
* Simultaneous development
* High cohesion 
* Loose coupling
* Ease of modification
* Multiple views for a model
Disadvantages:
* Code navigability
* Multi-artifact consistency
* Excessive boilerplate
* Pronounced learning curve

Variations:
* Model View Presenter 
* Presentation Model (Martin Fowler)
* Model View ViewModel (databinding)

## Architectural Patterns: IoC


## SOLID principles


## [Anti-patterns](https://en.wikipedia.org/wiki/Anti-pattern)

An anti-pattern is a common response to a recurring problem that is usually ineffective and risks being highly counterproductive.

Software design:
* Big ball of mud: A system with no recognizable structure
* Gold plating: Continuing to work on a task or project well past the point at which extra effort is not adding value
* Abstraction inversion: Not exposing implemented functionality required by callers of a function/method/constructor, so that the calling code awkwardly re-implements the same functionality in terms of those calls
* Interface bloat: Making an interface so powerful that it is extremely difficult to implement
* Inner-platform effect: A system so customizable as to become a poor replica of the software development platform

Object-oriented programming:
* Circular dependency: Introducing unnecessary direct or indirect mutual dependencies between objects or software modules
* Constant interface: Using interfaces to define constants
* God object: Concentrating too many functions in a single part of the design (class)
* Call super: Requiring subclasses to call a superclass's overridden method
* Circle-ellipse problem: Subtyping variable-types on the basis of value-subtypes
* Object cesspool: Reusing objects whose state does not conform to the (possibly implicit) contract for re-use
* Poltergeists: Objects whose sole purpose is to pass information to another object
* Sequential coupling: A class that requires its methods to be called in a particular order
* Yo-yo problem: A structure (e.g., of inheritance) that is hard to understand due to excessive fragmentation

Programming:
* Accidental complexity: Programming tasks which could be eliminated with better tools
* Action at a distance: Unexpected interaction between widely separated parts of a system
* Boat anchor: Retaining a part of a system that no longer has any use
* Busy waiting: Consuming CPU while waiting for something to happen
* Caching failure: Forgetting to clear a cache that holds a negative result (error) after the error condition has been corrected
* Cargo cult programming: Using patterns and methods without understanding why
* Error hiding
* Hard code: Embedding assumptions about the environment of a system in its implementation
* Lasagna code: Programs whose structure consists of too many layers of inheritance
* Spaghetti code: Programs whose structure is barely comprehensible, especially because of misuse of code structures
* Magic numbers
* Magic strings
* Repeating yourself

Methodological:
* Copy and paste programming
* Every Fool Their Own Tool
* Golden hammer
* Improbability factor: Assuming that it is improbable that a known error will occur
* Reinventing the wheel 
* Premature optimization

Configuration management:
* Dependency hell

Organizational:
* Analysis paralysis
* Bleeding edge: Operating with cutting-edge technologies
* Cash cow: A profitable legacy product that often leads to complacency about new products
* Design by committee: The result of having many contributors to a design, but no unifying vision
* Micromanagement
* Mushroom management: Keeping employees "in the dark and fed manure"

Project management:
* Ninety-ninety rule: Tendency to underestimate the amount of time to complete a project when it is "nearly done"
* Death march: A project whose staff, while expecting it to fail, are compelled to continue, often with much overwork, by management which is in denial
* Overengineering: Spending resources making a project more robust and complex than is needed
* Scope creep: Uncontrolled changes or continuous growth in a project's scope, or adding new features to the project after the original requirements have been drafted and accepted
* Smoke and mirrors: Demonstrating unimplemented functions as if they were already implemented

