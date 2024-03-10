# analysis-and-design-of-algorithm

##  1.Practical 1 :- Selection sort analysis
ALGORITHM :  This practical  implements the selection sort algorithm. It iterates through the array, finds the minimum element in the unsorted part, and swaps it with the first element of the unsorted part. This process is repeated until the entire array is sorted.

GRAPH:import matplotlib.pyplot as plt

values = [
    (1000, 0),
    (3000, 4),
    (5000, 10),
    (7000,17),
    (9000, 29),
    (11000, 43),
    (13000,63),
    (15000,80),
    (17000,103),
    (19000,133)

]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b')

plt.xlabel('Input Values')

plt.ylabel('Seconds')
plt.title('Inputs Vs Time Graph')

plt.show()
![1_graph](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/078ae408-14ea-4fa0-8d0e-afd25de553ca)

TIME COMPLEXITY : The time complexity of the selection sort algorithm is O(n^2) in the worst case. This is because, for each element in the array, it performs a linear search through the remaining unsorted elements to find the minimum value and then swaps it. The nested loops contribute to the quadratic time complexity


## 2.PRACTICAL 2 :- SUM OF n NUMBERS

ALGORITHM : The algorithm used here is a straightforward summing of the elements in an array. The sum_numbers function iterates through each element of the array and accumulates the sum.

GRAPH:
import matplotlib.pyplot as plt

values = [
    (1000000,1621300),
    (1500000, 3539600),
    (2000000, 3340500),
    (2500000,4778800),
    (3000000, 5626300),
    (3500000,6389800),
    (4000000,6254900),
    (4500000,7175600),
    (5000000,9147300)

]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b')

plt.xlabel('Input Values')
plt.ylabel('NanoSeconds')
plt.title('Inputs Vs Time Graph')

plt.show()
![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/86d69680-a869-4d6e-a40f-b7daf49ed5d6)

TIME COMPLEXITY: The time complexity of the summing operation is O(n), where 'n' is the number of elements in the array. The loop in the sum_numbers function iterates through each element once, resulting in linear time complexity

## 3.PRACTICAL 3 : TOWER OF HANOI

ALGORITHM: The Tower of Hanoi algorithm is a classical recursive problem. It follows the principles of divide and conquer. The idea is to move 'n' disks from the source peg to the target peg using an auxiliary peg. 

GRAPH: 
import matplotlib.pyplot as plt

values = [
    (18,6221318),
(19,2812452),
(20,10571623),
(21,27133626),
(22,49885788),
(23,110367291),
(24,232394370)

]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b')

plt.xlabel('Input Values')
plt.ylabel('NanoSeconds')
plt.title('Inputs Vs Time Graph')

plt.show()
![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/d4c72d88-419a-4b59-aae5-be6fea176673)

TIME COMPLEXITY : The time complexity of the Tower of Hanoi algorithm is O(2^n), where 'n' is the number of disks. This is an exponential time complexity because, at each step, the problem is divided into two recursive subproblems.

## 4.PRACTICAL 4 : COIN PERMUTATION 

ALGORITHM : 
This function recursively generates all combinations of heads (1) and tails (0) for a given number of coin tosses. It starts with an array arr initialized to all zeros, and at each recursion level, it sets the current toss to heads (1) and recursively calls itself for the next toss. Then, it sets the current toss to tails (0) and recursively calls itself again. 
GRAPH: 
import matplotlib.pyplot as plt

values = [
    (10,0),
    (13, 0),
    (16, 1076300),
    (19,4862400),
    (22, 40249500)

]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b')

plt.xlabel('Input Values')
plt.ylabel('NanoSeconds')
plt.title('Inputs Vs Time Graph')

plt.show()
![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/b629443f-9640-4d4d-8019-8579d950ffb4)


TIME COMPLEXITY:
The time complexity of this code is exponential, specifically O(2^n), where 'n' is the number of coin tosses. This is because, at each toss, there are two possibilities (heads or tails), and the recursive function explores all possible combinations


## 5.PRACTICAL 5 : STRING PERMUTATION 
ALGORITHM :
This PRACRTICAL generates all permutations of a string using recursive backtracking. It swaps characters at different positions in the string to generate all possible arrangements. The base case is when the current position (k) reaches the end of the string (n).

GRAPH:
from math import radians
import numpy as np
import matplotlib.pyplot as plt

values = [
    (3,772),
    (5,7323),
    (7, 321847),
    (9,24059966),
    (11, 3517819827 )

]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b')

plt.xlabel('Input Values')
plt.ylabel('NanoSeconds')
plt.title('Inputs Vs Time Graph')

plt.show()
![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/13e9befa-65dc-445a-95b1-da5df54926d3)


TIME COMPLEXITY :
The time complexity of generating all permutations of a string is O(n!), where 'n' is the length of the string. The recursive backtracking approach explores all possible arrangements, resulting in a factorial growth in the number of function calls.

## 6.PRACTICAL : P0WER FUNCTION
**1.brute approach**
ALGORITHM :
This practical implements a simple recursive algorithm to calculate the power of 'm' raised to the 'n'-th exponent. It uses the recursive property of exponentiation: m^n = m * m^(n-1).

TIME COMPLEXITY : 
The time complexity of this code is exponential, specifically O(2^n), where 'n' is the exponent. This is because, at each step of the recursion, the problem is divided into two subproblems. 

**2.optimal approach**
ALGORITHM : 
The algorithm uses a recursive approach to calculate the power of 'm' raised to the 'n'-th exponent. It takes advantage of the fact that if 'n' is even, the exponentiation can be expressed as the square of the power of 'm' raised to half of 'n'.

TIME COMPLEXITY:
The time complexity of this code is logarithmic, specifically O(log n), where 'n' is the exponent. The optimization for even exponents significantly reduces the number of recursive calls, making the algorithm more efficient compared to the naive recursive approach. 

GRAPH :
import matplotlib.pyplot as plt

values = [
(1000, 3812),

(3000, 16874),
(4000, 21663),
(5000, 30111),
(6000, 35862),
 (7000, 34181),
(8000, 38398),
(9000, 38409),
(10000, 42505)
]



comparison_values = [
(1000, 1200),
(2000, 6800),
(3000, 73000),
(4000, 73000),
(5000, 78000),
(6000, 78000),
(7000, 85000),
(8000, 77000),
(9000, 77000),
(10000, 78000)

]

x_values, y_values = zip(*values)

x_comparison, y_comparison = zip(*comparison_values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b', label='Original Line')

plt.plot(x_comparison, y_comparison, marker='s', linestyle='--', color='r', label='Comparison Line')

plt.xlabel('Input Values')
plt.ylabel('Seconds')

plt.title('Inputs Vs Time Graph')

plt.legend()

plt.show()
![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/15613a0b-cebd-41e3-9ba5-d8bfd94c92ab)


