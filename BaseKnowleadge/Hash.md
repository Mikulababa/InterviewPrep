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
        + Linear probing: Find the very next empty location. If $h(k)$ is ocuppied, we check $h(k)+1$. If $h(k)+1$ fails, then $h(k)+2$,$h(k)+3$ ... until cacancy is found
## HashSet
  * ### Usage of HashSet
    A HashSet is usually used for high-performance operations involving a set of unique data.
  * ### HashSet Operaions and Time Complexity
    - Add O(1), Remove O(1) and Contains O(1)

## HashTable
  * ### Usage of HashTable
    Fast exist storage checking and adding new mapping k/v pair.
  * ### HashTable Operaions and Time Complexity
    - Insert O(1), Delete O(1), Search O(1)

