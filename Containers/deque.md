#### 3. deque

双端队列是序列容器，两端具有扩张和收缩的特性。

它们类似于vector，但在插入和删除元素时效率更高。与vector不同，**连续存储分配可能无法保证**。

双端队列基本上是数据结构双头队列的一种实现。队列数据结构只允许在末尾插入，从前面删除。这就像现实生活中的一个队列，人们从前面被移走，在后面添加。双端队列是队列的一种特殊情况，在这种情况下，两端都可以执行插入和删除操作。 deque的函数与vector相同，在前面和后面都添加了push和pop操作。

- [deque insert() function in C++ STL](https://www.geeksforgeeks.org/deque-insert-function-in-c-stl/): Inserts an element. And returns an iterator that points to the first of the newly inserted elements.
- [deque rbegin() function in C++ STL](https://www.geeksforgeeks.org/deque-rbegin-function-in-c-stl/): Returns a reverse iterator which points to the last element of the deque (i.e., its reverse beginning).
- [deque rend() function in C++ STL](https://www.geeksforgeeks.org/deque-rend-function-in-c-stl/): Returns a reverse iterator which points to the position before the beginning of the deque (which is considered its reverse end).
- [deque cbegin() in C++ STL](https://www.geeksforgeeks.org/deque-cbegin-in-c-stl/): Returns a constant iterator pointing to the first element of the container, that is, the iterator cannot be used to modify, only traverse the deque.
- [deque max_size() function in C++ STL](https://www.geeksforgeeks.org/deque-max_size-function-in-c-stl/): Returns the maximum number of elements that a deque container can hold.
- [deque assign() function in C++ STL](https://www.geeksforgeeks.org/deque-assign-function-in-c-stl/): Assign values to the same or different deque container.
- [deque resize() function in C++ STL](https://www.geeksforgeeks.org/deque-resize-function-in-c-stl/): Function which changes the size of the deque.
- [deque::push_front() in C++ STL](https://www.geeksforgeeks.org/dequepush_front-c-stl/): This function is used to push elements into a deque from the front.
- [deque::push_back() in C++ STL](https://www.geeksforgeeks.org/dequepush_back-c-stl/): This function is used to push elements into a deque from the back.
- [deque::pop_front() and deque::pop_back() in C++ STL](https://www.geeksforgeeks.org/dequepop_front-dequepop_back-c-stl/): **pop_front()** function is used to pop or remove elements from a deque from the front. **pop_back()** function is used to pop or remove elements from a deque from the back.
- [deque::front() and deque::back() in C++ STL](https://www.geeksforgeeks.org/dequefront-dequeback-c-stl/): **front()** function is used to reference the first element of the deque container. **back()** function is used to reference the last element of the deque container.
- [deque::clear() and deque::erase() in C++ STL](https://www.geeksforgeeks.org/dequeclear-dequeerase-c-stl/): **clear()** function is used to remove all the elements of the deque container, thus making its size 0. **erase()** function is used to remove elements from a container from the specified position or range.
- [deque::empty() and deque::size() in C++ STL](https://www.geeksforgeeks.org/dequeempty-dequesize-c-stl/): **empty()** function is used to check if the deque container is empty or not. **size()** function is used to return the size of the deque container or the number of elements in the deque container.
- [deque::operator= and deque::operator[\] in C++ STL](https://www.geeksforgeeks.org/dequeoperator-dequeoperator-c-stl/):
  **operator=** operator is used to assign new contents to the container by replacing the existing contents. **operator[]** operator is used to reference the element present at position given inside the operator.
- [deque::at() and deque::swap() in C++ STL](https://www.geeksforgeeks.org/dequeat-dequeswap-c-stl/): **at()** function is used reference the element present at the position given as the parameter to the function. **swap()** function is used to swap the contents of one deque with another deque of same type and size.
- [deque::begin() and deque::end in C++ STL](https://www.geeksforgeeks.org/dequebegin-dequeend-c-stl/): **begin()** function is used to return an iterator pointing to the first element of the deque container. **end()** function is used to return an iterator pointing to the last element of the deque container.
- [deque::emplace_front() and deque::emplace_back() in C++ STL](https://www.geeksforgeeks.org/deque-emplace_front-deque-emplace_back-cpp-stl/): **emplace_front()** function is used to insert a new element into the deque container. The new element is added to the beginning of the deque. **emplace_back()** function is used to insert a new element into the deque container. The new element is added to the end of the deque.

#### 