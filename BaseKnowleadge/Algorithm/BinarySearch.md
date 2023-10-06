# Binary Search
## 1. Binary Search 
Binary Search is defined as a searching algorithm used in a **sorted array** by repeatedly dividing the search interval in half. 

## 2. When to use
To apply Binary Search algorithm:
+ The data structure must be sorted.
+ Access to any element of the data structure takes constant time.

## 3. How to use
The Binary Search Algorithm can be implemented in the following two ways:
+ Iterative Binary Search Algorithm
+ Recursive Binary Search Algorithm

## 4. Complexity
+ Time Complexity: 
    + Best Case: O(1)
    + Average Case: O(log N)
    + Worst Case: O(log N)
+ Auxiliary Space: O(1), If the recursive call stack is considered then the auxiliary space will be O(logN).

## 5. Advantages of Binary Search:
+ Binary search is faster than linear search, especially for large arrays.
+ More efficient than other searching algorithms with a similar time complexity, such as interpolation search or exponential search.
+ Binary search is well-suited for searching large datasets that are stored in external memory, such as on a hard drive or in the cloud.

## 6. Drawbacks of Binary Search:
+ The array should be sorted.
+ Binary search requires that the data structure being searched be stored in contiguous memory locations. 
+ Binary search requires that the elements of the array be comparable, meaning that they must be able to be ordered.

## 7. Applications of Binary Search:
+ Binary search can be used as a building block for more complex algorithms used in machine learning, such as algorithms for training neural networks or finding the optimal hyperparameters for a model.
+ It can be used for searching in computer graphics such as algorithms for ray tracing or texture mapping.
+ It can be used for searching a database.