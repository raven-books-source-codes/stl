Sets are a type of associative containers in which each element has to be **unique**, because the value of the element identifies it. The value of the element cannot be modified once it is added to the set, though it is possible to remove and add the modified value of that element.

**Some basic functions associated with Set:**

- [begin()](https://www.geeksforgeeks.org/setbegin-setend-c-stl/) – Returns an iterator to the first element in the set.
- [end()](https://www.geeksforgeeks.org/setbegin-setend-c-stl/) – Returns an iterator to the theoretical element that follows last element in the set.
- [size()](https://www.geeksforgeeks.org/setsize-c-stl/) – Returns the number of elements in the set.
- [max_size()](https://www.geeksforgeeks.org/set-max_size-function-in-c-stl/) – Returns the maximum number of elements that the set can hold.
- [empty()](https://www.geeksforgeeks.org/setempty-c-stl/) – Returns whether the set is empty.

**Methods of set:**

- [begin()](https://www.geeksforgeeks.org/setbegin-setend-c-stl/) – Returns an iterator to the first element in the set.
- [end()](https://www.geeksforgeeks.org/setbegin-setend-c-stl/) – Returns an iterator to the theoretical element that follows last element in the set.
- [rbegin()](https://www.geeksforgeeks.org/setrbegin-and-setrend-in-c-stl/)– Returns a reverse iterator pointing to the last element in the container.
- [rend()](https://www.geeksforgeeks.org/setrbegin-and-setrend-in-c-stl/)– Returns a reverse iterator pointing to the theoretical element right before the first element in the set container.
- [crbegin()](https://www.geeksforgeeks.org/set-crbegin-and-crend-function-in-c-stl/)– Returns a constant iterator pointing to the last element in the container.
- [crend() ](https://www.geeksforgeeks.org/set-crbegin-and-crend-function-in-c-stl/)– Returns a constant iterator pointing to the position just before the first element in the container.
- [cbegin()](https://www.geeksforgeeks.org/set-cbegin-and-cend-function-in-c-stl/)– Returns a constant iterator pointing to the first element in the container.
- [cend() ](https://www.geeksforgeeks.org/set-cbegin-and-cend-function-in-c-stl/)– Returns a constant iterator pointing to the position past the last element in the container.
- [size()](https://www.geeksforgeeks.org/setsize-c-stl/) – Returns the number of elements in the set.
- [max_size()](https://www.geeksforgeeks.org/set-max_size-function-in-c-stl/) – Returns the maximum number of elements that the set can hold.
- [empty()](https://www.geeksforgeeks.org/setempty-c-stl/) – Returns whether the set is empty.
- [insert(const g)](https://www.geeksforgeeks.org/set-insert-function-in-c-stl/) – Adds a new element ‘g’ to the set.
- [iterator insert (iterator position, const g)](https://www.geeksforgeeks.org/set-insert-function-in-c-stl/) – Adds a new element ‘g’ at the position pointed by iterator.
- [erase(iterator position)](https://www.geeksforgeeks.org/seterase-c-stl/) – Removes the element at the position pointed by the iterator.
- [erase(const g)](https://www.geeksforgeeks.org/seterase-c-stl/)– Removes the value ‘g’ from the set.
- [clear()](https://www.geeksforgeeks.org/setclear-c-stl/) – Removes all the elements from the set.
- [key_comp()](https://www.geeksforgeeks.org/setkey_comp-in-c-stl/) / [value_comp()](https://www.geeksforgeeks.org/set-value_comp-function-in-c-stl/) – Returns the object that determines how the elements in the set are ordered (‘<‘ by default).
- [find(const g)](https://www.geeksforgeeks.org/set-find-function-in-c-stl/) – Returns an iterator to the element ‘g’ in the set if found, else returns the iterator to end.
- [count(const g)](https://www.geeksforgeeks.org/set-count-function-in-c-stl/) – Returns 1 or 0 based on the element ‘g’ is present in the set or not.
- [lower_bound(const g)](https://www.geeksforgeeks.org/set-lower_bound-function-in-c-stl/) – Returns an iterator to the first element that is equivalent to ‘g’ or definitely will not go before the element ‘g’ in the set.
- [upper_bound(const g)](https://www.geeksforgeeks.org/set-upper_bound-function-in-c-stl/) – Returns an iterator to the first element that is equivalent to ‘g’ or definitely will go after the element ‘g’ in the set.
- [equal_range()](https://www.geeksforgeeks.org/set-equal_range-function-in-c-stl/)– The function returns an iterator of pairs. (key_comp). The pair refers to the range that includes all the elements in the container which have a key equivalent to k.
- [emplace()](https://www.geeksforgeeks.org/setemplace-c-stl/)– This function is used to insert a new element into the set container, only if the element to be inserted is unique and does not already exists in the set.
- [emplace_hint()](https://www.geeksforgeeks.org/set-emplace_hint-function-in-c-stl/)– Returns an iterator pointing to the position where the insertion is done. If the element passed in the parameter already exists, then it returns an iterator pointing to the position where the existing element is.
- [swap()](https://www.geeksforgeeks.org/setswap-c-stl/)– This function is used to exchange the contents of two sets but the sets must be of same type, although sizes may differ.
- [operator= ](https://www.geeksforgeeks.org/set-operator-in-c-stl/)– The ‘=’ is an operator in C++ STL which copies (or moves) a set to another set and set::operator= is the corresponding operator function.
- [get_allocator()](https://www.geeksforgeeks.org/set-get_allocator-in-c-stl/)– Returns the copy of the allocator object associated with the set.

```c++
#include <iostream> 
#include <set> 
#include <iterator> 

using namespace std; 

int main() 
{ 
	// empty set container 
	set <int, greater <int> > s1;		 

	// insert elements in random order 
	s1.insert(40); 
	s1.insert(30); 
	s1.insert(60); 
	s1.insert(20); 
	s1.insert(50); 
	s1.insert(50); // only one 50 will be added to the set 
	s1.insert(10); 

	// printing set s1 
	set <int, greater <int> > :: iterator itr; 
	cout << "\nThe set s1 is : "; 
	for (itr = s1.begin(); itr != s1.end(); ++itr) 
	{ 
		cout << '\t' << *itr; 
	} 
	cout << endl; 

	// assigning the elements from s1 to s2 
	set <int> s2(s1.begin(), s1.end()); 

	// print all elements of the set s2 
	cout << "\nThe set s2 after assign from s1 is : "; 
	for (itr = s2.begin(); itr != s2.end(); ++itr) 
	{ 
		cout << '\t' << *itr; 
	} 
	cout << endl; 

	// remove all elements up to 30 in s2 
	cout << "\ns2 after removal of elements less than 30 : "; 
	s2.erase(s2.begin(), s2.find(30)); 
	for (itr = s2.begin(); itr != s2.end(); ++itr) 
	{ 
		cout << '\t' << *itr; 
	} 

	// remove element with value 50 in s2 
	int num; 
	num = s2.erase (50); 
	cout << "\ns2.erase(50) : "; 
	cout << num << " removed \t" ; 
	for (itr = s2.begin(); itr != s2.end(); ++itr) 
	{ 
		cout << '\t' << *itr; 
	} 

	cout << endl; 

	//lower bound and upper bound for set s1 
	cout << "s1.lower_bound(40) : "
		<< *s1.lower_bound(40) << endl; 
	cout << "s1.upper_bound(40) : "
		<< *s1.upper_bound(40) << endl; 

	//lower bound and upper bound for set s2 
	cout << "s2.lower_bound(40) : "
		<< *s2.lower_bound(40) << endl; 
	cout << "s2.upper_bound(40) : "
		<< *s2.upper_bound(40) << endl; 

	return 0; 

} 

```

