<pre>
How to solve a problem
1. Understand the problem
2. Finalize the approach
3.
4.



Intro to Array Problems

1.Square Matrix
Print a 2D matrix of size A*A in spiral order
- i/p =1 2 3 4 5 6 7 8 9 
- o/p= 
1 2 3
8 9 4
7 6 5
 
sol:-
top left------------- top right
 |                       |
 |                       |
 bottom left-----------bottom right
 </pre>
 
 ![photo1641993018](https://user-images.githubusercontent.com/65703138/149146813-e922a492-c11f-4a3c-828c-0f93dd98842d.jpeg)
<pre>
2. Increment number represented as array 
Given a numb represented as an array of digits , increment the numb by 1 and return the resulting sum as an array.
- i/p
3
1 1 1
-o/p
112
(111+1=112)

sol:-
get a carry num>10
move ahead num<10

</pre>
<pre>
3. Given an unsorted array of int ,find the smallest missing positive integers.

i/p 
4
3 4 -1 1

o/p
2

sol:
if the elemnt is in range 1 to n 
push it into hashmap
now check if the number is present on hashmap or not

range of valuse present in array: -10^9 to 10^9

2 3 -1 4
First missing +ve numb is always between 1 to N+1
ith index contains i+1 value.
-1 2  3  4
0  1  2  3


![photo1641996588](https://user-images.githubusercontent.com/65703138/149157025-ac8cfe0a-8288-4c38-bd43-29b5c2ea9644.jpeg)


</pre>


