# 11-Counting Subgrids

## Algorithm:

We must determine whether all feasible pairings of squares in the same column are set to 1 for the two rows that are provided. Then, we can combine any two of these square combinations to create a subgrid with black color in all four corners. It is now evident to us that every row in the matrix can be represented as a binary number or bit string. This facilitates row-by-row computations to determine which two squares in a given column are set in O(1) time. In order to determine every conceivable combination of squares in a given column for each row, we first apply the AND operation to the two rows (bit strings). The number of 1s in the resulting bit string is then determined. Next, we count all possible unique pairs of 1s to determine the number of subgrids where the four corners are located in those two rows, two of each. After that, we continue this process for every pair of rows, adding up each pair's answers to get our final answer. 
### Time Complexity: O(N * N)

### Space Complexity: O(N) (for storing all rows as bitsets)