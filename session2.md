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
max value on rhs- maintain an array and put on the elements larger 
lower bound - trying to put the element in set and use the lower bound

</pre>
<pre>

4.Prartioning element in an array

sol:- 1st and last element can't be the ans.
take the prefix sum and suffix sum and return the index where both the values are equal.

or

a. sufix sum=sum of array
b. prefix sum=0
c. for i=0 to n
ps=a[i]
if ps==ss
return a[i]
ss==a[i]
return -1

</pre>

<pre>
5. Kadanes algo 

prefix sum(l to r)=prefixsum[r]-prefixsum[l-1]
![Screenshot (916)](https://user-images.githubusercontent.com/65703138/149615170-e778349d-033c-474c-82cc-2419822c3fc3.png)


</pre>
