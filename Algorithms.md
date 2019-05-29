# [Algorithms](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Algorithms)

__Qualification Requirements Overview:__  
Base algorithm knowledge that should be sufficient to implement basic tasks with necessary performance.


## Algorithms complexity (understanding, big O notation, complexity of common algorithms)

How quickly it grows relative to the input, as the input gets arbitrarily large.  

Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity.  

In computer science, big O notation is used to classify algorithms according to how their running time or space requirements grow as the input size grows.  

Some rules:
* Drop the constants.
* Drop the less significant terms

Types of complexity:
* Constant Time: O(1)
* Linear Time: O(n)
* Logarithmic Time: O(log n)
* Quadratic Time: O(n^2)
* Cubic time O(n^3)	
* Exponential time O(2^n)
* Factorial time O(n!)

#### Some examples:  
![algo_complexity](algo_complexity.jpg)

### Analysis of Algorithms
The term analysis of algorithms is used to describe approaches to the study of the performance of algorithms. In this course we will perform the following types of analysis:
* the worst-case runtime complexity of the algorithm is the function defined by the maximum number of steps taken on any instance of size a.
* the best-case runtime complexity of the algorithm is the function defined by the minimum number of steps taken on any instance of size a.
* the average case runtime complexity of the algorithm is the function defined by an average number of steps taken on any instance of size a.
*  the amortized runtime complexity of the algorithm is the function defined by a sequence of operations applied to the input of size a and averaged over time.

### NP-complete
A problem is NP-complete when it can be solved by a restricted class of brute force search algorithms and it can be used to simulate any other problem with a similar algorithm.  

### Polynomial time
An algorithm is said to be of polynomial time if its running time is upper bounded by a polynomial expression in the size of the input for the algorithm, i.e., T(n) = O(nk) for some positive constant k.  

## Array sorting methods(bubble sort, quick sort, merge sort)


## Tree structure(construction, traversal)


## Binary search algorithm	


## Hash table(creating, collisions)


## Stack, queue, linked list(construction, understanding, usage)

