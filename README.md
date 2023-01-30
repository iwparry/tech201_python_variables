# Tech 201 Python Variables

### What are variables?
A variable can be thought of as an object that stores data in our code we set these as shown below:

`variable_name = variable_data`

Here are some examples of variables

- `a = 1`
- `b = 3.5`
- `c = "Hello World!"`

In these examples we have assigned each variable a different data type:

`a` in our example has been assigned an integer value, which is a whole number.

`b` has been assigned a floating point number, which represent real numbers and is written with a decimal point.

And `c` has been assigned a string, which is a sequence of characters and we represent a string typically by using single or double quotes (' ', or " ").

We are able to verify the data types of our variables by using a couple of Python's built-in functions, being the `type()` function which takes a variable as its argument and the `print()` function to print the results to our Python console.

```
print(type(a))               # prints <class 'int'>
print(type(b))               # prints <class 'float'>
print(type(c))               # prints <class 'str'>   
```

### What can we do with variables?
There are a variety of things we can do with variables, one of the most basic being printing as shown in the data types example.
```
print(a)                 # returns 1 to our console
```
Python's built-in function `print()` can take variables as arguments and will return the value stored in the variable as shown above.
We can also perform operations on our variables.

For example:
```
a = 1
b = 3.5
print(a + b)            # returns 4.5 to our console  
```
Here it doesn't matter that `a` is has data type `int` and `b` has data type `float` Python will still perform the operation which makes sense in this instance since both types are numeric, but what if we were to attempt this with a string instead of a float in this instance?
```
a = 1                        # int
c = "Hello World!"           # str
print(a + c)                 # this returns a TypeError
```
The reason we get a `TypeError` in this instance is because Python cannot perform the operation in question with a `int` and a `str` variable, same applies with a `float` and `str`. 
However
```
h = "Hello "                    # str
w = "World!"                    # str
print(h + w)                    # returns Hello World!
```
Python is able to perform the `+` operator on strings (known as string concatenation) and it simply combines the two strings, if we were to convert our variables `a` and `b` into strings we would get:
```
print(str(a) + str(b))              # returns 13.5
```
Here we convert the data types of variables `a` and `b` by using `str()` and then performing the operation, known as concatenation. Python doesn't recognise the numerical values of any string data type, strings are simply a sequence of characters.

Note that variables are mutable, meaning that they can be changed after they are created, for example:
```
a = 1
print(a)                     # this will return 1
a = 4
print(a)                     # this will return 4
```
Python executes the code line by line, meaning if a variable  is changed at any point in the code Python recognises the value we set later. In the above example if we were to add more print statements after we set `a = 4` we would get 4 printed to our console for each print statement since by then Python has recognised that  we changed the value of `a` at some point in our code. 