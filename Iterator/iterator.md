Iterator类似于指针，指向container中的元素，但是它们和指针却大不相同。

stl中的iterator可被分为5类。如下图，越外面的越powerful, 越内部的越least powerful.

![img](https://media.geeksforgeeks.org/wp-content/uploads/C_Iterator.jpg)

不同的contaienr支持的iterator不同，vector支持 Random-access iterators, list 支持 bidiectional iterators. 下图总结了container的iterators支持情况：

![img](https://media.geeksforgeeks.org/wp-content/uploads/C_Iterator_Support.jpg)

1. [**Input Iterators**](https://www.geeksforgeeks.org/input-iterators-in-cpp/): They are the weakest of all the iterators and have very limited functionality. They can only be used in a single-pass algorithms, i.e., those algorithms which process the container sequentially, such that no element is accessed more than once.
2. [**Output Iterators**](https://www.geeksforgeeks.org/output-iterators-cpp/): Just like [input iterators](https://www.geeksforgeeks.org/input-iterators-in-cpp/), they are also very limited in their functionality and can only be used in single-pass algorithm, but not for accessing elements, but for being assigned elements.
3. [**Forward Iterator**](https://www.geeksforgeeks.org/forward-iterators-in-cpp/): They are higher in the hierarachy than[ input](https://www.geeksforgeeks.org/input-iterators-in-cpp/) and [output iterators](https://www.geeksforgeeks.org/output-iterators-cpp/), and contain all the features present in these two iterators. But, as the name suggests, they also can only move in a forward direction and that too one step at a time.
4. [**Bidirectional Iterators**](https://www.geeksforgeeks.org/bidirectional-iterators-in-cpp/): They have all the features of[ forward iterators](https://www.geeksforgeeks.org/forward-iterators-in-cpp/) along with the fact that they overcome the drawback of [forward iterators](https://www.geeksforgeeks.org/forward-iterators-in-cpp/), as they can move in both the directions, that is why their name is bidirectional.
5. [**Random-Access Iterators**](https://www.geeksforgeeks.org/random-access-iterators-in-cpp/): They are the most powerful iterators. They are not limited to moving sequentially, as their name suggests, they can randomly access any element inside the container. They are the ones whose functionality are same as pointers.

![img](https://media.geeksforgeeks.org/wp-content/uploads/iteratorOperation.jpg)

使用iterator的benefits：

1. 方便编程，如，在遍历数组时，如果我们使用 [] 符号访问元素，我们需要keep track of arr size. 但是使用iterator，我们有 end() 函数
2. 提高代码复用率
3. 动态处理container，使用iterator insert和erease 元素。

一些常用函数：

**1. begin()** :- This function is used to return the **beginning position** of the container.

**2. end()** :- This function is used to return the ***after\* end position** of the container.

**3. advance()** :- This function is used to **increment the iterator position** till the specified number mentioned in its arguments.

**4. next()** :- This function **returns the new iterator** that the iterator would point after **advancing the positions** mentioned in its arguments.

**5. prev()** :- This function **returns the new iterator** that the iterator would point **after decrementing the positions** mentioned in its arguments.

**6. inserter()** :- This function is used to **insert the elements at any position** in the container. It accepts **2 arguments, the container and iterator to position where the elements have to be inserted**.