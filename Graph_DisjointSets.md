
## Disjoint Set
Motivation:
- The primary use of disjoint sets is to address the connectivity between the components of a network.
- Answers the question: In a Graph with "Disjoint" components,
   - Is Vertex A connected to B?
   - How many Disjoint Components are there?
   -  Does Vertex A and B share "Common Ancestor"?
   - https://leetcode.com/problems/count-unreachable-pairs-of-nodes-in-an-undirected-graph/description/
- Implementation
  - Find function: The find function finds the root node of a given vertex.
  - Union function: unions two vertices and makes their root nodes the same.
  - Quick Find: TC of Find: O(1) , Union: O(N) , SC - O(N)
      - Instead os Storing the parent index, directly store the root index. This way find becomes O(1). But while doing Union, addition step is required to update the Root of all nodes in one of the compoenent. This can be done by traversing the array and updating nodes that have matching root.
  - Quick Union : Find: O(N) , Union: O(N) , SC - O(N)
      - Lazy approach : In Union operation, only one entry's "root" is changed.
      - Think why O(N) for both (and not O(height))
