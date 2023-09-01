# Anagram detection
an anagram is **two strings that contain same letters**<br>
we can use an algorithm that:<br>
            - sorts the two strings **into alphabetical order**<br>
            - compare two sorted strings, if same, they are anagrams
  
```py
def is_anagram(s1,s2):
    s1 = s1.replace(" ", "")
    s2 = s2.replace(" ", "")
    if sorted(s1) == sorted(s2):
        return True
    else:
        return False
    
print(is_anagram("car", "arc"))
# returns true
```
anagrams are case sensitive and can contain multiple words: therefore we ```s1 = s1.replace(" ", "")``` to **remove any spaces , and convert all to lowercase**<br>
Then uses ``py sorted()``` function to sort, and then compare

# Palindrome detection
A **Palindrome** is a word that reads backwards and forwards the same<br>
to check this, we can reverse the string using ```py [::-1]```, and compare<br>

```py
def is_palindrome(s1):
    if s1.lower() == (s1[::-1]).lower():
        return True
    return False
```
**return breaks a function** and ends it completely. So if it returns True it does not get to return False<br>
again **capitilization can affect comparision**, so we use ```py .lower()``` aswell

The **time complexity** of this algorithm. The dominant term is the slicing. This visits every time in the list to reverse it. Its complexity is ```O(n)```. Making the algorithm run time ``O(n)``

# Last digit 
return the rightmost digit in a string

my way
```py
def right_int(s1):
    all_int = []
    for char in s1:
        if char.isdigit():
            all_int.append(char)
    print(all_int[-1])
```

### **list comprehension**<br>
to create a list based on the values of an existing list<br>
to create a new, altered list from an existing **iterable** (like another list)
an iterable is a **python object that can be iterated through**, and can return all its elements, such as a list

**Advantage**: use a more optimized internal mechanism for iterating over the collection.<br>
**performs transformations and filtering in a single statement**, therefore **more concise, efficient code**. Using a loop is excess lines.

the template syntax for list comprehension:<br>
```py
new_list = [expression(i) for i in iterable if filter(i)]
```
**expression(i)** is a variable that holds each element from the iterable, and adds it to the new list.<br>
**for i in iterable** is traversing through the iterable<br>
**if filter(i)** will be the condition, to make changes to the original iterable

```py
newList = [val for val in "selftaught"]
print(newList)
```
its not just a list, an **iterable**! so it can be a string aswell that you iterate through<br>
here I just create a new list of each individual char value of the string

```py
newList = [val for val in "Buy 1 get 2 free" if val.isdigit()]
print(newList[-1])
```
**Time complexity**: O(n), because iterating through a string once<br>
shorter, reable code


# Caeser Cipher
> **Cipher** = an algorithm for encryption or decryption<br>

Caeser Cipher shifted the alphabet by a certain number. If the letter would go past the last letter, it wraps around back to the first letter.
The key to this is using **modulo arithmetic**<br>
            - numbers wrap around at a specific value<br>
            - such as a clock that wraps around 12 to go back to 1<br>
this is caused by the **modulos**. For example 7 oclock add 8 hours is 15, but its **3** modulos 12

```py
import string


def CaeserCipher(a_string, key):
    encrypt = ""
    uppercase = string.ascii_uppercase
    lowercase = string.ascii_lowercase

    for letter in a_string:
        if letter in uppercase:
            newLetter = (uppercase.index(letter) + key) % 26
            encrypt += lowercase[newLetter]
        elif letter in lowercase:
            newLetter = (lowercase.index(letter) + key) % 26
            encrypt += uppercase[newLetter]
    return encrypt



print(CaeserCipher("hello", 2))
```
**Time complexity**: O(n)
Due to the for loop that iterates through the string
