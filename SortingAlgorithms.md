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
## Insertion sort

