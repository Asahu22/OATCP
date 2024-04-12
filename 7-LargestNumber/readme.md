This method sorts a vector of strings of numbers by defining a custom comparator. If a + b > b + a, then an is larger than b. The numbers are then sorted and concatenated. You can use any kind of sort; however, while sorting, we can use the current comparator logic to compare and swap elements based on that comparison rather than explicitly comparing two values. We now add each iteration of the string vector to the answer. 

Time Complexity : O(n * logn)
Space Complexity : O(n)