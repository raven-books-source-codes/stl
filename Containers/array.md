## 4. array

The introduction of array class from C++11 has offered a better alternative for C-style arrays. The advantages of array class over C-style array are :-

- Array classes **knows its own size,** whereas C-style arrays lack this property. So when passing to functions, we don’t need to pass size of Array as a separate parameter.
- With C-style array there is more risk of [array being decayed into a pointer](https://www.geeksforgeeks.org/what-is-array-decay-in-c-how-can-it-be-prevented/). Array classes don’t decay into pointers. (参数传递的时候，c-like数组退化为指针,但是这里的array不用)
- Array classes are generally **more efficient**, light-weight and reliable than C-style arrays.

常用函数：

**1. at()** :- This function is used to access the elements of array.

**2. get()** :- This function is also used to access the elements of array. This function is not the member of array class but overloaded function from class tuple.

**3. operator[]** :- This is similar to C-style arrays. This method is also used to access array elements.

**4. front()** :- This returns the first element of array.

**5. back()** :- This returns the last element of array.

**6. size()** :- It returns the number of elements in array. This is a property that C-style arrays lack.

**7. max_size()** :- It returns the maximum number of elements array can hold i.e, the size with which array is declared. The size() and max_size() return the same value.

**8. swap()** :- The swap() swaps all elements of one array with other. 注意size应该要相同。

**9. empty()** :- This function returns true when the array size is zero else returns false.

**10. fill()** :- This function is used to fill the entire array with a particular value. 这个用来初始化蛮有用的，避免了memset只能按照单字节初始化。

```c++

int main()
{
    array<int,6> arr1 = {1,2,3};
    array<int,6> arr2 = {3,2,1};
    // print val
    iter(arr1.begin(),arr1.end());
    
    cout << "first val:" << arr1[0] << "\n";
    cout << "the size of this arr:" << arr1.size() << "\n";
    
    // swap
    arr1.swap(arr2);
    iter(arr1.begin(),arr1.end());
    
    // fill
    arr1.fill(100);
    iter(arr1.begin(),arr1.end());
    return 0;
}
```

