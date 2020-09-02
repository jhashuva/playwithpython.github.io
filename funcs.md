## Functions

Functions are first class objects in python. Function is a piece of code or set of instructions to carry out specific task.

- Functions may take single or multipule inputs to carry out the the task and sometimes they may not take input.
- After carried out specific task, functions may return single or multipule values or may not return any values.

There are three types of functions available in python:

- Built-in functions
- User Defined Functions(UDFs)
- Anonymus functions

You can find about Built-in functions [here](https://docs.python.org/3/library/functions.html)

### User Defined Functions(UDF)

- The keyword def introduces a function definition.
- It must be followed by the function name and the parenthesized list of formal parameters.
- The statements that form the body of the function start at the next line, and must be indented.
- The first statement of the function body can optionally be a string literal; this string literal is the function’s documentation string, or docstring.
- End your function with a return statement if the function should output something. Without the return statement, your function will return an object None.

Syntax:

```markdown
def functionName(<parsmeters>):
    """function documentation goes here""""
    code goes here
    return something or nothing
```

Syntax for calling the function

```markdown
functionName(<parametervalues>)
```
Example 1:
simple function

```python
def greeting():
    """greeting will greet you"""
    return "Welcome to python functions"
```
We can call the above declared function <code>greeting</code> like this:

```python
greeting() #return 'Welcome to python functions'
```
The above function call will return <code>Welcome to python functions</code>
If you try the <code>greeting.__doc__</code>. It will print :

```markdown
greeting will greet you
```
Docstrings are very useful for the programmers to know what really the function does.

Example 2:

Creating a function with argument(s):

```python
def greeting(a):
    """greeting requires 1 argument to greet you"""
    return a+' Welcome to python functions'
```
You need to call <code>greeting</code> function with the argument.

```python
greeting('Joshua') #str given as an argument
```
This will return us the output:

```markdown
Joshua Welcome to python functions
```

- You can store the function call in another variable like this

```python
b = greeting("Blake")
print(b)
```
output:
```markdown
Blake Welcome to python functions
```
If you call the function <code>greeting</code> without passing argument, it will throw  exception like this:
```markdown
TypeError: greeting() missing 1 required positional argument: 'a'
```
There are different types of arguments available in python functions.

If you pass other than string argument to <code>greeting</code>, It will throw exception to overcome this we need to mdify function defination like this:
```python
def greeting(a):
    """greeting requires 1 argument to greet you"""
    return f'{a} Welcome to python functions'
```
Now you can call the function by passing any data type argument.
```python
greeting(b'Bob')
```
That will give us the output:
```markdown
"b'Bob' Welcome to python functions"
```

Example 3:

Lets take one more function called <code>add</code> and pass two arguments to it and the <code>add</code> will return sum of two arguments as shown below:

```python
def add(a,b):
    """Add two variables and return sum of it"""
    return a+b
```
case-1: Lets call the function by passing two numbers.

```python
print(add(2,5))
```
This will return us 7 as an output

Try to pass two floating point numbers.

```python
print(add(3.14,1.6))
```
The above function call will return 4.74

Now try to pass one float and int values to the function.

```python
print(add(5.3+7))
```
That will return float value 12.3 since we know <code>float+int = float</code> in python.


case-2: Pass two string values as an arguments.

```python
print(add("Hello ","Python"))
```
That will give us the output:

```markdown
Hello Python
```
Another way of doing this is passing two variables

```python
one = "Hello "
two = "Python"
print(add(one, two))
```
That too will return same output.

One more example:

```python
one = "Hello "
print(add(one,"Python"))
```
It gives same output

Case 3: Passing bools to the <code>add</code>

```python
print(add(True,False))
```
It will print 1

```python
print(add(True,True))
```
It will print 2

Now you try the function <code>print(add(False, False))</code>

Case 4: Passing bytes to the <code>add</code>

```python
p = b'Python '
q = b'Functions'
print(add(p,q))
```
It gives output

```markdown
b'Python Functions'
```
Case 5: Passing <code>None</code> to the <code>add</code>

```python
print(add(None, None))
```
It will give us exception.

```markdown
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "<stdin>", line 2, in add
TypeError: unsupported operand type(s) for +: 'NoneType' and 'NoneType'
```

Case 6: Passing different data types as a arguments to <code>add</code>

Number and String:

```python
print(add('Hello ',6))
```
It gives us exception like this:

```markdown
TypeError: can only concatenate str (not "int") to str
```

String and bool:

```python
print(add('Hello',True))
```

It will also gives us the exception like this:

```markdown
TypeError: can only concatenate str (not "bool") to str
```

str and byte

```python
print(add('Hello',b' world'))
```
That would gives us the exception like this:

```markdown
TypeError: can only concatenate str (not "bytes") to str
```






[Home](index.md)
