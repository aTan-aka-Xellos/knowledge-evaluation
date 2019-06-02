# [Construction - Language - Java](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Construction-Language-Java)

## CL1 (Qualified)
__Qualification Requirements Overview:__  
Knowledge of java language specification and main packages is required.  


### Identifiers & JavaBeans


### Declare Classes


### Declare Interfaces


### Declare Class Members


### Reference Variable Casting


### Implementing an Interface


### Legal Return Types


### Constructors and Instantiation


### Statics

https://docs.oracle.com/javase/tutorial/java/IandI/override.html
https://www.geeksforgeeks.org/can-we-overload-or-override-static-methods-in-java
Static method cannot be overrided by child. It __hide__ method from parent and have it's own unique static method.

The distinction between hiding a static method and overriding an instance method has important implications:
* The version of the overridden instance method that gets invoked is the one in the subclass.
* The version of the hidden static method that gets invoked depends on whether it is invoked from the superclass or the subclass.

### Stack and Heap


### Literals, Assignments, and Variables


### Passing Variables into Methods


### Array Declaration, Construction, and Initialization


### Java Operators


### if and switch Statements


### Loops and Iterators

### Handling Exceptions


### Common Exceptions and Errors


### String, StringBuilder, and StringBuffer


### Using the javac and java Commands


### String literals in switch statements


### Underscores in literals to improve code readability


### try-with-resources block and exception handling


### Catching multiple exception types


### Rethrowing exceptions in Java 7


### Using the diamond operator for constructor type inference


### Using the @SafeVarargs annotation


## Java 8 features 


### [Default and Static Methods](https://docs.oracle.com/javase/tutorial/java/IandI/defaultmethods.html)

https://www.geeksforgeeks.org/default-methods-java  

If a new method is to be added in an interface, then its implementation code has to be provided in the class implementing the same interface. To overcome this issue, Java 8 has introduced the concept of default methods which allow the interfaces to have methods with implementation without affecting the classes that implement the interface.  

The default methods were introduced to provide backward compatibility so that existing intefaces can use the lambda expressions without implementing the methods in the implementation class. Default methods are also known as __defender methods__ or __virtual extension methods.__

In case both the implemented interfaces contain deafult methods with same method signature, the implementing class should explicitly specify which default method is to be used or it should override the default method.  

Important Points:
* Interfaces can have default methods with implementation from java 8 onwards.
* Interfaces can have static methods as well similar to static method of classes.
* Default methods were introduced to provide backward compatibility for old interfaces so that they can have new methods without effecting existing code.


https://www.geeksforgeeks.org/static-method-in-interface-in-java
Unlike other methods in Interface, these static methods contain the complete definition of the function and since the definition is complete and the method is static, therefore these methods cannot be overridden or changed in the implementation class.  

Similar to Default Method in Interface, the static method in an interface can be defined in the interface, but these methods cannot be overridden in Implementation Classes.  

To use a static method, Interface name should be instantiated with it, as it is __a part of the Interface only.__  


## Java 10 features

### Local-Variable Type Inference

### Time-Based release versioning


## CL2 (Competent)

__Qualification Requirements Overview:__  
Capability to pass Oracle Certified Professional Java Programmer Exam.

### Using Wrapper Classes and Boxing

### Overloading


### Garbage Collection


### Working with the Assertion Mechanism


### File Navigation and I/O


### Dates, Numbers, and Currency


### Parsing,Tokenizing, and Formatting


### Overriding hashCode() and equals()

### [Collections](https://docs.oracle.com/javase/tutorial/collections/TOC.html)

https://docs.oracle.com/javase/8/docs/api/java/util/Collection.html

Collections extended by List (LinkedList, ArrayList, Vector), Queue (LinkedList, PriorityQueue) and Set (HashSet, TreeSet, LinkedHashSet).  
![collections](https://3.bp.blogspot.com/-LUCDWSG5qXE/Uy_ee5bIR5I/AAAAAAAAAZA/oY1hR_1fcwk/s1600/Java+collection+cheat+sheet.PNG)


![performance](http://i.imgur.com/gb66dmb.png)

__Some highlights:__

The java.util.concurrent package contains several collections implementations, which are thread-safe but not governed by a single exclusion lock.  

The Collections class (as opposed to the Collection interface), provides static methods that operate on or return collections, which are known as Wrapper implementations.  



#### Interfaces  
* The first tree starts with the Collection interface, which provides for the basic functionality used by all collections, such as add and remove methods. Its subinterfaces — Set, List, and Queue — provide for more specialized collections.
The Set interface does not allow duplicate elements. This can be useful for storing collections such as a deck of cards or student records. The Set interface has a subinterface, SortedSet, that provides for ordering of elements in the set.

* The List interface provides for an ordered collection, for situations in which you need precise control over where each element is inserted. You can retrieve elements from a List by their exact position.

* The Queue interface enables additional insertion, extraction, and inspection operations. Elements in a Queue are typically ordered in on a FIFO basis.

* The Deque interface enables insertion, deletion, and inspection operations at both the ends. Elements in a Deque can be used in both LIFO and FIFO.

* The second tree starts with the Map interface, which maps keys and values similar to a Hashtable.

* Map's subinterface, SortedMap, maintains its key-value pairs in ascending order or in an order specified by a Comparator.

#### Implementation
* For the Set interface, HashSet is the most commonly used implementation.
* For the List interface, ArrayList is the most commonly used implementation.
* For the Map interface, HashMap is the most commonly used implementation.
* For the Queue interface, LinkedList is the most commonly used implementation.
* For the Deque interface, ArrayDeque is the most commonly used implementation.


## [Map](https://docs.oracle.com/javase/tutorial/collections/interfaces/map.html)
HashTable, HashMap, TreeMap, LinkedHashMap.  
https://habr.com/ru/post/128017  
![Map](https://habrastorage.org/storage1/4e3e57f4/aaa0b3fd/c697a3d8/5108f778.png)

A Map is an object that maps keys to values. A map cannot contain duplicate keys: Each key can map to at most one value. It models the mathematical function abstraction. The Map interface includes methods for basic operations (such as put, get, remove, containsKey, containsValue, size, and empty), bulk operations (such as putAll and clear), and collection views (such as keySet, entrySet, and values).  

The Java platform contains three general-purpose Map implementations: HashMap, TreeMap, and LinkedHashMap.  

### HashMap

#### [Collisions](https://www.geeksforgeeks.org/internal-working-of-hashmap-java)

In case of hash collision entry objects are stored as a node in a linked-list and equals() method is used to compare keys. That comparison to find the correct key with in a linked-list is a linear operation so in a worst case scenario the complexity becomes O(n).
To address this issue, Java 8 hash elements use balanced trees instead of linked lists after a certain threshold is reached.

#### [get() with collisions](https://www.geeksforgeeks.org/internal-working-of-hashmap-java)
Steps:

1. Calculate hash code of Key {“sachin”}. It will be generated as 115.
2. Calculate index by using index method it will be 3.
3. Go to index 3 of array and compare first element’s key with given key. If both are equals then return the value, otherwise check for next element if it exists.



### Using the Collections Framework

### Generic Types

### JAR Files


### Static Imports

### Serialization

### Inner Classes


### Method-Local Inner Classes


### Anonymous Inner Classes


### Static Nested Classes


### Reflection


### Annotations


### Locating Files and Directories Using Paths


### Obtaining and Managing Files and Directories


### Working with Filesystems in Java 7


### Stream IO in Java 7


## Java 8 features

### Lambdas and Functional Interfaces

### [Method references](https://docs.oracle.com/javase/tutorial/java/javaOO/methodreferences.html)
The method reference is semantically the same as the lambda expression.  


![MethodReference](files/MethodReference.jpg)

Lambda:  
Arrays.sort(rosterAsArray,
    (a, b) -> Person.compareByAge(a, b)
);

Because this lambda expression invokes an existing method, you can use a method reference instead of a lambda expression:  

Arrays.sort(rosterAsArray, Person::compareByAge);

Each has the following characteristics:  
* Its formal parameter list is copied from Comparator<Person>.compare, which is (Person, Person).
* Its body calls the method Person.compareByAge.
  


### Stream API

### Method parameter reflection

### New Date API

## Java 9 features

### Java Platform Module System
