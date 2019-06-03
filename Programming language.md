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

Overriding default method in class (without keyword default and with public access lvl) is allowed.

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

### [Functional interface](https://www.geeksforgeeks.org/functional-interfaces-java)

A functional interface is an interface that contains only one abstract method. They can have only one functionality to exhibit. From Java 8 onwards, lambda expressions can be used to represent the instance of a functional interface. A functional interface can have any number of default methods. Runnable, ActionListener, Comparable are some of the examples of functional interfaces.  

#### @FunctionalInterface Annotation
@FunctionalInterface annotation is used to ensure that the functional interface can’t have more than one abstract method. In case more than one abstract methods are present, the compiler flags an ‘Unexpected @FunctionalInterface annotation’ message. However, it is not mandatory to use this annotation.  

#### java.util.function Package
The java.util.function package in Java 8 contains many builtin functional interfaces like:  


##### Supplier
Represents a supplier of results.  
There is no requirement that a new or distinct result be returned each time the supplier is invoked.  
It is typically used for lazy generation of values.  
```
public interface Supplier<T> {
    T get();
}
```

##### Consumer  
Represents an operation that accepts a single input argument and returns no result. 
Unlike most other functional interfaces, Consumer is expected to operate via side-effects.  
```
@FunctionalInterface
public interface Consumer<T> {
    void accept(T t);
}
```

##### Predicate 
In mathematical logic, a predicate is a function that receives a value and returns a boolean value.  
The Predicate interface has an abstract method test which gives a Boolean value as a result for the specified argument.  
The Predicate functional interface is a specialization of a Function that receives a generified value and returns a boolean.  
A typical use case of the Predicate lambda is to filter a collection of values.  
```
public Predicate  
{  
   public boolean test(T  t);
 }
```

##### Function 
Represents a function that accepts one argument and produces a result.  
The Function interface has an abstract method apply which takes argument of type T and returns a result of type R.   
Applies this function to the given argument.  
Its prototype is public interface Function.
```
{
   public R apply(T t);
}
```

### [Lambdas](https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html)


Lambda expressions enable you to treat functionality as method argument, or code as data. 

A lambda expression consists of the following:
* A comma-separated list of formal parameters enclosed in parentheses. You can omit the data type of the parameters in a lambda expression. In addition, you can omit the parentheses if there is only one parameter. 
* The arrow token, ->
* A body, which consists of a single expression or a statement block. If you specify a single expression, then the Java runtime evaluates the expression and then returns its value. A return statement is not an expression; in a lambda expression, you must enclose statements in braces ({}). However, you do not have to enclose a void method invocation in braces.

#### Accessing Local Variables of the Enclosing Scope

Lambda expressions are lexically scoped. This means that they do not inherit any names from a supertype or introduce a new level of scoping. Declarations in a lambda expression are interpreted just as they are in the enclosing environment.  

Lambda expression can only access local variables and parameters of the enclosing block that are final or effectively final.  
A variable or parameter whose value is never changed after it is initialized is effectively final.  
Simplest way to explain "effectively final" is to imagine adding the final modifier to a variable declaration. If, with this change, the program continues to behave in the same way, both at compile time and at run time, then that variable is effectively final.  

To determine the type of a lambda expression, the Java compiler uses the target type of the context or situation in which the lambda expression was found.  


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
  


### [Stream API](https://docs.oracle.com/javase/tutorial/collections/streams/index.html)

A __pipeline__ is a sequence of aggregate operations.  
A pipeline contains the following components:
* A source
* Zero or more intermediate operations
* A terminal operation

#### Differences Between Aggregate Operations and Iterators
Aggregate operations, like forEach, appear to be like iterators. However, they have several fundamental differences:
* They use internal iteration: Aggregate operations do not contain a method like next to instruct them to process the next element of the collection.
* They process elements from a stream: Aggregate operations process elements from a stream, not directly from a collection.
* They support behavior as parameters: You can specify lambda expressions as parameters for most aggregate operations. This enables you to customize the behavior of a particular aggregate operation.

#### Laziness
All intermediate operations are lazy. An expression, method, or algorithm is lazy if its value is evaluated only when it is required.

#### Interference
Lambda expressions in stream operations should not interfere. Interference occurs when the source of a stream is modified while a pipeline processes the stream. 

#### Stateful Lambda Expressions
Avoid using stateful lambda expressions as parameters in stream operations. A stateful lambda expression is one whose result depends on any state that might change during the execution of a pipeline.

#### Some methods
https://habr.com/ru/company/luxoft/blog/270383

Intermediate Operations:

##### map 
The map method is used to map the items in the collection to other objects according to the Predicate passed as argument

##### filter 
The filter method is used to select elements as per the Predicate passed as argument.

##### sorted
The sorted method is used to sort the stream.

##### distinct
##### peek
##### limit
##### skip

Terminal Operations:

##### forEach
The forEach method is used to iterate through every element of the stream.  

##### reduce
Method is a general-purpose reduction operation.
The reduce operation can takes two arguments:
* identity: The identity element is both the initial value of the reduction and the default result if there are no elements in the stream.
* accumulator: The accumulator function takes two parameters: a partial result of the reduction and the next element of the stream.

##### collect
The collect method modifies, or mutates, an existing value.  
The collect method is used to return the result of the intermediate operations performed on the stream.

##### findFirst 
Return first element of the stream (return Optional)

##### findAny 
Return any element of the stream (return Optional)

##### count
Return number of elements in the stream.

##### anyMatch
Return true if the condition is true for at least one element of the stream

##### allMatch

##### min

##### max

##### toArray


#### Parallelism
Parallel computing involves dividing a problem into subproblems, solving those problems simultaneously (in parallel, with each subproblem running in a separate thread), and then combining the results of the solutions to the subproblems.   

You can execute streams in serial or in parallel. When a stream executes in parallel, the Java runtime partitions the stream into multiple substreams. Aggregate operations iterate over and process these substreams in parallel and then combine the results.  



### Method parameter reflection

### New Date API

## Java 9 features

### Java Platform Module System
