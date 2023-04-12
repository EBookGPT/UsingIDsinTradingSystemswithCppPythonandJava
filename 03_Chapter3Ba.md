# Chapter 3: Basic Data Structures for IDs

Welcome, dear reader, to the third chapter of our book on Using IDs in Trading Systems with Cpp, Python, and Java. In the previous chapter, we had the honor of having Bjarne Stroustrup join us for an overview of IDs in Trading Systems. In this chapter, we will focus on the basic data structures used for handling IDs.

An ID is a unique identifier that distinguishes one object from another. IDs are commonly used in Trading Systems to represent different entities such as orders, trades, accounts, and portfolios. Efficient management and processing of IDs are critical to ensure robust and scalable trading systems.

To properly handle IDs, we need to use appropriate data structures that can efficiently store, retrieve, and manipulate IDs. In this chapter, we will discuss some of the basic data structures that can be used to manage IDs, including arrays, lists, maps, and sets.

We will also demonstrate how these data structures can be implemented in Cpp, Python, and Java. By the end of this chapter, you will have a solid understanding of the basic data structures used for handling IDs in Trading Systems and how to implement them in your code.

So, let us dive into the world of basic data structures for IDs!
# Chapter 3: Basic Data Structures for IDs

Welcome, dear reader, to the third chapter of our book on Using IDs in Trading Systems with Cpp, Python, and Java. In this chapter, we have a special guest joining us once again, Bjarne Stroustrup, the creator of C++. We will be presenting a Sherlock Holmes mystery that will teach us the importance of using the proper data structure for IDs and how it impacts the performance of our Trading System.

## Mystery: The Case of the Untracked Orders

Sherlock Holmes had received a request from a prominent trading firm to investigate a problem with their trading system. The system had been experiencing slow processing times and missing orders, causing significant financial losses. Holmes set out to investigate the issue, starting with a review of the system's code.

Upon examining the code, Holmes noticed that the IDs of the orders were stored in an array. Furthermore, for each order, the system would iterate through the entire array to find a match for the order ID. This approach worked fine when the system was handling a small number of orders, but as the order count increased, the processing time and the complexity of the code grew exponentially.

To improve system performance, Holmes recommended replacing the array with a hash table, which would optimize the search for the order IDs. However, the trading firm had already tried using a hash table and it did not improve their system's performance. Holmes could not accept this defeat and continued to investigate.

After analyzing the hash table implementation used by the trading firm, Holmes noticed that they had mistakenly used a linked list to resolve hash collisions. A linked list is a data structure where each element contains a reference to the next element, which turned out to be a bottleneck for the system.

## Resolution: The Importance of Choosing the Correct Data Structure

After the design flaw in the system was discovered, Holmes recommended using separate chaining, resolving hash collisions by using a vector of elements rather than a list. This simple change drastically improved the system's performance and the trading firm was astonished by the results.

As Bjarne Stroustrup explained, choosing the correct data structure is crucial to the performance of a system. Hash tables are commonly used to manage IDs, as they allow for constant-time searching of the identifiers. However, we must also consider other factors such as the size and complexity of the data, the frequency of access, and the performance requirements of the system. The wrong choice of a data structure can cause significant performance degradation, as was the case in this Sherlock Holmes mystery.

In conclusion, the detectives in this case learned about the importance of choosing the right data structure for their system. By using arrays, linked lists, and hash tables, traders can efficiently handle IDs in Cpp, Python, and Java. The use case described above highlights the need to weigh the advantages and disadvantages of each data structure to ensure that our system is operating optimally. With this knowledge, you can confidently use the right data structure for IDs to improve the performance of your Trading System.
To resolve the Sherlock Holmes mystery presented in the previous section, the team replaced the linked list with a vector in order to resolve collisions in the hash table more efficiently. 

Here is an example of how you can use vectors in C++, Python, and Java to store IDs:
```cpp
// C++ code using vector to store IDs
#include <vector>
std::vector<int> id_vector;

// Python code using list to store IDs
id_list = []

# Java code using ArrayList to store IDs
import java.util.ArrayList;
ArrayList<String> id_list = new ArrayList<String>();
```

After replacing the linked list for collisions with a vector in the hash table, the Trading System in our Sherlock Holmes mystery was much more efficient. Here is an example of how you could change your C++ code to implement separate chaining with a vector for your hash table:
```cpp
// C++ code for separate chaining with vector
#include <vector>
#include <iostream>
#include <list>

class HashMap {
   private:
      // hash table with vectors for separate chaining
      std::vector<std::list<int>> hash_table;

   public:
      // constructor to set initial size of hash table
      HashMap(int size) {
         hash_table.resize(size);
      }
      // method to add String keys and int values to hash table
      void insert(int id) {
         int hash = id % hash_table.size();
         hash_table[hash].push_back(id);
      }
};
```
In Python, we could use lists instead of vectors:
```python
# Python code for separate chaining with list
hash_table = [[] for _ in range(size)]
def insert(hash_table, key, value):
    hash_key = hash(key) % len(hash_table)
    key_exists = False
    bucket = hash_table[hash_key]    
    for i, kv in enumerate(bucket):
        k, v = kv
        if key == k:
            key_exists = True 
            break
    if key_exists:
        bucket[i] = ((key, value))
    else:
        bucket.append((key, value))
```

And in Java, we could use ArrayLists:
```java
// Java code for separate chaining with ArrayList
import java.util.ArrayList;

class HashMap {
   private ArrayList<ArrayList<Integer>> hash_table = new ArrayList<ArrayList<Integer>>();

   public HashMap(int size) {
      for(int i = 0; i < size; i++) {
         hash_table.add(new ArrayList<Integer>());
      }
   }

   public void insert(int id) {
      int hash = id % hash_table.size();
      hash_table.get(hash).add(id);      
   }
}
```
These examples demonstrate how we can use different data structures such as vectors (in C++), lists (in Python) or ArrayLists (in Java) to efficiently resolve hash collisions in our Trading System implementations.