# Implementation: Linked Lists

Terminology:

**Linked List** - A data structure that contains nodes that links/points to the next node in the list.

**Singly** - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

**Doubly** - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

**Node** - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

**Next** - Each node contains a property called Next. This property contains the reference to the next node.

**Head** - The Head is a reference of type Node to the first node in a linked list.

**Current** - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

## Discussion by teaching something that you learned




## Big O: Analysis of Algorithm Efficiency

<https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html>

**Big O(oh)** notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

Running Time (also known as time efficiency / complexity)
The amount of time a function needs to complete.

Memory Space (also known as space efficiency / complexity)
The amount of memory resources a function uses to store data and instructions.

**Importance**
Big O’s role in algorithm efficiency is to describe the **Worst Case** of efficiency an algorithm can have in performing it’s job. It specifically looks at the factors mentioned above, which we often refer to as Space and Time. In order to analyze these limiting factors, we should consider 4 Key Areas for analysis

Input Size
Units of Measurement
Orders of Growth
Best Case, Worst Case, and Average Case

*We can describe overall efficiency by using the input size n and measuring the overall Units of Space and Time required for the given input size n. As the value of n grows, the Order of Growth represents the increase in Running Time or Memory Space.


image.png

ALGORITHM FibonacciIndex(number n)

    if n <= 1
       return 1

    return FibonacciIndex(n - 1) + FibonacciIndex(n - 2);

Asymptotic Notations

Big O(oh): This notation describes the Worst Case for an algorithm. The Order of Growth used represents the upper bounds of Time and Space.

Big Omega: This notation describes the Best Case for a given algorithm. The Order of Growth used represents the lower bounds of Time and Space.

Big Theta: This notation describes the Average Case. The Order of Growth used represents the tight bound of Time and Space.

We use the term tight since, in order to predict a “typical” input, we need an idea of what makes our function perform better or worse. Tight means that the upper and lower can both be set by this Order of Growth.

<https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/EfficiencyNotations.png>

## Linked Lists

<https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html>

## What’s a Linked List, Anyway pt1

<https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d>

## What’s a Linked List, Anyway pt2

<https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996>