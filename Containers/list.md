####  2. list

list是允许非连续内存分配的序列容器。和vector相比，list遍历速度较慢，但一旦找到位置，插入和删除都很快。通常，当我们说一个列表时，我们谈论的是**双链**表。为了实现一个单链表，我们使用**forward list**。

list的常用函数：

- [front()](https://www.geeksforgeeks.org/list-front-function-in-c-stl/) – Returns the value of the first element in the list.
- [back()](https://www.geeksforgeeks.org/list-back-function-in-c-stl/) – Returns the value of the last element in the list .
- [push_front(g)](https://www.geeksforgeeks.org/list-push_front-function-in-c-stl/) – Adds a new element ‘g’ at the beginning of the list .
- [push_back(g)](https://www.geeksforgeeks.org/list-push_back-function-in-c-stl/) – Adds a new element ‘g’ at the end of the list.
- [pop_front()](https://www.geeksforgeeks.org/list-pop_front-function-in-c-stl/) – Removes the first element of the list, and reduces size of the list by 1.
- [pop_back()](https://www.geeksforgeeks.org/list-pop_back-function-in-c-stl/) – Removes the last element of the list, and reduces size of the list by 1
- [list::begin() and list::end() in C++ STL](https://www.geeksforgeeks.org/listbegin-listend-c-stl/)– **begin()** function returns an iterator pointing to the first element of the list
- [end()](https://www.geeksforgeeks.org/list-end-function-in-c-stl/)– **end()** function returns an iterator pointing to the theoretical last element which follows the last element.
- [list rbegin() and rend() function in C++ STL](https://www.geeksforgeeks.org/list-rbegin-and-rend-function-in-c-stl/)– **rbegin()** returns a reverse iterator which points to the last element of the list. **rend()** returns a reverse iterator which points to the position before the beginning of the list.
- [list cbegin() and cend() function in C++ STL](https://www.geeksforgeeks.org/list-cbegin-and-cend-function-in-c-stl/)– **cbegin()** returns a constant random access iterator which points to the beginning of the list. **cend()** returns a constant random access iterator which points to the end of the list.
- [list crbegin() and crend() function in C++ STL](https://www.geeksforgeeks.org/list-crbegin-and-crend-function-in-c-stl/)– **crbegin()** returns a constant reverse iterator which points to the last element of the list i.e reversed beginning of container. **crend()** returns a constant reverse iterator which points to the theoretical element preceding the first element in the list i.e. the reverse end of the list.
- [empty()](https://www.geeksforgeeks.org/list-empty-function-in-c-stl/) – Returns whether the list is empty(1) or not(0).
- [insert()](https://www.geeksforgeeks.org/list-insert-in-c-stl/) – Inserts new elements in the list before the element at a specified position.
- [erase()](https://www.geeksforgeeks.org/list-erase-function-in-c-stl/) – Removes a single element or a range of elements from the list.
- [assign()](https://www.geeksforgeeks.org/list-assign-function-in-c-stl/) – Assigns new elements to list by replacing current elements and resizes the list.
- [remove()](https://www.geeksforgeeks.org/list-remove-function-in-c-stl/) – Removes all the elements from the list, which are equal to given element.
- [list::remove_if() in C++ STL](https://www.geeksforgeeks.org/listremove-listremove_if-c-stl/)– Used to remove all the values from the list that correspond true to the predicate or condition given as parameter to the function.
- [reverse()](https://www.geeksforgeeks.org/list-reverse-function-in-c-stl/) – Reverses the list.
- [size()](https://www.geeksforgeeks.org/list-size-function-in-c-stl/) – Returns the number of elements in the list.
- [list resize()function in C++ STL](https://www.geeksforgeeks.org/list-resize-function-in-c-stl/)– Used to resize a list container.
- [sort()](https://www.geeksforgeeks.org/stdlistsort-c-stl/) – Sorts the list in increasing order.
- [list max_size() function in C++ STL](https://www.geeksforgeeks.org/list-max_size-function-in-c-stl/)– Returns the maximum number of elements a list container can hold.
- [list unique() in C++ STL](https://www.geeksforgeeks.org/list-unique-in-c-stl/)– Removes all duplicate consecutive elements from the list.
- [list::emplace_front() and list::emplace_back() in C++ STL](https://www.geeksforgeeks.org/listemplace_front-listemplace_back-c-stl/)– **emplace_front()** function is used to insert a new element into the list container, the new element is added to the beginning of the list. **emplace_back()** function is used to insert a new element into the list container, the new element is added to the end of the list.
- [list::clear() in C++ STL](https://www.geeksforgeeks.org/listclear-c-stl/)– **clear()** function is used to remove all the elements of the list container, thus making it size 0.
- [list::operator= in C++ STL](https://www.geeksforgeeks.org/listoperator-c-stl/)– This operator is used to assign new contents to the container by replacing the existing contents.
- [list::swap() in C++ STL](https://www.geeksforgeeks.org/listswap-c-stl/)– This function is used to swap the contents of one list with another list of same type and size.
- [list splice() function in C++ STL](https://www.geeksforgeeks.org/list-splice-function-in-c-stl/)– Used to transfer elements from one list to another.
- [list merge() function in C++ STL](https://www.geeksforgeeks.org/list-merge-function-in-c-stl/)– Merges two **sorted** lists into one
- [list emplace() function in C++ STL](https://www.geeksforgeeks.org/list-emplace-function-in-c-stl/)– Extends list by inserting new element at a given position.

例子：

```c++
#include <iostream>
#include <list>
using namespace std;


template<class Iter>
void iter(Iter first, Iter last)
{
    while (first != last) {
        cout << *first << " ";
        first++;
    }
    cout << "\n";
}

int main()
{
    list<int> qlist1, qlist2;
    const int n = 5;
    
    // push values
    for (int i = 0; i < n; i++) {
        qlist1.push_back(i * 2);
        qlist2.push_front(i * 3);
    }
    cout << "push values:\n";
    cout << "qlist1:\n";
    iter(qlist1.begin(), qlist1.end());
    cout << "qlist2:\n";
    iter(qlist2.begin(), qlist2.end());
    
    // get values
    cout << "front value of qlist1:" << qlist1.front() << "\n";
    cout << "back balue of qlist2:" << qlist2.back() << "\n";
    
    // insert value in the middle pos
    int ql1_size = qlist1.size();
    auto ql1_iter = qlist1.begin();
    advance(ql1_iter,ql1_size/2); // advance iterator by 2 pos
    
    ql1_iter = qlist1.insert(ql1_iter,10);
    // print result
    cout << "after insert qlist1:\n";
    iter(qlist1.begin(),qlist1.end());
   
    // erase
    qlist1.erase(ql1_iter);
    cout << "after erase qlist1:\n";
    iter(qlist1.begin(),qlist1.end());
    
    cout << "reverse order qlist1:\n";
    iter(qlist1.rbegin(),qlist1.rend());
    
    // reverse qlist1
    qlist1.reverse();
    cout << "rever order qlist1:\n";
    iter(qlist1.begin(),qlist1.end());
    
    // sort
    qlist1.sort();
    cout << "sort qlist1\n";
    iter(qlist1.begin(),qlist1.end());
    
    // splice: add 2 elements of qlist2 into qlist1
    auto ql2_iter = qlist2.begin();
    advance(ql2_iter,2);
    qlist1.splice(qlist1.end(),qlist2,qlist2.begin(),ql2_iter);
    cout << "after splice:\n";
    iter(qlist1.begin(),qlist1.end());
    
    // merge: merge 2 list
    // before merge, we should sort two lists
    qlist1.sort();
    qlist2.sort();
    qlist1.merge(qlist2);
    cout << "after merge:\n";
    iter(qlist1.begin(),qlist1.end());
    
    // swap
    qlist1.swap(qlist2);
    cout << "after swap:\n";
    cout << "qlist1:\n";
    iter(qlist1.begin(),qlist1.end());
    cout << "qlist2:\n";
    iter(qlist2.begin(),qlist2.end());
    
    return 0;
}

```

#### 