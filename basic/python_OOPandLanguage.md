1. OOP General:
- [Aliasing, Namespace & scope](https://docs.python.org/3/tutorial/classes.html)
- Overloading is not supported by default in python, but you can use [other ways](https://www.geeksforgeeks.org/python-method-overloading/).
- [Polymorphism](https://www.geeksforgeeks.org/polymorphism-in-python/)
- [Encapsulation](https://www.geeksforgeeks.org/encapsulation-in-python/)
- [Abstraction](https://www.geeksforgeeks.org/abstract-classes-in-python/)

2. Python language feature
- Is Python call by reference or call by value?
  <br>Python utilizes a system, which is known as “Call by Object Reference” or <mark>“Call by assignment”</mark>. In 
  the event that you pass arguments like whole numbers, strings or tuples to a function, the passing is like 
  call-by-value because you can not change the value of the immutable objects being passed to the function. 
  Whereas passing mutable objects can be considered as call by reference because when their values are changed inside 
  the function, then it will also be reflected outside the function.
  <br>
- A special quirk of Python is that – if no global or nonlocal statement is in effect – assignments to names always 
  go into the innermost scope.
- Overflow(int bound specifically): [explaination](https://hackmd.io/@y56/SkDyI8efH) (python int are signed int which has 32 bits
  meaning the boundary is inclusive -2^31 to 2^31 -1)

3. Data Manipulation:
- Swap values for two variables: <br>&nbsp;&nbsp;&nbsp;&nbsp;no temp variable needed in python a, b, c = c, b, a

4. String Manipulation:
    - Slicing syntax:
       ```python
       a[start:stop]  # items start through stop-1
       a[start:]      # items start through the rest of the array
       a[:stop]       # items from the beginning through stop-1
       a[:]           # a copy of the whole array
       a[start:stop:step] # start through not past stop, by step
       ```
    - Index range
      ```python
      str = "12"
      str[10:] -> ''
      str[2:] -> ''
      ```
    - not "" -> True; not " " -> False
    - Check palindrome: sub == sub[::-1] Reference: leetcode 4
    - Take tail of string:
        ```python
        s = "dnewkf"
        s[-1] # 'f'
        s[-2] # 'k'
        ```
    - To list:
        ```python
        list(str) # char list
        str.split(" ") # vocabulary list
        ```
    - To str:
        ```python
        x = 345
        y = int(str(x)[::-1]) # reverse int x
        ```

5. Class: Bundle function and data together
- Modifier: 
  - Public: accessible from any class (class member default python/C++)
  - Private: accessible from own class
  - Virtual: can be modified in a derived class by override modifier. (class method default python/C++)
- [Dataclass](https://realpython.com/python-data-classes/)
- [Class Attributes with leading underscores in their names and why](https://stackoverflow.com/questions/1301346/what-is-the-meaning-of-single-and-double-underscore-before-an-object-name)
- [Generator](https://realpython.com/introduction-to-python-generators/): Lazy iterator using yield statement, no return no memory storage:
  - [Yield](https://www.geeksforgeeks.org/use-yield-keyword-instead-return-keyword-python/)
- Initializer: class variable vs. instance variable (self.val)
- A method is a function that “belongs to” an object. 
  <br>Say, x is an instance for class MyClass. Then the call x.f() is
      exactly equivalent to MyClass.f(x). In general, calling a method with a list of n arguments is equivalent to calling the
      corresponding function with an argument list that is created by inserting the method’s instance object before the first argument.

6. Asterisk marks * and ** passing arguments: [usage](https://treyhunner.com/2018/10/asterisks-in-python-what-they-are-and-how-to-use-them/)

7. Condition: if 0/None/[]/"" will break
8. Lambda: assign function with no definition to a variable; v = lambda x: x[0], can be used in sort(key=v)
9. Max int value: [(1<<31) - 1](https://stackoverflow.com/questions/39206842/how-does-1-left-shift-by-31-1-31-work-to-get-maximum-int-value-here-are-my); also check [mod 10^9+7](https://www.geeksforgeeks.org/modulo-1097-1000000007/)