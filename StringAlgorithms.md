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
