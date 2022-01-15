<pre>
1.Given a sorted array of integers and a target, find if there’s a pair of elements that add up to the target. 
Return true if such a pair can be found, and false otherwise.


Brute force - Use of two loops
Optimal approach :
1. Use of hashmap
2. Two pointer approach
O(n2) could be simplified or optimized using 2 pointer approach to O(n) so we should always try it.
One pointer at the first second pointer at the last.



</pre>

<pre>

2. Given two sorted arrays of size M and N, merge the two arrays and return the final array, sorted.

sol:-
Using two pointer approach . Taking one pointer at one array second pointer on another and ding mergea sort on them .
</pre>

<pre>

3.Given an array nums, you need to find the maximum sum of triplet (nums[i] + nums[j] + nums[k]) such that 0 <= i < j < k and nums[i] < nums[j] < nums[k]. If no such triplet exists print 0.

sol:-

brute force : 3 loops
optimized:
Take a pointer. Find the lower bound on left and max element in right. 

</pre>
<pre>
4. Given a sorted array, remove the duplicates in-place, such that each element in the array appears at most twice, and return the new length.

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

</pre>
