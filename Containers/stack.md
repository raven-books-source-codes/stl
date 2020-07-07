Stacks are a type of container adaptors with LIFO(Last In First Out) type of working, where a new element is added at one end and (top) an element is removed from that end only.

The functions associated with stack are:

1. [empty()](https://www.geeksforgeeks.org/stack-empty-and-stack-size-in-c-stl/) – Returns whether the stack is empty – Time Complexity : O(1)
2. [size()](https://www.geeksforgeeks.org/stack-empty-and-stack-size-in-c-stl/) – Returns the size of the stack – Time Complexity : O(1)
3. [top()](https://www.geeksforgeeks.org/stack-top-c-stl/) – Returns a reference to the top most element of the stack – Time Complexity : O(1)

4. [push(g)](https://www.geeksforgeeks.org/stack-push-and-pop-in-c-stl/) – Adds the element ‘g’ at the top of the stack – Time Complexity : O(1)

5. [pop()](https://www.geeksforgeeks.org/stack-push-and-pop-in-c-stl/) – Deletes the top most element of the stack – Time Complexity : O(1)

```c++
// CPP program to demonstrate working of STL stack 
#include <bits/stdc++.h> 

using namespace std; 

void showstack(stack <int> s) 
{ 
	while (!s.empty()) 
	{ 
		cout << '\t' << s.top(); 
		s.pop(); 
	} 
	cout << '\n'; 
} 

int main () 
{ 
	stack <int> s; 
	s.push(10); 
	s.push(30); 
	s.push(20); 
	s.push(5); 
	s.push(1); 

	cout << "The stack is : "; 
	showstack(s); 

	cout << "\ns.size() : " << s.size(); 
	cout << "\ns.top() : " << s.top(); 


	cout << "\ns.pop() : "; 
	s.pop(); 
	showstack(s); 

	return 0; 
} 

```

