## Functions
<p id='top'>

</p>
Functions are first class objects in python. Function is a piece of code or set of instructions to carry out specific task.

- Functions may take single or multipule inputs to carry out the the task and sometimes they may not take input.
- After carried out specific task, functions may return single or multipule values or may not return any values.

<p id='types'></p>
There are three types of functions available in python:

- <a href='#bfs'>Built-in Functions</a><br>
- <a href='#udfs'>User Defined Functions(UDFs)</a><br>
- <a href='#anonymus'>Anonymus Functions</a>

<h3 id='bfs'>Built-in Functions</h3><br>
Built-in functions comes up with python. There are different built-in functions are avialble.
You can find about Built-in functions [here](https://docs.python.org/3/library/functions.html)

<a href='#top'>Go to Top</a>    <a href="index.md" class='right'>Home</a>
<hr>


<h3 id='udfs'> User Defined Functions(UDF)</h3>

- The keyword <code>def</code> introduces a function definition.
- It must be followed by the function name and the parenthesized list of formal parameters.
- The statements that form the body of the function start at the next line, and must be indented.
- The first statement of the function body can optionally be a string literal; this string literal is the function’s documentation string, or docstring.
- End your function with a return statement if the function should output something. Without the return statement, your function will return an object None.

<a href='#pa'>Parameters vs Arguments</a><br>
<a href='#positional'>Positional arguments</a><br>
<a href='#keyword'>Keyword arguments</a><br>
<a href='#default'>Default arguments or Optional arguments</a><br>
<a href='#args'>Different types of arguments</a><br>
<a href='#pop'>Position-only Parameters</a><br>
<a href='#koa'>Keyword-only Parameters</a><br>
<a href='#sp'>Special Parameters</a><br>

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

If you pass other than string argument to <code>greeting</code>, It will throw exception.To overcome this we need to modify function definition like this:
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

<strong id='pa'>Parameters vs Arguments</strong>

- Parameters are the names used when defining a function or a method, and into which arguments will be mapped.
- In other words, arguments are the things which are supplied to any function or method call, while the function or method code refers to the arguments by their parameter names.

<p id='args'>
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
Another way of passing positional arguments is like this:
```python
posfunc(*(5,6,7))
```
That will return the output:
```markdown
5   6   7
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
You can change the position of arguments if you want to call arguments by keyword.

```python
keyfunc(b=2,a=1,c=3)
```
Above function call will result the output.

```markdown
a=1
b=2
c=3
```
Another way of calling function with keyword arguments is:

```python
keyfunc(**{'a':7,'b':8,'c':9})
```
That will return the output:

```markdown
a=7     b=8     c=9
```
<h3 id='pop'>Position-only Parameters</h3>
- If positional-only, the parameters’ order matters, and the parameters cannot be passed by keyword.
- Positional-only parameters are placed before a / (forward-slash).
- The / is used to logically separate the positional-only parameters from the rest of the parameters.
- If there is no / in the function definition, there are no positional-only parameters.

```python
def pos_only_arg(arg, /):
    """demo on position only arguments"""
    print(arg)
```

<code>pos_only_arg(1)</code> will return 1. But if you try to call the function like this <code>pos_only_arg(arg=1)</code>. It gives you exception.

```markdown
TypeError: pos_only_arg() got some positional-only arguments passed as key
word arguments: 'arg'
```

<h3 id='default'>Default arguments or Optional arguments</h3>

Optional arguments or Default arguments are arguments that may not be passed to the function. Because they contains default value.

Default parameter values are evaluated from left to right when the function definition is executed.

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
<h3 id='koa'> Keyword-Only Arguments</h3>

To mark parameters as keyword-only, indicating the parameters must be passed by keyword argument, place
an * in the arguments list just before the first keyword-only parameter.

```python
def kwd_only_arg(*, arg):
    """Demo on Keyword-only arguments"""
    print(arg)
```
If you call the above function like this <code>kwd_only_arg(3)</code>. It will throw you exception.

```markdown
TypeError: kwd_only_arg() takes 0 positional arguments but 1 was given
```

<code>kwd_only_arg(arg=3)</code> will print 3.

<h3 id='sp'>Special parameters</h3>

- By default, arguments may be passed to a Python function either by position or explicitly by keyword.
- For readability and performance, it makes sense to restrict the way arguments can be passed so that a
developer need only look at the function definition to determine if items are passed by position, by
position or keyword, or by keyword.

Syntax:

<pre>
def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):
      -----------    ----------     ----------
            |            |              |
            |    Positional or keyword  |
            |                           - Keyword only
            -- Positional only
</pre>

- where / and * are optional
- If used, these symbols indicate the kind of parameter by how the arguments may be passed to the function: positional-only, positional-or-keyword, and keyword-only.
- Keyword parameters are also referred to as named parameters.


In some scenarios arguments size varies for the same function in different scenarios.
You could pass as many arguments as you want to function with the help of <code>*</code>.

Example:

```python
def demo(*arg):
    """Dealing with multipule arguments"""
    return arg
```
You could pass as many arguments you can. Above function return all the passed arguments in the form of tuples.

```python
demo(1,2,'a',True,13.6)
```
Above function call return us this output:

```markdown
(1,2,'a',True,13.6)
```
But if you try to call the function with keyword arguments. You will get exception.
```python
demo(a=1,b=2,c=3)
```
The above function call gives you exception.
```markdown
TypeError: demo() got an unexpected keyword argument 'a'
```

If you want to call the function with keyword arguments . You could do by mentioning <code>**</code>before to the parameter.

```python
def demofunc(**kwargs):
    """Demo on variable names and their values"""
    return kwargs
```
You have to call the function with variable names and their values:

```python
demofunc(a=1,b=2,c=3)
```
Above called function will return parameter name which is passed during the function call and its value as a form of dictionary.

```markdown
{'a': 1, 'b': 2, 'c': 3}
```
But if you try calling the function with positional arguments, you will get exception.

```python
demofunc(1,2,3)
```
Above function call gives you exception.

```markdown
TypeError: demofunc() takes 0 positional arguments but 3 were given
```

If you want to pass both positional and keyword arguments. First you need to pass positional arguments and then keyword arguments.

Function definition would looks like this.

```python
def combo(*arg, **kwargs):
    return arg, kwargs
```
Above function will return in the form of tuple.

```python
combo('a','b','c',a=1,b=2,c=3)
```
Above function call returns

```markdown
(('a','b','c'),{a:1,b:2,c:3})
```

You could decare like this:

```python
def f(par, *arg, **kwarg)
    print(par, *arg, **kwarg)
```

Call the above function like this <code>f(1,2,34,5,a='x',b='y',c='z')</code> will print:

```markdown
1 (2,34,5) {'a':'x','b':'y','c':'z'}
```

But if you try call like this <code>f(par=1,2,34,5,a='x',b='y',c='z')</code> you will get exception like this:

```markdown
SyntaxError: positional argument follows keyword argument
```
To resolve this exception you have to define like this:

```python
def f(*arg,par, **kwarg):
    print(arg, par, kwarg)
```

So you could call the function like this <code>f(1,2,34,par=5,a='x',b='y',c='z')</code>

that will print the result without giving any exception.

<a href='#top'>Go to Top</a>    <a href="index.md" class='right'>Home</a>
<hr>
<h3 id='anonymus'>Anonymus Function</h3>

Anonymus function is a function that could be declared without name, anonymus function  can be declared using <code>lambda</code>.

- Lambda functions can be used wherever function objects are required.
- They are syntactically restricted to a single expression.
- Like nested function definitions, lambda functions can reference variables from the containing scope.

```python
lambda x: x
```
In the above example <code>lambda</code> is keyword, <code>x</code> is a bound variable and the body is <code>x</code>.
Above lambda expression is equivalent to the following function.

```python
def f(x):
    return x
```
You could call the above declared lambda function like this.

```python
(lambda x: x)(2)
```
That will return 2.

One more example:
```python
(lambda x: x+1)(2)
```
That will produce the output 3.

Another way of calling anonymous function is

```python
a = lambda x: x
```
Now variable <code>a</code> will be act as a function.

```python
a(1)
```
Above call will return 1.

Few more examples on the function is

```python
full_name = lambda first, last: f'{first.title()} {last.title()}'
```
You could call this function

```python
full_name('paul','walker')
```

That will give us the output Paul Walker



<a href='#top'>Go to Top</a>    <a href="index.md" class='right'>Home</a>
<hr>
