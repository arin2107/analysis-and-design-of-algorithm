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


## 7.PRACTICAL 7 : QUICK SORT ANALYSIS
ALGORITHM:

This function implements the partition operation of the QuickSort algorithm. It selects a pivot element (here, the first element), rearranges the array elements such that elements smaller than the pivot come before it, and elements greater than the pivot come after it. The function returns the index of the pivot after partitioning.


GRAPH:

import matplotlib.pyplot as plt
values = [
(1000000,1696900),
(1050000,1686100),
(1100000,1684900),
(1150000,3296500),
(1200000,4991100),
(1250000,2151000),
(1300000,3353100),
(1350000,1521300),
(1400000,1686600),
(1450000,4773100),
(1500000,4853600),
(1550000,1779800),
(1600000,3417300),
(1650000,3400300),
(1700000,5020600),
(1750000,4903600),
(1800000,1844600),
(1850000,4775000),
(1900000,5095700),
(1950000,5274300),
(2000000,5364900),
(2050000,3545400),
(2100000,4806200),
(2150000,3327900),
(2200000,6712900),
(2250000,6795300),
(2300000,5184600),
(2350000,6869900),
(2400000,6330500),
(2450000,8046900),
(2500000,2835300),
(2550000,3538400),
(2600000,4965900),
(2650000,7992400),
(2700000,4161200),
(2750000,5046700),
(2800000,6562700),
(2850000,7407200),
(2900000,5851600),
(2950000,3715100),
(3000000,8400100),
(3050000,7181300),
(3100000,7896700),
(3150000,6677400),
(3200000,3344800),
(3250000,4868500),
(3300000,9109300),
(3350000,10471300),
(3400000,8252300),
(3450000,5106400),
(3500000,10910300),
(3550000,9309400),
(3600000,6824600),
(3650000,9708900),
(3700000,11761300),
(3750000,12322100),
(3800000,11688500),
(3850000,9776600),
(3900000,6657600),
(3950000,5005600),
(4000000,8805100),
(4050000,11371200),
(4100000,5006400),
(4150000,7384600),
(4200000,11356600),
(4250000,11255200),
(4300000,9176000),
(4350000,12974500),
(4400000,5132600),
(4450000,13116900),
(4500000,9576000),
(4550000,11330600),
(4600000,8623600),
(4650000,7965700),
(4700000,13249700),
(4750000,12945700),
(4800000,5385600),
(4850000,12718000),
(4900000,9598000),
(4950000,11166400),
(5000000,11564900),
(5050000,12917000),
(5100000,14487800),
(5150000,14178800),
(5200000,11157900),
(5250000,14533400),
(5300000,7546300),
(5350000,9108900),
(5400000,9802700),
(5450000,14265600),
(5500000,16550600),
(5550000,14201200),
(5600000,8042000),
(5650000,8005500),
(5700000,11188900),
(5750000,17218500),
(5800000,11221500),
(5850000,12525800),
(5900000,15737700),
(5950000,15811000),
(6000000,17404700),
(6050000,9617200),
(6100000,20719400),
(6150000,16508000),
(6200000,9596400),
(6250000,17433900),
(6300000,19645400),
(6350000,11054900),
(6400000,14489500),
(6450000,8042800),
(6500000,15990800),
(6550000,19967900),
(6600000,17399800),
(6650000,15992400),
(6700000,17424300),
(6750000,11031500),
(6800000,11133600),
(6850000,21053000),
(6900000,12482400),
(6950000,17874300),
(7000000,15645700),
(7050000,9538800),
(7100000,12735700),
(7150000,11131800)
]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b')

plt.xlabel('Input Values')
plt.ylabel('NanoSeconds')
plt.title('Inputs Vs Time Graph')

plt.show()

![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/5f4fd052-e735-4832-84b0-8813af3bf381)


TIME COMPLEXITY:
The time complexity of the partition operation in the QuickSort algorithm is O(n), where 'n' is the size of the array being partitioned



## 8.PRACTICAL : MERGE SORT ANALYSIS

ALGORITHM:

This practical implements the merge sort algorithm recursively. It divides the array into two halves, sorts each half independently, and then merges the sorted halves.
GRAPH:
import matplotlib.pyplot as plt

values = [
    (100000, 400100),
 (120000, 799900),
  (140000, 700400),
  (160000, 699500),
  (180000, 900300),
  (200000, 1103200),
  (220000, 1201400),
  (240000, 1100600),
   (260000, 1401600),
  (280000, 1699600),
  (300000, 1500200),
  (320000, 1899700),
  (340000, 1798900),
  (360000, 1899700),
  (380000, 1899500),
  (400000, 2099700),
  (420000, 2302200),
  (440000, 2300400),
  (460000, 2800400),
   (480000, 3199800),
  (500000, 3397200)
  ]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b', label='Original Line')

plt.xlabel('Input Values')
plt.ylabel('Seconds')

plt.title('Inputs Vs Time Graph')

plt.legend()

plt.show()

![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/3eb0e5d6-cc31-4a5a-bdaf-f89ed27a28e6)


TIME COMPLEXITY:

The time complexity of the merge sort algorithm is O(n log n), where 'n' is the size of the array.


## 9. GENERATE MAGIC SQAURE 

ALGORITHM :

The Siamese method is a constructive algorithm for creating odd-order magic squares.
The main idea is to start from the central cell of the first row and fill the square by moving diagonally up and to the right.
If a move takes the position out of the matrix bounds, it wraps around to the opposite side.
If the cell is already occupied, move vertically down one position instead.


GRAPH:

import matplotlib.pyplot as plt

values = [
(3,00 ),
(5,00 ),
(7,00 ),
(9,10 ),
(11,20 ),
(13,20 ),
(15,30 ),
      
]

x_values, y_values = zip(*values)

plt.plot(x_values, y_values, marker='o', linestyle='-', color='b')

plt.xlabel('Input Values')
plt.ylabel('NanoSeconds')
plt.title('Inputs Vs Time Graph')

plt.show()
![image](https://github.com/arin2107/analysis-and-design-of-algorithm/assets/121510816/e8986be6-e2dc-4e25-90be-3ec91fea579b)


TIME COMPLEXITY:
The time complexity of generating a magic square using the Siamese method is O(n^2), where 'n' is the order of the square.
