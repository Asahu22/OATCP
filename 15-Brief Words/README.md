# 15-Brief Words

## Algorithm:

The algorithm creates a bipartite graph, with the input strings represented by one set of vertices and the distinct short strings (of length 4 or fewer) represented by the other set. If the input string can be changed into that short string, then an edge is generated between the string vertex and the short string vertex. The algorithm looks for a perfect matching in the bipartite network, where each input string is given a distinct short string, in order to identify a successful transformation. To do this, a DFS is applied to the graph, beginning at each vertex of the input string. If a legitimate short string assignment to the current input string is discovered during the DFS, the search is carried out recursively to assign short strings to the remaining input strings. The matching short string for each input string is pulled from the map and printed as the output if a perfect match is found.

### Time Complexity: O(N * M), where N is the number of input strings and M is the maximum length of a string

### Space Complexity: O(N * M), where N is the number of input strings and M is the maximum length of a string