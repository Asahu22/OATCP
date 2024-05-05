# 12-Finding Maximum Flow

## Algorithm:

Finding the maximum flow in a graph is computed by using a standard algorithm called the Ford Fulkerson algorithm. It is as follows:

We attempt to discover a feasible path from the source to the sink in the graph, starting with 0 flow (max capacity) in every edge. Any path from the source to the sink along which the flow may be increased without causing any edges to overflow is considered a feasible path. An augmenting path is another name for this route. The next step is to identify the edge in the path with the least amount of available capacity, or "bottleneck," and use that value to increase the capacity of all the edges in the opposite direction and reduce it in the direction of travel.  Until there are no more augmenting paths accessible, or paths connecting the source and the sink, we continue to identify new ones and carry out the same procedure. We calculate the total feasible flow in the graph by adding the bottlenecks over all augmenting pathways. Since the augmenting pathways are not specified in the Ford Fulkerson algorithm, we can locate them using any graph traversal approach, such as BFS or DFS. The adjacency matrix was utilized to store the graph, and BFS, also referred to as the Edmonds-Karp Algorithm, was utilized to identify the augmenting pathways.

### Time Complexity: O(E * V * V * V) where V is the number of vertices in the graph and E is the number of edges in the graph

### Space Complexity: O(V * V)