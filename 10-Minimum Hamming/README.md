# 10-Minimum Hamming

## Algorithm:

The Hamming Distance of every feasible pair can be used to solve this problem naively, but a quicker method is known that can reduce the complexity to O(N). It is evident that each bit pair adds one bit to the final result when we compute the Hamming distance between two values. Thus, for every ith bit in a number, we can compute the answer provided by all such pairings. Assuming that every number can be represented in 32 bits, we may maintain the final on_bits and off_count count by iterating over every number's ith bit and determining whether it is on or off. We can therefore determine the answer contributed as only the pairs with different ith bits contribute to the solution  by all ith bits of the integers by figuring out how many pairs have distinct ith bits. This allows us to compute the response for a single bit in O(N) and to sum the answers for all bits, whose count does not exceed 32, to get the final answer.     

### Time Complexity: O(N * 32) = O(N) (Ammortized)

### Space Complexity: O(1)