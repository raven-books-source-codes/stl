C++98 introduced a special container called valarray to **hold and provide mathematical operations** on arrays efficiently.

- It supports element-wise mathematical operations and various forms of generalized subscript operators, slicing and indirect access.
- As compare to vectors, valarrays are efficient in certain mathematical operations than vectors also.

**Public member functions in valarray class :**

**1. apply()** :- This function **applies the manipulation** given in its arguments **to all** the valarray elements at once and **returns a new valarray** with manipulated values.

**2. sum()** :- This function **returns the summation** of all the elements of valarrays at once.

**3. min()** :- This function returns the **smallest** element of valarray.

**4. max()** :- This function returns the **largest** element of valarray.

**5. shift()** :- This function returns the new valarray after **shifting elements** **by** the **number** mentioned in its argument. If the **number is positive**, **left-shift** is applied, if **number is negative**, **right-shift** is applied.

**6. cshift()** :- This function returns the new valarray after **circularly shifting(rotating)** elements **by** the **number** mentioned in its argument. If the **number is positive, left-circular** **shift** is applied, if **number is negative, right-circular shift** is applied.

**7. swap()** :- This function **swaps** one valarray with other.

```c++
int main()
{
    valarray<int> varr;
    varr.resize(10);
    
    for(size_t i = 0; i < varr.size(); ++i)
    {
        varr[i] = 2*i;
    }
    
    for(const auto& val : varr)
    {
        cout << val << " ";
    }
    cout << endl;
    
    // shift
    varr =varr.cshift(2);
    for(const auto& val : varr)
    {
        cout << val << " ";
    }
    cout << endl;
    
    // min max
    cout << varr.min() << endl;
    cout << varr.min() << endl;
    // sum
    cout << varr.sum() << endl;
    
    // apply
    varr = varr.apply([](int x){return x+5;});
    for(const auto& val : varr)
    {
        cout << val << " ";
    }
    cout << endl;

    return 0;
}
```

