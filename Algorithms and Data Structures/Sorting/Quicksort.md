## Quicksort
**Type**: in-place algorithm.

**Best case performance:** O(n log(n))  
log(n)   
In the most balanced case, each time we perform a partition we divide the list into two nearly equal pieces. This means each recursive call processes a list of half the size. Consequently, we can make only log2n nested calls before we reach a list of size 1.

n  
When we have left subarray, pivot, and right subarray we need to do partitioning. This means that we will go form the start of left subarray and from the end of the right subarray to the pivot. So as we don't know whether or not it's already sorted we will go for *n* iterations.

**Worst case performance:** O(n^2)  
When we peek leftmost or rightmost pivot and

 - Array is already sorted(either in direct order or reverse)
 - All element are the same.

**Algorithm**
1. Pick a pivot.
2. Divide array into three parts: 
left-subarray - elements that are lesser than pivot
pivot
right-subarray - elements that are greater than pivot
3. Partitioning phase.
Go from start of the left-subarray and end of the right sub-array. Find element form the left which is greater then pivot and element from the right which is lesser than pivot. Swap them.

 
