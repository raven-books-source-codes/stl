Priority queues are a type of container adapters, specifically designed such that **the first element of the queue is the greatest of all elements** in the queue and elements are **in non increasing order**(hence we can see that each element of the queue has a priority{fixed order}).

### Methods of priority queue are:

- [priority_queue::empty() in C++ STL](https://www.geeksforgeeks.org/priority_queueempty-priority_queuesize-c-stl/)– **empty()** function returns whether the queue is empty.
- [priority_queue::size() in C++ STL](https://www.geeksforgeeks.org/priority_queueempty-priority_queuesize-c-stl/)– **size()** function returns the size of the queue.
- [priority_queue::top() in C++ STL](https://www.geeksforgeeks.org/priority_queuetop-c-stl/)– Returns a reference to the top most element of the queue
- [priority_queue::push() in C++ STL](https://www.geeksforgeeks.org/priority_queuepush-priority_queuepop-c-stl/)**– push(g)** function adds the element ‘g’ at the end of the queue.
- [priority_queue::pop() in C++ STL](https://www.geeksforgeeks.org/priority_queuepush-priority_queuepop-c-stl/)– **pop()** function deletes the first element of the queue.
- [priority_queue::swap() in C++ STL](https://www.geeksforgeeks.org/priority_queueswap-c-stl/)– This function is used to swap the contents of one priority queue with another priority queue of same type and size.
- [priority_queue::emplace() in C++ STL ](https://www.geeksforgeeks.org/priority_queueemplace-c-stl/)– This function is used to insert a new element into the priority queue container, the new element is added to the top of the priority queue.
- [priority_queue value_type in C++ STL](https://www.geeksforgeeks.org/priority_queue-value_type-in-c-stl/)– Represents the type of object stored as an element in a priority_queue. It acts as a synonym for the template parameter.

==c++使用max-heap实现priority-queue==

如何实现最小堆？

**每个元素乘以 -1 即可。**

```
// Note that by default C++ creates a max-heap 
// for priority queue 
#include <iostream> 
#include <queue> 

using namespace std; 

void showpq(priority_queue <int> gq) 
{ 
	priority_queue <int> g = gq; 
	while (!g.empty()) 
	{ 
		cout << '\t' << g.top(); 
		g.pop(); 
	} 
	cout << '\n'; 
} 

int main () 
{ 
	priority_queue <int> gquiz; 
	gquiz.push(10); 
	gquiz.push(30); 
	gquiz.push(20); 
	gquiz.push(5); 
	gquiz.push(1); 

	cout << "The priority queue gquiz is : "; 
	showpq(gquiz); 

	cout << "\ngquiz.size() : " << gquiz.size(); 
	cout << "\ngquiz.top() : " << gquiz.top(); 


	cout << "\ngquiz.pop() : "; 
	gquiz.pop(); 
	showpq(gquiz); 

	return 0; 
} 

```

