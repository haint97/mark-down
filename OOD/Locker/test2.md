```mermaid
graph TD
    A[Identify Problem Type] --> B1{Is input sorted?}
    B1 -->|Yes| C1[Binary Search or Two Pointers]
    B1 -->|No| B2{Is it permutations/combinations/subsets?}
    B2 -->|Yes| C2[Backtracking]
    B2 -->|No| B3{Is it a graph problem?}
    B3 -->|Yes| C3[DFS, BFS, Union-Find, Topological Sort]
    B3 -->|No| B4{Is it a tree problem?}
    B4 -->|Yes| C4[DFS Preorder, Inorder, Postorder, BFS]
    B4 -->|No| B5{Is it a sliding window problem?}
    B5 -->|Yes| C5[Sliding Window, Two Pointers]
    B5 -->|No| B6{Does it involve finding the top-k elements?}
    B6 -->|Yes| C6[Min-Heap, Max-Heap]
    B6 -->|No| B7{Does it involve overlapping subproblems?}
    B7 -->|Yes| C7[Dynamic Programming]
    B7 -->|No| B8{Is it a merge intervals problem?}
    B8 -->|Yes| C8[Merge Intervals]
    B8 -->|No| B9{Is it a fast/slow pointer problem?}
    B9 -->|Yes| C9[Fast & Slow Pointers]
    B9 -->|No| B10{Does it require prefix sum or range queries?}
    B10 -->|Yes| C10[Prefix Sum, Difference Array]
    B10 -->|No| B11{Is recursion banned but the problem is recursive?}
    B11 -->|Yes| C11[Simulate with Stack]
    B11 -->|No| C12[Use maps/sets or sort for efficient search]

    C3 --> D1[Graph-Specific Algorithms]
    D1 --> E1[Shortest Path: BFS, Dijkstra, A*]
    D1 --> E2[Minimum Spanning Tree: Kruskal, Prim]
    D1 --> E3[Cycle Detection: Union-Find]

    C7 --> D2[DP Techniques]
    D2 --> F1[Top-Down Memoization]
    D2 --> F2[Bottom-Up Tabulation]

    C4 --> D3[Tree Traversals]
    D3 --> G1[Level Order Traversal]
    D3 --> G2[Lowest Common Ancestor]

    C6 --> D4[Heap Applications]
    D4 --> H1[Kth Largest Element]
    D4 --> H2[Top K Frequent Elements]

    C2 --> I1[Subset Generation]
    C2 --> I2[N-Queens]

    C5 --> J1[Maximum/Minimum Subarray Problems]
    C5 --> J2[Longest Substring Without Repeating Characters]

    C8 --> K1[Interval Intersection]
    C8 --> K2[Meeting Rooms II]

    C9 --> L1[Cycle Detection]
    C9 --> L2[Middle of Linked List]

    C10 --> M1[Range Sum Query]
    C10 --> M2[Subarray Sum Equals K]

    C11 --> N1[Inorder Traversal Without Recursion]
    C11 --> N2[Evaluate Reverse Polish Notation]

    C12 --> O1[Two Sum]
    C12 --> O2[Frequency Count Problems]
```
