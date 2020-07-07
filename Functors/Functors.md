考虑一个只接受一个参数的函数。然而，在调用这个函数时，我们有很多想要传递给这个函数的信息，但是我们不能，因为它只接受一个参数。我们该怎么做？

一个明显的答案可能是全局变量。然而，良好的编码实践并不提倡使用全局变量，并且只在没有其他选择时才使用全局变量。

Functors是可以当作函数或函数指针来处理的对象。Functors最常与stl一起在如下场景中使用:

先看一个例子：

```c++
#include <iostream>
#include <algorithm>
using namespace std;


int increment(int x)
{
    return x+1;
}

int main()
{
    int arr[] = {1,2,3,4,5};
    transform(arr,arr+sizeof(arr)/sizeof(arr[0]),arr,increment);
    
    for(const auto& val : arr)
    {
        cout << val << " ";
    }
    
    return 0;
}
```

考虑现在一个场景，我需要对所有元素 **加5**。

由于increment函数只能接受一个参数，所以我们只好再写一个函数。

那如果我又要加6呢？

难道又要写一个函数?

这就要引出Functors了。Functors是一个C++ class，但是它可以act like a functions. 它的调用方法和普通函数一样。创建一个functors的方法是，创建一个普通类，并且重载 operator():

```c++
The line,
MyFunctor(10);

Is same as
MyFunctor.operator()(10);
```

现在在来看一个例子：

```c++
#include <iostream>
#include <algorithm>

using namespace std;

class increment {
private:
    int num;
public:
    explicit increment(int num) : num(num) {}
    
    int operator()(int factor) const
    {
        return num + factor;
    }
    
};

int main()
{
    int arr[] = {1, 2, 3, 4, 5};
    
    increment increment1(1);
    increment increment2(2);
    increment increment3(3);
    increment increment4(4);
    
    transform(arr, arr + sizeof(arr) / sizeof(arr[0]), arr,increment1);
    
    for (const auto &val : arr) {
        cout << val << " ";
    }
    
    return 0;
}
```

