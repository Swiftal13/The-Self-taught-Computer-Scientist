## Bubble sort
Comparing numbers in pairs, swapping them if they are in the wrong order
![image](https://github.com/Swiftal13/The-Self-taught-Computer-Scientist/assets/76588047/0177c791-af05-45d6-989e-738c8249dd48)
- simple to implement
- time complexity is O(n**2), therefore useful for small data sets, but not efficient choice for larger ones

My approach to coding it
```py
def binary_search(list2, n):
    first = 0
    last = len(list2) - 1
    while last >= first:
        mid = (first + last) // 2
        if list2[mid] == n:
            return True
        else:
            if n < list2[mid]:
                last = mid - 1
            else:
                first = mid + 1
                
    return False
```



## Merge sort
Merge sort is a recursive sorting algorithm
merge sort is the process of breaking down a list into single elements, then grouping them into pairs, ordering, grouping into two smaller lists, ordering, and then finally grouping them back into one complete list in the correct order
## Insertion sort
insertion sort is conparing a number to all the prevoous ones before it 
bad for very long data good for short
