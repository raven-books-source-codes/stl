## 1. vector

向量与动态数组一样，当插入或删除元素时，向量可以自动调整自身大小，容器会自动处理向量的存储。向量元素被放置在连续的存储器中，这样就可以使用**迭代器**访问和遍历它们。在向量中，数据是在末尾插入的。

特性：**在末尾插入需要不同的时间，因为有时可能需要扩展数组。移除最后一个元素只需要固定的时间，因为没有调整大小。开始或中间的插入和删除在时间上是线性的。**

### 1. iterator

1. [begin()](https://www.geeksforgeeks.org/vectorbegin-vectorend-c-stl/) – Returns an iterator pointing to the first element in the vector
2. [end()](https://www.geeksforgeeks.org/vectorbegin-vectorend-c-stl/) – Returns an iterator pointing to the theoretical element that follows the last element in the vector
3. [rbegin()](https://www.geeksforgeeks.org/vector-rbegin-and-rend-function-in-c-stl/) – Returns a reverse iterator pointing to the last element in the vector (reverse beginning). It moves from last to first element
4. [rend()](https://www.geeksforgeeks.org/vector-rbegin-and-rend-function-in-c-stl/) – Returns a reverse iterator pointing to the theoretical element preceding the first element in the vector (considered as reverse end)
5. [cbegin()](https://www.geeksforgeeks.org/vector-cbegin-vector-cend-c-stl/) – Returns a constant iterator pointing to the first element in the vector.
6. [cend()](https://www.geeksforgeeks.org/vector-cbegin-vector-cend-c-stl/) – Returns a constant iterator pointing to the theoretical element that follows the last element in the vector.
7. [crbegin()](https://www.geeksforgeeks.org/vectorcrend-vectorcrbegin-examples/) – Returns a constant reverse iterator pointing to the last element in the vector (reverse beginning). It moves from last to first element
8. [crend()](https://www.geeksforgeeks.org/vectorcrend-vectorcrbegin-examples/) – Returns a constant reverse iterator pointing to the theoretical element preceding the first element in the vector (considered as reverse end)

例子：

```c++
#include <iostream>
#include <vector>
using namespace std;

int main()
{
    vector<int> v;
    // push_back
    for (int i = 0; i < 5; ++i) {
        v.push_back(i);
    }
    
    // iterator normal order
    for (auto i = v.begin(); i != v.end(); ++i) {
        cout << *i << " ";
    }
    cout << "\n";
    
    //iterator reverse order
    for (auto ir = v.rbegin(); ir != v.rend(); ++ir) {
        cout << *ir << " ";
    }
    cout << "\n";
    
    // iterator normal order with const
    for (auto ci = v.cbegin(); ci != v.cend(); ++ci) {
        cout << *ci << " ";
    }
    cout << "\n";
    return 0;
}
```

输出：

```
0 1 2 3 4
4 3 2 1 0
0 1 2 3 4
```

### 2. capacity

1. [size()](https://www.geeksforgeeks.org/vectorempty-vectorsize-c-stl/) – Returns the number of elements in the vector.
2. [max_size()](https://www.geeksforgeeks.org/vector-max_size-function-in-c-stl/) – Returns the maximum number of elements that the vector can hold.
3. [capacity()](https://www.geeksforgeeks.org/vector-capacity-function-in-c-stl/) – Returns the size of the storage space currently allocated to the vector expressed as number of elements.
4. [resize(n)](https://www.geeksforgeeks.org/vector-resize-c-stl/) – Resizes the container so that it contains ‘n’ elements.
5. [empty()](https://www.geeksforgeeks.org/vectorempty-vectorsize-c-stl/) – Returns whether the container is empty.
6. [shrink_to_fit()](https://www.geeksforgeeks.org/vector-shrink_to_fit-function-in-c-stl/) – Reduces the capacity of the container to fit its size and destroys all elements beyond the capacity.
7. [reserve() ](https://www.geeksforgeeks.org/using-stdvectorreserve-whenever-possible/)– Requests that the vector capacity be at least enough to contain n elements.

```c++
void capacity_test()
{
    vector<int> v;
    v.reserve(10);
    // push some values
    for (int i = 0; i < 5; ++i) {
        v.push_back(i);
    }
    // print size and capacity info of this vector
    cout << "size:" << v.size() << "\n";
    cout << "capacity:" << v.capacity() << "\n";
    cout << "max size:" << v.max_size() << "\n";
    // shrink to fit size
    v.shrink_to_fit();
    cout << "after shrink, the capacity of this vector:" << v.capacity() << "\n";
    // resize
    v.resize(4);
    cout << "after resize, the size of this vector:" << v.size() << "\n";
    // check if empty
    cout << "is empty?" << v.empty() << "\n";
    
    // iterator
    for(auto i: v)
    {
        cout << i << " " ;
    }
    cout << "\n";
}

int main()
{
    capacity_test();
    return 0;
}
```

输出：

```c++
size:5
capacity:10
max size:1073741823
after shrink, the capacity of this vector:5
after resize, the size of this vector:4
is empty?0
0 1 2 3
```

### 3.Element access:

1. reference operator [g] – Returns a reference to the element at position ‘g’ in the vector
2. [at(g)](https://www.geeksforgeeks.org/vectorat-vectorswap-c-stl/) – Returns a reference to the element at position ‘g’ in the vector
3. [front()](https://www.geeksforgeeks.org/vectorfront-vectorback-c-stl/) – Returns a reference to the first element in the vector
4. [back()](https://www.geeksforgeeks.org/vectorfront-vectorback-c-stl/) – Returns a reference to the last element in the vector
5. [data()](https://www.geeksforgeeks.org/vector-data-function-in-c-stl/) – Returns a direct pointer to the memory array used internally by the vector to store its owned elements.

 

例子：

```c++
void access_test()
{
    vector<int> v;
    v.reserve(5);
    // assign values
    for(int i = 0; i< 5 ; i++)
    {
        v.push_back(i);
    }
    cout << "index 2 value:" << v[2] << "\n";
    cout << "index 3 value:" << v.at(3) << "\n";
    cout << "front value:" << v.front() << "\n";
    cout << "back value: " << v.back() << "\n";
    // get memory region
    int* ptr = v.data();
    cout << "first value of this vector: " << *ptr << "\n";
}
```

### 4.Modifiers

1. [assign() ](https://www.geeksforgeeks.org/vector-assign-in-c-stl/)– It assigns new value to the vector elements by replacing old ones
2. [push_back()](https://www.geeksforgeeks.org/vectorpush_back-vectorpop_back-c-stl/) – It push the elements into a vector from the back
3. [pop_back()](https://www.geeksforgeeks.org/vectorpush_back-vectorpop_back-c-stl/) – It is used to pop or remove elements from a vector from the back.
4. [insert()](https://www.geeksforgeeks.org/vector-insert-function-in-c-stl/) – It inserts new elements before the element at the specified position
5. [erase()](https://www.geeksforgeeks.org/vectorclear-vectorerase-c-stl/) – It is used to remove elements from a container from the specified position or range.
6. [swap()](https://www.geeksforgeeks.org/vectorat-vectorswap-c-stl/) – It is used to swap the contents of one vector with another vector of same type. Sizes may differ.
7. [clear()](https://www.geeksforgeeks.org/vectorclear-vectorerase-c-stl/) – It is used to remove all the elements of the vector container
8. [emplace()](https://www.geeksforgeeks.org/vector-emplace-function-in-c-stl/) – It extends the container by inserting new element at position
9. [emplace_back()](https://www.geeksforgeeks.org/vectoremplace_back-c-stl/) – It is used to insert a new element into the vector container, the new element is added to the end of the vector

insert和emplace的区别：

参考：

1. https://stackoverflow.com/questions/15659292/what-is-difference-between-insert-and-emplace-for-vector-in-c
2. https://stackoverflow.com/questions/4303513/push-back-vs-emplace-back

> `std::vector::insert` **copies** or **moves** the elements into the container by calling copy constructor or move constructor.
> while,
> In `std::vector::emplace` elements are **constructed in-place**, i.e. no copy or move operations are performed.
>
> The later was introduced since C++11 and its usage is desirable if copying your class is a non trivial operation.

example:

```c++
template<class Iter>
void iter(Iter first, Iter last)
{
    while (first != last) {
        cout << *first << " ";
        first++;
    }
    cout << "\n";
}

void modify_test()
{
    vector<int> v;
    
    // assign the array with 10 five times
    v.assign(5, 10);
    // print
    iter(v.begin(), v.end());
    
    // insert to last
    v.push_back(15);
    cout << "after push back:\n";
    iter(v.begin(), v.end());
    
    // remove from last
    cout << "after remove from last:\n";
    v.pop_back();
    iter(v.begin(), v.end());
    
    // insert function test
    v.insert(v.begin(), 5);
    cout << "after insert 5 to the first pos. the first value :" << v.at(0) << "\n";
    
    // insert to last
    v.insert(v.end(), 20);
    
    // clear
    v.clear();
    
    // swap test
    vector<int> v1, v2;
    v1.push_back(1);
    v1.push_back(2);
    v2.push_back(3);
    v2.push_back(4);
    cout << "before swap\n";
    cout << "v1:";
    iter(v1.begin(), v1.end());
    cout << "v2:";
    iter(v2.begin(), v2.end());
    
    v1.swap(v2);
    cout << "after swap\n";
    cout << "v1:";
    iter(v1.begin(), v1.end());
    cout << "v2:";
    iter(v2.begin(), v2.end());
}
```

#### 