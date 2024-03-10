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
