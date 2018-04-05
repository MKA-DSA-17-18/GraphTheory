# GraphTheory Notes
## Terms
* Graph
  * a graph is a triple consisting of vertex set V(G), an edge set E(G) and a relation that associateds the two vertices with each edge. The vertices associated with each edge are called endpoints
  
* Vertex
  * fundamental piece of the graph

* Edge
  * connects verticies
  
* Loop
  * edge with just one endpoint
  
* mulitple edge
  * edge that shares verticies with another edge
  
* simple graph
  * a graph with no loops or multi-edges

* adjacent verticies
  * verticies connected by an edge
 
* Walk 
  * set of verticies that give directions from one vertex to another
 
* Path
  * a walk that touches a given vertex once
  
* Trail
  * a walk that doesn't pass over a given edge more than once

* Circuit
  * a trail that starts and ends at the same vertex
  
* cycle
  * walk that starts and ends in the same place
  
* Connected graph 
  * there exists a walk between any two points
  
* Disconnected graph 
  * a walk may not exist between any two points 
 
* Cyclic graph
  * a graph that contains a cycle
 
* Eulerian trail
  * a trail in a graph that contains all edges
  
* Eulerian Circuit
  * a circuit that contains all the edges
   
## Representing Graphs
  
### Adjacency Matrices
  * a matrix that displays which vertices are connected by an edge represented by 1s and 0s
  * if it's directed it's row to column
  * if its undirected it will be symmetrical over the left diagonal \
### Adjacency Lists
  * list of each vertex and all nodes it is connected to
  * useful for topological sort
  * have in degree version and out degree version


## Algorithms
### Topological Sort
  * a graph theory sorting algorithm in which we use an adjacency list starting with the node with a null input degree, removing the node with null input from all the adjacency lists, then repeat for next null input degree vertex
  * if you pick any two vertices, they will appear sorted in that order
  * has to be a directed acyclical graph
### Shortest Path Problem 
  * finding shortest possible path for one point to another
  * find paths from one vertex to every other vertex at the same time because it has the same big O as finding the path from 1 to 1



#### Dijkstra's Algorithm
  * start with a vertex, set it as known (and remove from set of unknowns), then update the distances to its unknown neighbors, find next smallest distance connecting to another unknown and repeat
### Minimum Spanning Tree
  * to find lowest cost that makes the entire graph connected as a tree
  * no cycles
#### Prim's Algorithm
  * start off at any vertex, pick least cost edge going out, from any known vertices pick next least cost edge, repeat
#### Kruskals Algorithm
  * list all edge costs, start from beginning and choose them in order from least to greatest while avoiding cycles
