- **Important Algorithms.md**

- For all those who aspire to excel in competitive programming, only having a knowledge about containers of STL is of less use till one is not aware what all STL has to offer.

- STL has an ocean of algorithms, for all < algorithm > library functions : Refer [**here**](https://www.geeksforgeeks.org/algorithms-library-c-stl/).

- Some of the most used algorithms on vectors and most useful one’s in Competitive Programming are mentioned as follows :
 
1. [**sort**](https://www.geeksforgeeks.org/sort-c-stl/)**(first****iterator, last****iterator)** – To      sort the given vector.
2. **reverse(first****iterator, last****iterator)** – To reverse a vector.
3. ***max****element      (first****iterator, last_iterator)** – To find the maximum element of a vector.
4. ***min****element      (first****iterator, last_iterator)** – To find the minimum element of a vector.
5. **accumulate(first****iterator, last****iterator, initial value of sum)** – Does the summation of      vector elements
6. **count(first****iterator, last****iterator,x)** – To count the occurrences of x in vector.
7. **find(first****iterator, last****iterator, x)** – Points to last address of vector ((name*of*vector).end()) if element is      not present in vector.
8. [**binary_search**](http://quiz.geeksforgeeks.org/binary-search-algorithms-the-c-standard-template-library-stl/)**(first****iterator, last****iterator, x)** – Tests whether      x exists in sorted vector or not.
9. **lower****bound(first****iterator,      last_iterator, x)**      – returns an iterator pointing to the first element in the range      [first,last) which has a value not less than ‘x’.
10. **upper****bound(first****iterator,      last_iterator, x)**      – returns an iterator pointing to the first element in the range      [first,last) which has a value greater than ‘x’.
11. **arr.erase(position to be deleted)** – This erases selected      element in vector and shifts and resizes the vector elements accordingly.
12. arr.erase(unique(arr.begin(),arr.end()),arr.end())      – This erases the duplicate occurrences in sorted vector in a single      line.
13. **next****permutation(first****iterator,      last_iterator)**      – This modified the vector to its next permutation.
14. **prev****permutation(first****iterator,      last_iterator)**      – This modified the vector to its previous permutation.
15. distance(first_iterator,desired_position)      – It returns the distance of desired position from the first      iterator.This function is very      useful while finding the index.
