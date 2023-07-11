## Searching algorithms

Linear search is a sequential searching algorithm<br>
- You look at each value one by one, comparing to the value your looking for<br>
- if a value does not match, move onto the next one
- do this till you have gone through the whole list

```py
for i in list:
  if i == 5:
      return True
  else:
    pass
```

Efficient for small lists, can work on both ordered and unordered lists


<b>Binary search</b> is another searching algorithm<br>
This includes finding the middle value, comparing number. If number is the one you want, stop.<br>
if number is less than the number your finding, remove left half of list<br>
if number is higher than numebr your finding, remove right half of list<br><br>
Repeat previous 3 lines, until you reach your number

Time complexity of O(log n)


My approach to coding it
```py
while len(list) != 1:
    index = int((len(list)+1)/2)
    middle = list[index]
    print(middle)
    if middle == 49:
        print("FOUND IT")
        break
    else:
        if middle < 49:
            del list[0:index]
        elif middle > 49:
            del list[index:-1]
```

Best way to code it
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

You can use logarithm to find how many iterations it will take a binary seach to find a number in a list<br>
Logarithmic notation is log2(8) = 3<br>
Exponential notation is 2x2x2 = 8  (three 2s)
