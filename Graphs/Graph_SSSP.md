


## Rule of thumb:
Unweighted → BFS
Weighted, non-negative → Dijkstra
Negative edges possible → Bellman–Ford

## Comparison Table
| Feature | BFS | Dijkstra | Bellman–Ford |
|----------|------|-----------|---------------|
| Shortest path type | Single-source | Single-source | Single-source |
| Edge weights | Only unweighted / equal weights | Weighted allowed | Weighted allowed |
| Negative weights | Not supported | Not supported | Supported |
| Directed graph | Works | Works | Works |
| Undirected graph | Works | Works | Works |
| Cycles allowed | Yes | Yes | Yes |
| Negative cycle handling | Not applicable | Fails | Detects & reports |
| Core data structure | Queue | Priority queue (min-heap) | Repeated edge relaxation |
| Time complexity | O(V + E) | O((V + E) log V) | O(V × E) |
| Typical use case | Unweighted shortest path | Weighted shortest path (no negative edges) | Graphs with negative edges |
