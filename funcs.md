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

```python
def greeting(a):
    """Hi this is print statement. It will print the input given to this function"""
    return a

greeting(a="Hello World")
```
- Above example will return the string Hello World

- You can store the function call in another variable like this

```python
b = greeting(a="Hello Python")
print(b)
```
output:
```markdown
Hello Python
```
If you want to know what really function does. You can check using <code>function.__doc__</code>
For example you want to know what <code>print</code> does.

```python
print(greeting.__doc__)
```
The above statement will print the following:

```markdown
'Hi this is print statement. It will print the input given to this function'
```
Example 2:

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
It gives exception like this:






[Home](index.md)
