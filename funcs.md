## Functions
<p id='top'>
<a href='#types'>Types of functions</a><br>
<a href='#udfs'>User Defined Functions(UDFs)</a><br>
<a href='#pa'>Parameters vs Arguments</a><br>
<a href='#args'>Different types of arguments</a>
</p>
Functions are first class objects in python. Function is a piece of code or set of instructions to carry out specific task.

- Functions may take single or multipule inputs to carry out the the task and sometimes they may not take input.
- After carried out specific task, functions may return single or multipule values or may not return any values.

<p id='types'></p>
There are three types of functions available in python:

- Built-in functions
- User Defined Functions(UDFs)
- Anonymus functions

You can find about Built-in functions [here](https://docs.python.org/3/library/functions.html)

<a href='#top'>Go to Top</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Go Home](index.md)


<h3 id='udfs'> User Defined Functions(UDF)</h3>

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

Creating a function with parameters(s):

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

If you pass other than string argument to <code>greeting</code>, It will throw exception.To overcome this we need to mdify function definition like this:
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

Lets take one more function called <code>add</code> with two parameters

```python
def add(a,b):
    """Add two variables and return sum of it"""
    return a+b
```
You need to pass the two arguments to call the <code>add</code>.
```python
add(10,120)
```
It will return 130

<a href='#top'>Go to Top</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [GO Home](index.md)

<strong id='pa'>Parameters vs Arguments</strong>

- Parameters are the names used when defining a function or a method, and into which arguments will be mapped.
- In other words, arguments are the things which are supplied to any function or method call, while the function or method code refers to the arguments by their parameter names.


<a href='#top'>Go to Top</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Go Home](index.md)

<p id='args'>
<a href='#positional'>Positional arguments</a><br>
<a href='#keyword'>
Keyword arguments</a><br>
<a href='#default'>
Default arguments or Optional arguments
</a>
</p>
<h3 id='positional'>Positional arguments</h3>
Positional arguments are arguments that can be called by their position in the function definition.

Example 3:
```python
def posfunc(a,b,c):
    """Demo about positional arguments"""
    return f'a={a}\nb={b}\nc={c}'
```
You required to pass the three arguments to the function <code>posfunc</code> in same order.
```python
posfunc(1, 2, 3)
```
<code>posfunc</code> will return the output:
```markdown
a=1
b=2
c=3
```
<h3 id='keyword'>Keyword arguments</h3>
Keyword arguments are arguments that must call by their name.

Example 4:
```python
def keyfunc(a,b,c):
    """Demo about keyword arguments"""
    return f'a={a}\nb={b}\nc={c}'
```
You need to call the function <code>keyfunc</code> arguments by their name:
```python
keyfunc(a=1,b=2,c=3)
```
Above function will return
```markdown
a=1
b=2
c=3
```
You can change the position of arguments if you want to call arguments by their name.
```python
keyfunc(b=2,a=1,c=3)
```
Above function call will result the output.

```markdown
a=1
b=2
c=3
```
<h3 id='default'>Default arguments or Optional arguments</h3>

Optional arguments or Default arguments are arguments that may not be passed to the function. Because they contains default value.

Example 5:

```python
def defunc(a=1,b=2,c=3):
    """default arguments demonstration"""
    return f'a={a}/t b={b} /t c={c}'
```

You could call this function without passing arguments like this:

```python
defunc()
```
That will return the output like this:
```markdown
a=1     b=2     c=3
```
If you want to overwrite default values in the function you could do that by passing argument as a positional or keyword to the function call

```python
defunc(2) #positional argument
```
The above call will overwrites first argument value, in this case <code>a</code>
```markdown
a=2     b=2     c=3
```
You could also overwrite default value by using keyword argument.

```python
defunc(c=99)
```
The above function call will return us.
```markdown
a=1     b=2     c=99
```
Caution: You should not pass positional and keyword arguments for the same parmeter.

For example if you pass positional argument then try to pass keyword argument to the same parameter it will throw us exception.

```python
defunc(5,a=555)
```
This call will throw an exception like this:
```markdown
TypeError: defunc() got multiple values for argument 'a'
```
**Note:** You need to pass positional arguments followed by keyword arguments.

```python
defunc(2,b=3)
```
That will return us the output:
```markdown
a=2     b=3     c=3
```
But if you try to pass other way you will get exception:
```python
defunc(a=5,777)
```
The output would be like this:
```markdown
SyntaxError: positional argument follows keyword argument
```

<a href='#top'>Go to Top</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Home](index.md)
