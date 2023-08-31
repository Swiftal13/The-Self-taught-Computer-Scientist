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
remember the reason we dont need else, is because return breaks a function and ends it completely. So if it returns True it does not get to return False<br>
again capitlization can affect comparision, so we use ```py .lower()``` aswell

