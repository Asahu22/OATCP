Using a stack, we can employ a greedy strategy in this case. We begin by adding a non-zero element to the stack. We look to see if the next element we come across is smaller than the one that is presently in the stack. If so, we push the new element and remove the old one from the stack. This is because, in comparison to the previous element, the new one may produce a lesser number. However, since only k deletions are permitted, we must restrict the total number of pops to a maximum of k.

Time Complexity : O(n)
Space Complexity : O(n)