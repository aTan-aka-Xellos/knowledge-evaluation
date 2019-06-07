# [Construction - Concurrency - Java](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Construction-Concurrency-Java)

## CL1 (Qualified)
__Qualification Requirements Overview:__  
Knowledge of basic concepts of concurrency and thread management.


### Defining, Instantiating, and Starting Threads
The formal definition of a thread is, A thread is a basic processing unit to which an operating system allocates processor time, and more than one thread can be executing code inside a process. A thread is sometimes called a lightweight process or an execution context.  
When you create a Java thread you can give it a name.  

Create thread:

#### You can implement the Runnable interface.
Inside run( ), you will define the code that constitutes the new thread. It is important to understand that run( ) can call other methods, use other classes, and declare variables, just like the main thread can. The only difference is that run( ) establishes the entry point for another, concurrent thread of execution within your program. This thread will end when run( ) returns.
```
MyRunnableThreadmyRunnable = new MyRunnableThread ();
Thread thread = new Thread(myRunnable);
```
or lambda approach:
```Runnable runnable = () -> { System.out.println("Lambda Runnable running"); };```


#### You can extend the Thread class
The limitation with this approach (besides being a poor design choice in most cases) is that if you extend Thread, you can't extend anything else. And it's not as if you really need that inherited Thread class behavior because in order to use a thread you'll need to instantiate one anyway.
```
MyThread thread = new MyThread();
```

#### Starting a Thread

```t.start();```


### Thread States and Transitions

https://www.geeksforgeeks.org/lifecycle-and-states-of-a-thread-in-java

* New
* Runnable
* Blocked
* Waiting
* Timed Waiting
* Terminated

### Thread Interaction

The Object class has three methods, wait(), notify(), and notifyAll()  

They must be called from within a synchronized context. A thread can't invoke a wait or notify method on an object unless it owns that object's lock.  

* wait() - It tells the calling thread to give up the lock and go to sleep until some other thread enters the same monitor and calls notify()  
* notify() - It wakes up one single thread that called wait() on the same object. It should be noted that calling notify() does not actually give up a lock on a resource.
* notifyAll() - It wakes up all the threads that called wait() on the same object.

* join(): It will put the current thread on wait until the thread on which it is called is dead. 

Java Thread join method can be used to pause the current thread execution until unless the specified thread is dead.  


### Synchronizing Code with synchronized keyword 


### The Volatile Keyword


### Race conditions 


### Nested Locks in Java 


### Using wait(), notify(), and notifyAll() for synchronization 


### Using of conditional variables for synchronization


