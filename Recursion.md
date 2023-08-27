<b>Recursion</b>

An alternative aproach to an iterative process via loops, you can use recursion instead
- it can be less lines of code more efficient 
- more elegent concise

- A function is called to be executed
- however inside a function there can be a line that calls the function aswel
- therefore the function continually calls itself

  The recursive manner stops until a certain condition is met called: Base Case
This is similar to a while loop running until the certain condition is false

```py
def factorial(n):
    if n == 1:
      return 1
    else:
      n -= 1
      n * factorial(n-1)
  ```

recursion works with a **call stack**. **Stack data structure**<br> 
It is made of frames, each are function calls<br>
It adds each one on top of eachother, then rewinds it back down like LIFO<br>
Everytime it recursive pass goes, it adds a frame to the stack.
Then, when it reaches the base case. IT goes back down the call stack. this works when printing the number.<br>

With recursion and call stacks. Two things are created. Stack overflow and stack
