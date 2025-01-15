```mermaid
graph TD
  A[What is the nature of the problem?] --> B{Is the input sorted or can it be sorted?}
  B --> |Yes| C[Binary Search - Find specific element]
  B --> |Yes| D[Two Pointers - Find pairs/triplets]
  B --> |Yes| E[Sliding Window - Max/Min subarray or substring]
  B --> |No| F{Permutations, combinations, or subsets?}
  F --> |Yes| G[Backtracking - Recursive solution generation]
  F --> |No| H{Is it a graph or grid traversal problem?}
  
  H --> |Yes| I{Shortest path problem?}
  I --> |Yes, Weighted graph| J[Dijkstra's Algorithm or A*]
  I --> |Yes, Unweighted graph| K[Breadth-First Search (BFS)]
  H --> |Yes| L{Cycle detection or connectivity?}
  L --> M[Union-Find or Depth-First Search (DFS)]
  H --> |Yes| N{Topological ordering with dependencies?}
  N --> O[Topological Sort (Kahn's or DFS-based)]
  
  H --> |No| P{Does the problem involve trees?}
  P --> |Yes| Q[Tree Traversal (DFS - Preorder, Inorder, Postorder)]
  P --> |Yes| R[BFS for Level-Order Traversal]
  P --> |Yes| S[Lowest Common Ancestor - DFS/Recursion]
  
  P --> |No| T{Overlapping subproblems?}
  T --> |Yes| U[Dynamic Programming (DP)]
  U --> V[Top-Down Memoization or Bottom-Up Tabulation]
  
  T --> |No| W{Interval processing?}
  W --> |Yes| X[Sort and Merge Intervals]
  W --> |Yes| Y[Sweep-Line Technique for Overlaps]
  
  W --> |No| Z{Linked List problem?}
  Z --> |Yes| AA[Fast & Slow Pointers - Cycle Detection]
  Z --> |Yes| AB[Find Middle Element with Fast & Slow Pointers]
  
  Z --> |No| AC{Finding k largest/smallest elements?}
  AC --> AD[Heap (Min-Heap or Max-Heap)]
  
  AC --> |No| AE{Counting or matching efficiently?}
  AE --> AF[Hash Map or Set]
```
