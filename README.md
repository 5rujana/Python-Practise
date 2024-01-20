# Python Pratice

### 1. Container With Most Water:

#### Problem Description:
Given an array `height` of non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.

#### Input:
```python
height = [1, 8, 6, 2, 5, 4, 8, 3, 7]
```

#### Output:
```
49
```

#### Explanation:
The input array represents the heights of bars. The goal is to find two bars such that the area between them and the x-axis forms a container with the maximum amount of trapped water. The maximum area is achieved by choosing the heights at positions 1 and 8, giving a width of 8 - 1 = 7 and a minimum height of 7. The area is calculated as width * min(height[left], height[right]).

### 2. 3Sum:

#### Problem Description:
Given an array `nums` of n integers, find all unique triplets in the array that give the sum of zero.

#### Input:
```python
nums = [-1, 0, 1, 2, -1, -4]
```

#### Output:
```
[[-1, -1, 2], [-1, 0, 1]]
```

#### Explanation:
The goal is to find three numbers in the array such that their sum is zero. Sort the array and use three pointers to iterate through the array. For each element, find two other elements such that their sum is zero. Avoid duplicates in the output.

### 3. Product of Array Except Self:

#### Problem Description:
Given an array `nums`, return an array `output` such that `output[i]` is equal to the product of all the elements of `nums` except `nums[i]`.

#### Input:
```python
nums = [1, 2, 3, 4]
```

#### Output:
```
[24, 12, 8, 6]
```

#### Explanation:
The goal is to calculate the product of all elements to the left and right of each element separately and multiply them to get the desired output. For example, the element at index 2 (3) is the product of elements to the left (1 * 2) and to the right (4), giving 24.

### 4. Rotate Image:

#### Problem Description:
You are given an n x n 2D matrix representing an image. Rotate the image by 90 degrees (clockwise).

#### Input:
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

#### Output:
```
[
    [7, 4, 1],
    [8, 5, 2],
    [9, 6, 3]
]
```

#### Explanation:
The task is to perform a 90-degree clockwise rotation of the given matrix. This can be achieved by transposing the matrix (swapping rows with columns) and then reversing each row.

### 5. Spiral Matrix:

#### Problem Description:
Given an m x n matrix, return all elements of the matrix in spiral order.

#### Input:
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

#### Output:
```
[1, 2, 3, 6, 9, 8, 7, 4, 5]
```

#### Explanation:
The goal is to traverse the matrix in a spiral order, starting from the top-left corner. This involves moving right, down, left, and up while updating the direction when reaching the boundaries.

### 6. Subarray Sum Equals K:

#### Problem Description:
Given an array `nums` and an integer `k`, return the total number of continuous subarrays whose sum equals `k`.

#### Input:
```python
nums = [1, 1, 1]
k = 2
```

#### Output:
```
2
```

#### Explanation:
The task is to find the number of subarrays with a sum equal to the given `k`. Use a cumulative sum and a hashmap to keep track of the sum encountered so far. The number of times the sum `sum - k` has been encountered gives the count of subarrays with sum `k`.

### 7. Find All Duplicates in an Array:

#### Problem Description:
Given an array `nums`, find all the integers that appear more than once in the array.

#### Input:
```python
nums = [4, 3, 2, 7, 8, 2, 1, 4]
```

#### Output:
```
[2, 4]
```

#### Explanation:
The goal is to find duplicates in the array. Use the array itself as a hash table. Mark the elements by negating the value at the corresponding index. If an element is encountered again and its value is already negative, it is a duplicate.

### 8. Jump Game:

#### Problem Description:
Given an array of non-negative integers `nums`, you are initially positioned at the first index of the array. Determine if you can reach the last index.

#### Input:
```python
nums = [2, 3, 1, 1, 4]
```

#### Output:
```
True
```

#### Explanation:
The task is to determine whether it is possible to reach the last index of the array. Use a greedy approach to keep track of the maximum reachable index. If, at any point, the current index is greater than the maximum reachable index, return False. Otherwise, continue updating the maximum reachable index.

### 9. Valid Sudoku:

#### Problem Description:
Determine if a 9x9 Sudoku board is valid.

#### Input:
```python
board = [
    ["5","3",".",".","7",".",".",".","."],
    ["6",".",".","1","9","5",".",".","."],
    [".","9","8",".",".",".",".","6","."],
    ["8",".",".",".","6",".",".",".","3"],
    ["4",".",".","8",".","3",".",".","1"],
    ["7",".",".",".","2",".",".",".","6"],
    [".","6",".",".",".",".","2","8","."],
    [".",".",".","4","1","9",".",".","5"],
    [".",".",".",".","8",".",".","7","9"]
]
```

#### Output:
```
True
```

#### Explanation:
The goal is to check the validity of the Sudoku board. This involves checking the validity of rows, columns, and 3x3 sub-grids separately. Use sets to keep track of encountered digits.

### 10. Next Permutation:

#### Problem Description:
Implement next permutation, which rearranges numbers into the lexicographically next greater permutation of numbers.

#### Input:
```python
nums = [1, 2, 3]
```

#### Output:
```
[1, 3, 2]
```

#### Explanation:
The task is to find the lexic

ographically next greater permutation of the given numbers. Find the first pair of consecutive numbers in reverse order such that `nums[i] < nums[i+1]`. Swap `nums[i]` with the smallest number greater than `nums[i]` from the suffix. Reverse the suffix. For example, for `[1, 2, 3]`, the next permutation is `[1, 3, 2]`.
