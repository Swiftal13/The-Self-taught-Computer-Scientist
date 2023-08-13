 ## Data structures
 Detailed notes for each data structure from arrays to BST heaps and stacks

- Arrays (2d,3d..)
- Linked lists
- stacks
- heaps / binary tree structure
- hashtables and maps




# Array 
An array is an **ordered, finite set of elements**, each of the **same data type**<br>
- **Each element has the same memory size**
- **each value is stored in contiguous memory locations**
contiguously means that the memory is allocated consecutively next to eachother, such as in the array

A 1D array is a **linear array**. It can also be 2D, 3D and so on<br><br>

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
a data structure that consists of **ordered items where they can occur more than once**<br><br>
- values **do not have to be same data type**, there can be different types<br>
- list also uses indexing to access elements.<br>
- one difference from an array is: **list values are stored non-contigouosly**

# Common functions
list.append(value) to add data value to end of list <br>
list.insert(value, index) insert a new data value at a specific point in the list<br>
list.remove(value) remove a value from list<br>
list.isEmpty() returns True if list is empty

 

# Tuple 
A tuple is set of ordered elements. However it is <b>immutable</b><br>
this means it cannot be modified 
```py 
TestTuple = (3,9,1)
```
specific values are accessed the same way as a list. **Indexing**<br>
TestTuple[1] will be 9

    
# Record
a Record is one row of fields in a database<br>
each field is a different type of value

you can access each specific field of the record by this format: <br>
- recordName.fieldName <br>
- Students.LastName

# Linked list
A linked list is a **dynamic and recursive data structure** <br>

it is made up of **nodes**, each containing a **data value** and a **pointer**<br>
  - at each node, it has a pointer, which acts as an address to the next node<br>

the first node is called the **head**, and the last node is called the **tail**  
  - the head pointer will point to the first node<br>
  - the last pointer will give the value "Null" . There is no next node. Null means there is no value associated<br>
  - also, when a linked list is empty, the head (first) pointer will point to Null, (no values)<br>

null in binary is all 0's aswell, hence represents no value

to access certain values, we cannot use indexing and instantly get a specific value like an array<br> **THERE IS NO INDEXING**
instead you have to **traverse through each node till you get to the right node**<br>
to get to the 4th node, you have to go 1,2,3 and then finally 4<br><br>

- video: if you add an extra pointer to each node, it can point to previous aswell as next node = **Doubley linked list**<br>
- video: if you make the last node point to the first node, you have created a **circular linked list**<br>
          circular linked list there is no head or tail, no null value either

you can also combine circular and doubley to form **doubley circular**
