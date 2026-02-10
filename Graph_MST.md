
## Spanning Tree
A spanning tree is a connected subgraph in an undirected graph where all vertices are connected with the **minimum number of edges**.

## Minimum Spanning Tree
A minimum spanning tree is a spanning tree with the minimum possible total edge weight in a “weighted undirected graph”

## Cut Property
In Graph theory, a “cut” is a partition of vertices in a “graph” into two disjoint subsets.
More formally, according to Wikipedia, the “cut property” refers to:

> For any cut C of the graph, if the weight of an edge E in the cut-set of C is strictly smaller than the weights of all other edges of the cut-set of C, then this edge belongs to all MSTs of the graph

### Kruskal's Alogrithm (Greedy)
“Kruskal’s algorithm” is an algorithm to construct a “minimum spanning tree” of a “weighted undirected graph”.

Sort the edges by weight. Include the first **N-1** minimimum weighted edges such that it does not lead to a cycle.


### Prim's Algorithm
Idea: Start with any vertex. From that find the cost(weight) to reach the adjacent vertex
##### Using Heap:
 Add all the vertices which are not yet in MST in heap which is sorted by weight to reach that node. Take the next node in the heap. Include the first **N-1** minimimum weighted edges such that it does not lead to a cycle.

#### Optimized:
Keep an  array[V]  to maintain the cost to reach a node. For the current vertex, (which is in MST), find the next vertex which has the minimum cost to reach and which does not cause cycle. Select that node, and update neighbours array[].


Q) https://leetcode.com/problems/min-cost-to-connect-all-points
  - Solve with Both Kruskal and Prim( Heap and optimized solns)
  - While calculating TC, worst case is when each node is connected directly to another node.

