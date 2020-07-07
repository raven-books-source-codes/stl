## Unsorted set

Unsorted set是C++11中引入的数据结构。其内部采用hash table实现。All operations on the **unordered_set** takes constant time **O(1)** on an average which can go up to linear time **O(n)** in worst case which depends on the internally used hash function, but practically they perform very well and generally provide a constant time lookup operation.

unsorted set能够使用任何类型的数据结构作为key，但是当使用user-define的数据结构时，需要实现自己的**比较函数。**

### Set vs Unsort set

[Set](http://geeksquiz.com/set-associative-containers-the-c-standard-template-library-stl/) is an ordered sequence of unique keys whereas unordered_set is a set in which key can be stored in any order, so unordered. Set is implemented as a balanced tree structure that is why it is possible to maintain order between the elements (by specific tree traversal). The time complexity of set operations is O(log n) while for unordered_set, it is O(1).

### Methods

For unordered_set many functions are defined among which most users are the size and empty for capacity, find for searching a key, insert and erase for modification.
The Unordered_set allows only unique keys, for duplicate keys unordered_multiset should be used.

**Methods of unordered_set:**

- [insert()](https://www.geeksforgeeks.org/unordered_set-insert-function-in-c-stl/)– Insert a new {element} in the unordered_set container.
- [begin()](https://www.geeksforgeeks.org/unordered_set-begin-function-in-c-stl/)– Return an iterator pointing to the first element in the unordered_set container.
- [end()](https://www.geeksforgeeks.org/unordered_set-end-in-c-stl/)– Returns an iterator pointing to the past-the-end-element.
- [count()](https://www.geeksforgeeks.org/unordered_set-count-function-in-c-stl/)– Count occurrences of a particular element in an unordered_set container.
- [find()](https://www.geeksforgeeks.org/unordered_set-find-function-in-c-stl/)– Search for an element in the container.
- [clear()](https://www.geeksforgeeks.org/unoredered_set-clear-function-in-c-stl/)– Removes all of the elements from an unordered_set and empties it.
- [cbegin()](https://www.geeksforgeeks.org/unordered_set-cbegin-function-in-c-stl/)– Return a const_iterator pointing to the first element in the unordered_set container.
- [cend()](https://www.geeksforgeeks.org/unordered_set-cend-function-in-c-stl/)– Return a const_iterator pointing to past-the-end element in the unordered_set container or in one of it’s bucket.
- [bucket_size()](https://www.geeksforgeeks.org/unordered_set-bucket_size-in-c-stl/)– Returns the total number of elements present in a specific bucket in an unordered_set container.
- [erase()](https://www.geeksforgeeks.org/unordered_set-erase-function-in-c-stl/)– Remove either a single element of a range of elements ranging from start(inclusive) to end(exclusive).
- [size()](https://www.geeksforgeeks.org/unordered_set-size-function-in-c-stl/)– Return the number of elements in the unordered_set container.
- [swap()](https://www.geeksforgeeks.org/unordered_set-swap-function-in-c-stl/)– Exchange values of two unordered_set containers.
- [emplace()](https://www.geeksforgeeks.org/unordered_set-emplace-function-in-c-stl/)– Insert an element in an unordered_set container.
- [max_size()](https://www.geeksforgeeks.org/unordered_set-max_size-in-c-stl/)– Returns maximum number of elements that an unordered_set container can hold.
- [empty()](https://www.geeksforgeeks.org/unordered_set-empty-function-in-c-stl/)– Check if an unordered_set container is empty or not.
- [equal_range](https://www.geeksforgeeks.org/unordered_set-equal_range-in-c-stl/)– Returns range that includes all elements equal to given value.
- [operator= ](https://www.geeksforgeeks.org/unordered_set-operator-in-c-stl/)– Copies (or moves) an unordered_set to another unordered_set and unordered_set::operator= is the corresponding operator function.
- [hash_function() ](https://www.geeksforgeeks.org/unordered_set-hash_function-in-c-stl/)– This hash function is a unary function which takes asingle argument only and returns a unique value of type size_t based on it.
- [reserve()](https://www.geeksforgeeks.org/unordered_set-reserve-function-in-c-stl/)– Used to request capacity change of unordered_set.
- [bucket()](https://www.geeksforgeeks.org/unordered_set-bucket-function-in-c-stl/)– Returns the bucket number of a specific element.
- [bucket_count() ](https://www.geeksforgeeks.org/unordered_set-bucket_count-function-in-c-stl/)– Returns the total number of buckets present in an unordered_set container.
- [load_factor()](https://www.geeksforgeeks.org/unordered_set-load_factor-function-in-c-stl/)– Returns the current load factor in the unordered_set container.
- [rehash()](https://www.geeksforgeeks.org/unordered_set-rehash-function-in-c-stl/)– Set the number of buckets in the container of unordered_set to given size or more.
- [max_load_factor()](https://www.geeksforgeeks.org/unordered_set-max_load_factor-in-c-stl/)– Returns(Or sets) the current maximum load factor of the unordered set container.
- [emplace_hint()](https://www.geeksforgeeks.org/unordered_set-emplace_hint-function-in-c-stl/)– Inserts a new element in the unordered_set only if the value to be inserted is unique, with a given hint.
- [== operator ](https://www.geeksforgeeks.org/unordered_set-operator-in-c-stl-3/)– The ‘\==’ is an operator in C++ STL performs equality comparison operation between two unordered sets and unordered_set::operator== is the corresponding operator function for the same.
- [key_eq()](https://www.geeksforgeeks.org/unordered_set-key_eq-function-in-c-stl/)– Returns a boolean value according to the comparison. It returns the key equivalence comparison predicate used by the unordered_set.
- [operator!=](https://www.geeksforgeeks.org/unordered_set-operator-in-c-stl-2/)– The != is a relational operator in C++ STL which compares the equality and inequality between unordered_set containers.
- [max_bucket_count() ](https://www.geeksforgeeks.org/unordered_set-max_bucket_count-function-in-c-stl/)– Find the maximum number of buckets that unordered_set can have.