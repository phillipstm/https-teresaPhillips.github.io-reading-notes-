# Graphs

<https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html>

Here is some common terminology used when working with Graphs:

**Vertex**- A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
**Edge**- An edge is a connection between two nodes.
**Neighbor**- The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
**Degree** The degree of a vertex is the number of edges connected to that vertex.

## Directed vs Undirected

An _Undirected Graph_ is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

A _Directed Graph_ also called a Digraph is a graph where every edge is directed.

## Complete vs Connected vs Disconnected

A _complete graph_is when all nodes are connected to all other nodes.

A _connected graph_ is graph that has all of vertices/nodes have at least one edge.

A _disconnected graph_ is a graph where some vertices may not have edges.

## Acyclic vs Cyclic

**Acyclic Graph**
An acyclic graph is a directed graph without cycles.

A cycle is when a node can be traversed through and potentially end up back at itself.

A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.

**Cyclic Graphs**
A Cyclic graph is a graph that has cycles.

A cycle is defined as a path of a positive length that starts and ends at the same vertex.

**Adjacency Matrix**
An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix.

a sparse graph is when there are very few connections. a dense graph is when there are many connections

Within an adjacency matrix, an undirected graph will always be symmetric. This is not the case for a directed graph.

**Adjacency List**
An adjacency list is the most common way to represent graphs.

An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

Adjacency lists make it easy to view if one vertices connects to another.

1.We can visually see that we are working with a collection of some sort. The visual is depicting a Linked List, but you could easily make it an array of arrays if you’d like.
2.Each index or node (depending on the data structure you choose to represent the adjacency list) will be a vertex within the graph.
3.Every time you add an edge, you will find the appropriate vertices in the data structure and add it to the appropriate location.

## Traversals

**Breadth First**
In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. 
The breadth first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. 
Traversing a graph that has cycles will result in an **infinite loop….**this is bad. To prevent such behavior, we need to have some way to keep track of whether a vertex has been “visited” before. 
Upon each visit, we’ll add the previously-unvisited vertex to a visited set, so we know not to visit it again as traversal continues.

**algorithm breadth first traversal**
1.Enqueue the declared start node into the Queue.
2.Create a loop that will run while the node still has nodes present.
3.Dequeue the first node from the queue
4.If the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.

ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()

    breadth.Enqueue(vertex)
    visited.Add(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)

    return nodes;

**Depth First**
In a depth first traversal, our approach is a bit different than the approach used for breadth first.

While the breadth first traversal uses a Queue to visit all children at a given level, the depth first traversal uses a Stack to visit all children of a given subtree. 
(This differs from our approach to tree traversal, where we visit nodes via recursive calls. Recursive calls use a call stack internally.)

The **algorithm for a depth first traversal** is as follows:

1.Push the root node into the Stack and mark as visited.
2.Start a while loop that runs as long as the stack is not empty.
3.Pop the top node off of the stack and check its neighbors.
4.If a neighbor hasn’t been visited, push it onto the stack and mark as visited.
5.Repeat until the stack is empty.

## Real World Uses of Graphs

Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:

GPS and Mapping
Driving Directions
Social Networks
Airline Traffic
Netflix uses graphs for suggestions of products
