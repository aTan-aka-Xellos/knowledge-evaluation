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
* Usually talking about the "worst case"


Types of complexity:
* Constant Time: O(1)
* Linear Time: O(n)
* Logarithmic Time: O(log n)
* Quadratic Time: O(n^2)
* Cubic time O(n^3)	
* Exponential time O(2^n)
* Factorial time O(n!)

#### Some examples:  
![algo_complexity](files/algo_complexity.jpg)

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

### [Bubble sort](https://www.geeksforgeeks.org/bubble-sort)
Based on the idea of repeatedly comparing pairs of adjacent elements and then swapping their positions if they exist in the wrong order.  
### [Merge sort](https://www.geeksforgeeks.org/merge-sort)
Is a divide-and-conquer algorithm based on the idea of breaking down a list into several sub-lists until each sublist consists of a single element and merging those sublists in a manner that results into a sorted list.  

Idea:
* Divide the unsorted list into  sublists, each containing  element.
* Take adjacent pairs of two singleton lists and merge them to form a list of 2 elements.  will now convert into  lists of size 2.
* Repeat the process till a single sorted list of obtained.

While comparing two sublists for merging, the first element of both lists is taken into consideration. While sorting in ascending order, the element that is of a lesser value becomes a new element of the sorted list. This procedure is repeated until both the smaller sublists are empty and the new combined sublist comprises all the elements of both the sublists.  

### [Quick sort](https://www.geeksforgeeks.org/quick-sort)
Quick sort is based on the divide-and-conquer approach based on the idea of choosing one element as a pivot element and partitioning the array around it such that: Left side of pivot contains all the elements that are less than the pivot element Right side contains all elements greater than the pivot.  

It reduces the space complexity and removes the use of the auxiliary array that is used in merge sort. Selecting a random pivot in an array results in an improved time complexity in most of the cases.  


## Binary search algorithm	
Search a sorted array by repeatedly dividing the search interval in half. Begin with an interval covering the whole array. If the value of the search key is less than the item in the middle of the interval, narrow the interval to the lower half. Otherwise narrow it to the upper half. Repeatedly check until the value is found or the interval is empty.  

The idea of binary search is to use the information that the array is sorted and reduce the time complexity to O(Log n).  


## Tree structure(construction, traversal)



## Hash table(creating, collisions)


## Stack, queue, linked list(construction, understanding, usage)

