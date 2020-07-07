STL中的forward lilst实现了单链表。从C++ 11中介绍，转发列表在插入、删除和移动操作（如排序）中比其他容器有用，并允许元素的**时间常数插入和移除。**

它与list的**不同之处**在于forward list只跟踪下一个元素的位置，而**list则同时跟踪下一个和前一个元素，从而增加了存储每个元素所需的存储空间。**forward list的**缺点是它不能向后迭代**，并且不能直接访问它的各个元素。
当只需要向前遍历时，转发列表比列表优先（与单链表优先于双链表相同），这样可以节省空间。例如， hash 中的链接、图的邻接表表示等。

常用函数：

**1. [assign()](https://www.geeksforgeeks.org/forward_list-assign-function-in-c-stl/)** :- This function is used to assign values to forward list, its another variant is used to assign repeated elements.

**2. [push_front()](https://www.geeksforgeeks.org/forward_listpush_front-forward_listpop_front-c-stl/)** :- This function is used to insert the element at the first position on forward list. The value from this function is copied to the space before first element in the container. The size of forward list increases by 1.

**3. [emplace_front()](https://www.geeksforgeeks.org/forward_listemplace_front-in-cstl/)** :- This function is similar to the previous function but in this no copying operation occurs, the element is created directly at the memory before the first element of the forward list.

**4. [pop_front()](https://www.geeksforgeeks.org/forward_listpush_front-forward_listpop_front-c-stl/)** :- This function is used to delete the first element of list.

**5. [insert_after()](https://www.geeksforgeeks.org/forward_list-insert_after-function-in-c-stl/)** This function gives us a choice to insert elements at any position in forward list. The arguments in this function are copied at the desired position.

**6. [emplace_after()](https://www.geeksforgeeks.org/forward_list-emplace_after-and-emplace_front-in-c-stl/)** This function also does the same operation as above function but the elements are directly made without any copy operation.

**7. [erase_after()](https://www.geeksforgeeks.org/forward_listclear-forward_listerase_after-c-stl/)** This function is used to erase elements from a **particular position** in the forward list.

**8. [remove()](https://www.geeksforgeeks.org/forward_listremove-forward_listremove_if-c-stl/)** :- This function removes the p**articular element** from the forward list mentioned in its argument.

**9. [remove_if()](https://www.geeksforgeeks.org/forward_listremove-forward_listremove_if-c-stl/)** :- This function removes according to the condition in its argument.

**10. [splice_after()](https://www.geeksforgeeks.org/forward_listsplice_after-in-c-stl/)** :- This function transfers elements from one forward list to other.

**11. [front()](https://www.geeksforgeeks.org/forward_listfront-forward_listempty-c-stl/)** – This function is used to reference the first element of the forward list container.

**12. [begin()](https://www.geeksforgeeks.org/forward_listbegin-forward_listend-c-stl/)**– begin() function is used to return an iterator pointing to the first element of the forward list container.

**13.[end()](https://www.geeksforgeeks.org/forward_listbegin-forward_listend-c-stl/)–** end() function is used to return an iterator pointing to the last element of the list container.

**14.[cbegin()](https://www.geeksforgeeks.org/forward_list-cbegin-in-c-stl/)**– Returns a constant iterator pointing to the first element of the forward_list.

**15.[cend()](https://www.geeksforgeeks.org/forward_listcend-in-c-stl-with-example/)**– Returns a constant iterator pointing to the past-the-last element of the forward_list.

**16.[before_begin()](https://www.geeksforgeeks.org/forward_listbefore_begin-in-c-stl/)**– Returns a iterator which points to the position before the first element of the forward_list.

**17.[cbefore_begin()](https://www.geeksforgeeks.org/forward_listcbefore_begin-in-c-stl/)**– Returns a constant random access iterator which points to the position before the first element of the forward_list.

**18.[max_size()](https://www.geeksforgeeks.org/forward_listmax_size-in-c-stl/)**– Returns the maximum number of elements can be held by forward_list.

**19.[resize()](https://www.geeksforgeeks.org/forward_list-resize-function-in-c-stl/)**– Changes the size of forward_list.