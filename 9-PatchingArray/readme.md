Here, we can iterate through nums while keeping track of the current range we can build in order to add items to a sorted integer array nums so that every number in the range [1, n] inclusive can be formed by the sum of some values in the array. We must include a patch to close the gap if the next element in nums is larger than the range that it is currently within. We can double the range by adding the patch as the current range as we can combine the new number with any prior number.

Time Complexity : O(n)
Space Complexity : O(1)