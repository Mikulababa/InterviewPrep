# Hash
## Hash Concept
The process of hashing revolves around making retrieval of information faster. In this, data values are mapped to certain "key" values which aim to uniquely identify them using a hash function. These key-value pairs are stored in a data structure called a hash map. Values can be inserted, deleted, searched and retrieved quickly from a hash map.
### 1. Hash Function
A hash function is any function that can be used to map data of arbitrary size to fixed-size values. The values returned by a hash function are called hash values, hash codes, digests, or simply hashes. 
### 2. Hash Table
The values are usually used to index a fixed-size table called a hash table.
### 3. Hashing
Use of a hash function to index a hash table is called hashing or scatter storage addressing.

### 4. Difference between Hash Table and Hashing:
|Hashing|Hash Table|
|----|----|
|Hashing is the process of transforming any given key or a string of characters into another value.|Hash Table is a container to store the key-value pairs.|
|Hashing is a built-in method. It can be defined by users also.|Hash table, HashMap, HashSet in  Java and map, multimap, unordered_map, set etc. in C++ uses hashing to store data.|
|Hashing is used to generate a hashcode which is of type Integer.|Based on our needs we can use any type of hash table.|
|Hashing uses the same process for every key to generate hashcodes.|Hash Table generally works as a lookup table to check the keys we already came across and update or change the values being mapped with them or insert a new key in the table.|

### 5. Most common hash data structure
- HashSet/Set 
- HashTable
  
## Hash Collision
  * ### Collision 
    When hashing functions are poorly chosen, collisions are observed in the table. When multiple values lead to the same key value, then collisions are said to have occurred.
  * ###  Resolution
    Since, we can't overwrite old entries from a hash table, we need to store this new inserted value at a location different than what its key indicates. This adjustment in the hash table to accommodate new values is termed as collision resolution.
    + #### Open Addressing
        The general thought process of this technique is to find a different empty location in the hash table to store the element. 
        - Linear probing: Find the very next empty location. If $h(k)$ is ocuppied, we check $h(k)+1$. If $h(k)+1$ fails, then $h(k)+2$,$h(k)+3$ ... until vacancy is found. However, linear probing leads to clustering of entries in the table, making searches slower and more cumbersome.
        - Quadratic probing: The table is traversed in the order h(k)+1, h(k)+4, h(k)+9, h(k)+16 and so on.
        - Double hashing: we use two hashing functions- h(n) for general hashing and and a new function h'(n) used specifically for resolving conflicts. So, vacancies are searched in the order as h(k), h(k) + h'(k), h(k) + 2h'(k) and so on...
        - Advantages: Open Addressing techniques are highly efficient in memory usage as elements are stored in the space already allocated for the hash table. No extra space is required.
        - Disadvantages: But due to clustering, searching is slower. In the worst case, when the hash table is at full capacity, we would have to check every cell in the hash table to determine if the element exists in the hash table or not.
    + ### Close Addressing
        Closed addressing techniques involves the use of chaining of entries in the hash table using linked lists. So, every entry in the hash table leads to a linked list of all the elements that were hashed to a particular key value. 
        - Advantages: Advantages of using closed addressing technique is its easy implementation, as well as the surety that if the element is present in the hash table, it will only be found in the linked list at its key. Deletion is also quick and simple in chaining.
        - Disadvantages:  Chaining leads to inefficient use of memory as some keys might never be used at all but have still been allocated space in the table. We also need extra memory allocation to store the elements as nodes in the linked list. In the worst case, chaining can lead to linear time complexity for searching.
        
## HashSet
  * ### Usage of HashSet
    A HashSet is usually used for high-performance operations involving a set of unique data.
  * ### HashSet Operaions and Time Complexity
    - Add O(1), Remove O(1) and Contains O(1)

## HashTable
  * ### Usage of HashTable
    Fast exist storage checking and adding new mapping k/v pair.
  * ### HashTable Operaions and Time Complexity
    - #### Open addressing
      |ACTIVITY|BEST CASE COMPLEXITY|AVERAGE CASE COMPLEXITY|WORST CASE COMPLEXITY|
      | ----| ---- | ---- | ---- |
      |Searching|O(1)|O(1)|O(n)|
      |Insertion|O(1)|O(1)|O(n)|
      |Deletion|O(1)|O(1)|O(n)|
      |Space Complexity|O(n)|O(n)|O(n)|
    - #### Close addressing (chaining)
      |ACTIVITY|BEST CASE COMPLEXITY|AVERAGE CASE COMPLEXITY|WORST CASE COMPLEXITY|
      | ----| ---- | ---- | ---- |
      |Searching|O(1)|O(1)|O(n)|
      |Insertion|O(1)|O(1)|O(n)|
      |Deletion|O(1)|O(1)|O(n)|
      |Space Complexity|O(m+n)|O(m+n)|O(m+n)|
      
      **where m is the size of the hash table and n is the number of items inserted. This is because linked nodes are allocated memory outside the hash map.**

