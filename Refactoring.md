# [Construction - Refactoring](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Construction-Refactoring)

### Refactoring Concept (what/when/why)


### Smells Catalog and possible re-factorings

https://en.wikipedia.org/wiki/Code_smell

Сode smell is any characteristic in the source code of a program that possibly indicates a deeper problem.

Application-level smells:
* Duplicated code
* Contrived complexity: forced usage of overcomplicated design patterns where simpler design would suffice.
* Shotgun surgery: a single change needs to be applied to multiple classes at the same time.

Class-level smells:
* Large class, God object
* Feature envy: a class that uses methods of another class excessively.
* Inappropriate intimacy: a class that has dependencies on implementation details of another class.
* Refused bequest: a class that overrides a method of a base class in such a way that the contract of the base class is not honored by the derived class. See Liskov substitution principle.
* Lazy class / freeloader: a class that does too little.
* Cyclomatic complexity

Method-level smells:
* Too many parameters
* Long method
* Excessively long identifiers
* Excessively long line of code


### Moving Features Between Objects (basic)


### Move Method

### Move Field


### Organizing Data (basic)


### Encapsulate Field


### Encapsulate Collection


### Composing Methods (basic)


### Extract Method


### Inline Method


### Inline Temp

### Replace Temp with Query

### Split Temporary Variable

### Simplifying Conditional Expressions (basic)

### Decompose Conditional Expression

### Consolidate Conditional Expression

### Consolidate Duplicate Conditional Fragments

### Remove Control Flag

### Replace Conditional with Polymorphism


