 ## Data structures
 Detailed notes for each data structure from arrays to BST heaps and stacks

- Arrays (2d,3d..)
- Linked lists
- stacks
- heaps / binary tree structure
- hashtables and maps




# Array 
An array is an **ordered, finite set of elements**, each of the **same data type**<br>
Each element has the same memory size . each value is stored contiguously in memory
A 1D array is a linear array. It can also be 2D, 3D and so on<br><br>

At default arrays are always **zero-indexed**, meaning to access the first (1) element, you use the index of [0]
<br><br>
**A 1D array**<br>
```py 
TestArray = [2,5,1,4,8,9,3]
```
To access the second element you do 
```py 
TestArray[1]
```

**A 2D array**<br>
```py 
TestArray = [[1,4,3,6],[5,3,7,1]]
```
To access the 3rd element of the 2nd list you do
```py
TestArray[1,2]
```

# List
similar to array but non contiguous memory placr
values do not have to be same data type
list also uses indexing to access elements.<br>
lists however can contain different data types, not just one

# Common functions
list.append(value) to add data value to end of list
list.insert(value, index)
list.remove(value)
list.isEmpty() returns True if list is empty

 

# Tuple 
A tuple is set of ordered elements. However it is <b>immutable</b>
```py
TestTuple = (3,9,1)
