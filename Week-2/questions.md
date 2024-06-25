1. **What are nodes and edges in a graph, and how do they relate to each other?**

   **Answer:** 
   - **Nodes (Vertices):** Represent entities or points in the graph.
   - **Edges:** Represent the relationships or connections between the nodes.

2. **Explain the concept of the degree of a vertex in both undirected and directed graphs.**

   **Answer:** 
   - **Undirected Graphs:** Degree of a vertex is the number of edges incident to it.
   - **Directed Graphs:** Degree is split into in-degree (edges coming in) and out-degree (edges going out).

3. **Define the length of a path in a graph. What is the length of a path consisting of a single vertex?**

   **Answer:** 
   - **Length of a Path:** Number of edges in the path.
   - **Single Vertex Path:** Length is 0 (no edges).

4. **Differentiate between directed and undirected graphs, focusing on their edge properties.**

   **Answer:** 
   - **Directed Graph:** Edges have direction, indicating one-way relationships.
   - **Undirected Graph:** Edges have no direction, indicating mutual relationships.

5. **Can you traverse backward in a directed graph without an explicitly reversed edge? Explain.**

   **Answer:** 
   - No, traversal in a directed graph depends on edge direction.
   - Without a reverse edge, no direct traversal against the edge direction is possible.

6. **What does an adjacency list represent for each vertex in a graph?**

   **Answer:** 
   - List of vertices adjacent to each vertex.

7. **How does the representation of an adjacency list change with the graph's density?**

   **Answer:** 
   - Sparse Graph: Fewer entries per vertex list.
   - Dense Graph: More entries per vertex list.

8. **Describe the structure of an adjacency matrix for unweighted graphs.**

   **Answer:** 
   - \( n \times n \) matrix (where \( n \) is number of vertices).
   - Entry at \( (i, j) \) is 1 if edge exists between vertex \( i \) and vertex \( j \); otherwise, 0.

9. **What determines the dimensions of an adjacency matrix for a given graph?**

   **Answer:** 
   - Number of vertices \( n \): Matrix is \( n \times n \).

10. **Why are adjacency matrices considered efficient for representing dense graphs?**

    **Answer:** 
    - Fixed size \( n \times n \), good for quick edge lookup.
    - Efficient representation when many edges exist.

11. **Compare the memory requirements of adjacency lists and adjacency matrices.**

    **Answer:** 
    - **Adjacency List:** \( \Theta(V + E) \) (V = vertices, E = edges).
    - **Adjacency Matrix:** \( \Theta(V^2) \).

12. **Explain why adjacency lists are preferred for sparse graphs over adjacency matrices.**

    **Answer:** 
    - Occupy less memory \( \Theta(V + E) \) compared to \( \Theta(V^2) \) for matrices.
    - More efficient for sparse graphs where \( E << V^2 \).

13. **Provide an example of an adjacency list for vertices u, v, and w, where each is adjacent to the others.**

    **Answer:** 
    - u: [v, w]
    - v: [u, w]
    - w: [u, v]

14. **Illustrate how an adjacency matrix would be filled for the same graph with vertices u, v, and w.**

    **Answer:** 
    ```
       u  v  w
    u  0  1  1
    v  1  0  1
    w  1  1  0
    ```

15. **What does a symmetric adjacency matrix indicate about a graph?**

    **Answer:** 
    - Indicates an undirected graph.
    - Edge from \( i \) to \( j \) implies an edge from \( j \) to \( i \).

16. **What are the primary attributes initialized for each vertex in the Breadth-First Search (BFS) algorithm?**

    **Answer:** 
    - Color (white, blue, black).
    - Distance from source vertex.
    - Parent vertex in BFS tree.

17. **What role does the queue play in the BFS algorithm, and why is it essential?**

    **Answer:** 
    - Manages order of vertex exploration (FIFO).
    - Ensures breadth-first traversal order.

18. **Describe the step-by-step process of BFS starting from a source vertex in a graph.**

    **Answer:** 
    1. Initialize source vertex (color blue, distance 0, parent null), enqueue.
    2. Dequeue vertex \( u \), explore adjacent vertices \( v \).
    3. If \( v \) unvisited, set color blue, distance \( u \)'s + 1, parent \( u \), enqueue \( v \).
    4. Set \( u \) color black after exploring all adjacent vertices.

19. **Explain the significance of vertex colors during the BFS traversal process.**

    **Answer:** 
    - White: Unvisited.
    - Blue: Discovered and in queue.
    - Black: Fully explored.

20. **What does the BFS algorithm output upon completion of its traversal?**

    **Answer:** 
    - Shortest path tree.
    - Distance from source to each reachable vertex.

21. **How does BFS define the "shortest path" in the context of graph traversal?**

    **Answer:** 
    - Minimum number of edges from source vertex to any other reachable vertex.

22. **What happens when the BFS queue becomes empty during its execution?**

    **Answer:** 
    - All reachable vertices explored, algorithm terminates.

23. **State the BFS theorem and its implication regarding the algorithm's correctness.**

    **Answer:** 
    - BFS finds every vertex reachable from source \( s \).
    - Determines shortest path from \( s \) to each reachable vertex.

24. **What are the memory requirements of the BFS algorithm, and how are they calculated?**

    **Answer:** 
    - \( \Theta(V + E) \) (V = vertices, E = edges).
    - Store color, distance, parent, queue, adjacency list.

25. **Describe how BFS produces a tree of shortest paths from a source vertex in a graph.**

    **Answer:** 
    - Records parent (predecessor) as each vertex is discovered and enqueued.
    - Parent information forms edges of shortest path tree.

26. **What is the significance of the tree edges in the BFS output?**

    **Answer:** 
    - Represent paths used to reach each vertex from source.
    - Structure of shortest path tree.

27. **Explain the relationship between Depth-First Search (DFS) and BFS in terms of traversal strategy.**

    **Answer:** 
    - DFS: Goes deep into graph, backtracks.
    - BFS: Explores all neighbors, level by level.

28. **Define Strongly Connected Components (SCCs) in the context of directed graphs.**

    **Answer:** 
    - Maximal subgraphs where every vertex is reachable from every other vertex in the same subgraph.

29. **How does DFS assist in identifying Strongly Connected Components (SCCs) in a directed graph?**

    **Answer:** 
    - First DFS run computes finish times.
    - Transpose graph, second DFS run identifies SCCs using finish times order.

30. **What are some real-world applications of Depth-First Search (DFS) and Strongly Connected Components (SCCs) in various domains?**

    **Answer:** 
    - DFS: Pathfinding, cycle detection, topological sorting.
    - SCCs: Network analysis, component-based systems, compiler optimizations.

---