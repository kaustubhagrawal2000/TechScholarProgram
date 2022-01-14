<pre>
How to solve a problem
1: Understand the problem clearly
1. Ask questions & clarify the problem statement clearly.
2. Take an example or two to confirm your understanding of the input/output & extend it to test cases
Milestone 2: Finalize approach & execution plan
1. Understand what type of problem you are solving.
     a. Obvious logic, tests ability to convert logic to code
     b. Figuring out logic
     c. Knowledge of specific domain or concepts
     d. Knowledge of specific algorithm
     e. Mapping real world into abstract concepts/data structures
2. Brainstorm multiple ways to solve the problem and pick one
3. Get to a point where you can explain your approach to a 10 year old
4. Take a stab at the high-level logic & write it down.
5. Try to offload processing to functions & keeping your main code small.
Milestone 3: Code by expanding your pseudocode
1. Make sure you name the variables, functions clearly.
2. Avoid constants in your code unless necessary; go for generic functions, you can use examples for your thinking though.
3. Use libraries as much as possible
Milestone 4: Prove to the interviewer that your code works with unit tests
1. Make sure you check boundary conditions
2. Time & storage complexity
3. Suggest optimizations if applicable

</pre>

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
</pre>

![photo1641996588](https://user-images.githubusercontent.com/65703138/149157025-ac8cfe0a-8288-4c38-bd43-29b5c2ea9644.jpeg)

<pre>
4. Find if the string permutation can form a palindrome

sol:-
//even len= all chars repeat twice
//odd len= all char repeat else one elem which repeats odd no of times


eg nnamm
n(2) a(1) m(2)
yes it is 

nnammd
n(2) m(2) a(1) d(1) 
not a palindrome

create a hasmap of the count of char
traverse the map 
if odd occ>1 declare it as false
if odd occ<1 declare it as true
</pre>


