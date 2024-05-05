# 14-Valid Arrangement of Pairs

## Algorithm:

The numerical pairs can be represented as a directed graph, where an edge from n to m vertices is indicated by the notation {n, m}. Therefore, the task at hand can be simplified to locating an Eulerian path within the graph. Hierholzer's Algorithm, a common algorithm, is used for this. It looks like this:

1. To determine whether the graph has an Eulerian path, we first determine if there are at most two vertices with indegree and outdegree differences of one and all other vertices have the same values.
2. The next step is to choose as the start node one of the two nodes with differing indegree and outdegree (i.e., the node with greater outdegree than indegree); if no such node exists, we can designate any node as the start node because the graph contains an Eulerian circuit. 
3. We call the DFS on the start node and initialize a stack.
4. We call the DFS recursively on neighboring nodes in each DFS call until we have used up all of the node's potential outgoing edges. The node is then pushed up the stack.
5. The solution is obtained by popping the nodes in the stack and adding them to the path vector when the recursive DFS is finish

### Time Complexity: O(V + E) where V is the number of vertices in the graph and E is the number of edges in the graph

### Space Complexity: O(1)