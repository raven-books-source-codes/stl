

C++ has a class in its STL algorithms library which allows us easy **partition algorithms** using certain inbuilt functions. Partition refers to act of dividing elements of containers depending upon a given condition.

分区算法。

### **Partition operations** **:**

**1. partition(beg, end, condition)** :- This function is used to **partition the elements** on **basis of condition** mentioned in its arguments.

**2. is_partitioned(beg, end, condition)** :- This function returns boolean **true if container is partitioned** else returns false.

例子：

```c++
int main()
{
    vector<int> vect1({1,2,3,4,5});
    // partition based on even or odd
    partition(vect1.begin(),vect1.end(),[](int x){
        return x % 2 == 0;
    });
    // iter
    for(const auto& x : vect1)
    {
        cout << x << " ";
    }
    cout << "\n";
    
    bool ret = is_partitioned(vect1.begin(),vect1.end(),[](int x){
        return x % 2 == 0;
    });
    cout << ret << endl;
    
    return 0;
}
```

**3. stable_partition(beg, end, condition)** :- This function is used to **partition the elements** on **basis of condition** mentioned in its arguments in **such a way that the relative order of the elements is preserved.**.

**4. partition_point(beg, end, condition)** :- This function **returns an iterator pointing to the partition point** of container i.e. the first element in the partitioned range [beg,end) for which condition is not true. The container should already be partitioned for this function to work.

**5. partition_copy(beg, end, beg1, beg2, condition)** :- This function **copies the partitioned elements** in the differenet containers mentioned in its arguments. It takes 5 arguments. **Beginning and ending position of container, beginning position of new container where elements have to be copied (elements returning true for condition), beginning position of new container where other elements have to be copied (elements returning false for condition) and the condition**. **Resizing** new containers **is necessary** for this function.

```c++
bool prediction(int x)
{
    return x % 2 == 0;
}

int main()
{
    vector<int> vect1({1,2,3,4,5});
    auto dist = distance(vect1.begin(),it_partition_point);
    
    // copy
    vector<int> vect2,vect3;
    vect2.resize(dist);
    vect3.resize(vect1.size() - dist);
    partition_copy(vect1.begin(),vect1.end(),vect2.begin(),vect3.begin(),prediction);
    
    print_container(vect1);
    print_container(vect2);
    print_container(vect3);
    
    return 0;
}
```

```c++
1 2 3 4 5
2 4
1 3 5
```

