# Searching
# EXPERIMENT 20: SEARCHING ALGORITHMS IN C++

## AIM
To understand and implement different searching techniques in C++ including **Linear Search**, **Sequential Search**, and **Binary Search** for locating elements in arrays.

## TOOLS REQUIRED
- Compiler: GCC / CodeBlocks / Visual Studio / any standard C++ compiler
- Operating System: Windows / Linux / MacOS
- Editor: VS Code / Sublime Text / CodeBlocks / Terminal-based editors

## THEORY

Searching is the process of finding a particular element (called **key**) within a data structure such as an array or list. Efficient searching reduces computation time in applications.

### 1. Linear Search
- Also known as **sequential search** (often the terms are used interchangeably).
- Works by checking each element in the array **one by one** until the desired element is found.
- Time Complexity: **O(n)**, where n is the number of elements.
- Advantages: Simple, does not require sorted data.
- Disadvantages: Inefficient for large datasets.

### 2. Binary Search
- Efficient search method for **sorted arrays**.
- Follows a **divide-and-conquer** approach:
  1. Compare the key with the middle element.
  2. If the key is smaller, search the left half; if larger, search the right half.
  3. Repeat until the element is found or the subarray is empty.
- Time Complexity: **O(log n)**.
- Advantages: Very fast for large sorted datasets.
- Disadvantages: Requires the array to be sorted.

### Applications
- Database lookup
- Searching in file systems
- Real-time systems where fast retrieval is critical
- Implementing algorithms for games, search engines, and AI systems

## EXPERIMENT 20(A): LINEAR SEARCH IN C++

### ALGORITHM
1. **START**  
2. Initialize an array `arr` of size `n` with given elements.  
3. Accept the `key` element to search for.  
4. Loop through each element of the array from index 0 to n-1:  
   - If `arr[i] == key`, return index `i`.  
5. If the loop ends without finding the key, return -1 indicating element not found.  
6. **STOP**

## EXPERIMENT 20(B): BINARY SEARCH IN C++

### ALGORITHM
1. **START**  
2. Initialize a **sorted** array `arr` of size `n`.  
3. Accept the `key` element to search for.  
4. Initialize `low = 0` and `high = n-1`.  
5. Repeat while `low <= high`:  
   - Compute `mid = low + (high - low)/2`.  
   - If `arr[mid] == key`, return `mid`.  
   - Else if `arr[mid] < key`, set `low = mid + 1`.  
   - Else, set `high = mid - 1`.  
6. If the loop ends without finding the key, return -1 (element not found).  
7. **STOP**

## CONCLUSION

In this experiment, we implemented **Binary Search**, an efficient searching algorithm for sorted arrays.  
We learned that Binary Search significantly reduces the number of comparisons compared to Linear Search, achieving a **time complexity of O(log n)**.  
The experiment demonstrated how dividing the search space in half repeatedly can quickly locate an element or determine its absence.  
We also understood the importance of maintaining a sorted array before applying Binary Search.
