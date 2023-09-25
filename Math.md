
## Binary
A binary number is a number in the **base 2 numberal system**<br>
```a numeral system is a writing system for expressing numbers```<br><br>

Base 2: only two digits: **0 and 1**<br>
A binary digit is called a bit. 01101, 1 is a bit<br>
the number system represents how many digits there are.<br>
We use base 10, as we count with numbers 1 to 9<br><br>

the same number can be in many different bases. Therefore to indicate what base a number is in, programmers use specific notation.<br>
```100b %1000 b100```

**A place value** is the numerical value a digit has becuase of its position<br>
1543. the number 5 has a place value of 100<br>
The decimal system, each place value is a power of 10<br>
10^0 = 1
10^1 = 10
10^2 = 100 and so on<br><br>

## Bitewise operators
operator to peform operations on individual bits of binary representations of numbers<br>
they work at a **Binary level**<br>

```bin``` to work with binary numbers in python, returns binary value of number<br>

### AND
**And** operator peforms Boolean arithmetic bit by bit<br> It is like python ``and``. **Both conditions must be true**, for result to be True, else False<br>
When both bits are 1 (True), returns 1(True)<br>
When both or one is 0 (False), returns 0 (False)
```py
print(1 and 2)
```
first it compares bit by bit if its 1 or 0 each digit, then it makes a binary number from it that can form a decimal base number<br>
ampersand symbol &
### to check if a number is even or odd
because the binary of number 2 has a **0 at the end**, whereas the number 1 always has **a 1 at the end**
how this works, is 1 is only 1 binary digit, 1 at the end. When you compare the last digit of two things, if its even it will return 0 (false), as the last digit of the even, will be 0, and the 1 is 1 so they are not the same


### OR
works bit by bit, returns 1 when one or more of the two bits is True, returns False when both are False<br>
pipe symbol<br>
similar to **python 

## Highest common factor
- highest number that n1 and n2 are divisible by.
python code
```py
def hcf(n1,n2):
    if n1 < n2:
        smaller = n1
    else:
        smaller = n2
    for i in range(1, smaller + 1):
        if n1 % i == 0 and n2 % i == 0:
            hcf= i
    return hcf
        
print(hcf(8,4))
```
