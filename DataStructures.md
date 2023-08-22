 ## Data structures
 Detailed notes for each data structure from arrays to BST heaps and stacks

- Arrays (2d,3d..)
- Linked lists
- stacks
- heaps / binary tree structure
- hashtables and maps

# Required context
Primitive data types
- Integer, boolean
- stores on data value

you combine primitive data types to form **compound data types** such as a record data structure

# Static vs Dynamic




# Array 
An array is an **ordered, finite set of elements**, each of the **same data type**<br>
- **Each element has the same memory size**
- **each value is stored in contiguous memory locations**<br>
contiguously means that the memory is allocated consecutively next to eachother, such as in the array, hence we use indexing

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
  - the last pointer will give the value **"Null"** . There is no next node. Null means there is no value associated<br>
  - also, when a linked list is empty, the head (first) pointer will point to Null, (no values)<br>
  ![image](https://github.com/Swiftal13/The-Self-taught-Computer-Scientist/assets/76588047/d33960fe-5a7d-49cd-80f5-093c3c5cbf63)


null in binary is all 0's aswell, hence represents no value


to access certain values, we cannot use indexing and instantly get a specific value like an array<br> **THERE IS NO INDEXING**
instead you have to **traverse through each node till you get to the right node**<br>
to get to the 4th node, you have to go 1,2,3 and then finally 4
This will take O(n) runtime<br><br>


- video: if you add an extra pointer to each node, it can point to previous aswell as next node = **Doubley linked list**<br>
- video: if you make the last node point to the first node, you have created a **circular linked list**<br>
          circular linked list there is no head or tail, no null value either

you can also combine circular and doubley to form **doubley circular**


# Graph

a graph is a **set of vertices or nodes** connected by **edges**<br>
it is used to **represent relationships between a set of objects**<br><br>

**3 Qualities:**<br>
**Directed graph**: The edges can only be **traversed in one direction**. They have a **direction** <br>
**Undirected graph**: The edges can be **traversed in both directions** forward and back<br>
**Weighted graph**: The edges have a **unique cost** to go across each edge
weighted probalistic outcomes

![image](https://github.com/Swiftal13/The-Self-taught-Computer-Scientist/assets/76588047/8c95cec3-aa16-4ece-ade6-4bac09c1f8ec)

**3 types of graphs**<br>
**Null graph** - **no edges** in the graph (no connections between each vertice/node)<br>
**Trivial graph** - graph with only **one vertex**

**A cycle** is a closed path, i.e. a path that starts and ends at the same node **(and no node is visited more than once)**


# Stack
A stack is a **LIFO (Last in First out)** data structure<br>
It is an abstract data structure, that serves as a collection of elements<br>
- the latest element added, would be the first element removed (imagine a stack of elements, only add and remove from the top)<br><br>

**Push(data)** - To add an element to the top of the stack<br>
**Pop()** - To remove the most recent element from top of the stack<br>
**Peak()** - returns a copy of the element on the top of the stack without removing it<br>
**is_empty()** - checks whether a stack is empty<br>
**is_full()** - checks whether a stack is at maximum capacity when stored in a static (fixed-size) structure<br><br>

**Stack overflow**<br>
when pushing data to a stack, if there is no more allocated memory, it will raise a buffer overflow, called stack overflow, meaning no more space<br>
**Stack underflow**<br>
when popping data from stack, if it is already empty and nothing to pop, stack underflow error is returned<br>
