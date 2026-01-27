
## Spanning Tree
A spanning tree is a connected subgraph in an undirected graph where all vertices are connected with the **minimum number of edges**.

## Minimum Spanning Tree
A minimum spanning tree is a spanning tree with the minimum possible total edge weight in a “weighted undirected graph”

## Cut Property
In Graph theory, a “cut” is a partition of vertices in a “graph” into two disjoint subsets.
More formally, according to Wikipedia, the “cut property” refers to:

> For any cut C of the graph, if the weight of an edge E in the cut-set of C is strictly smaller than the weights of all other edges of the cut-set of C, then this edge belongs to all MSTs of the graph

## Kruskal's Alogrithm (Greedy)
“Kruskal’s algorithm” is an algorithm to construct a “minimum spanning tree” of a “weighted undirected graph”.

Sort the edges by weight. Include the first **N-1** minimimum weighted edges such that it does not lead to a cycle
TC: O(E.logE)

