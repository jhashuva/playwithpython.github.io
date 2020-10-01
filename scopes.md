<p id='main'>
    <h2>Variables Scope</h2>
</p>

<h3> Local Scope</h3>
If you declare a variable within a function. You could access the variable value within a function.

```python
def f():
    x="Hello World"
    print(x)

f()#calling the function
print(x) #outside of the function
```

Above function call <code>f()</code> prints <code>Hello World</code> but <code>print(x)</code> in the global scope return us exception <code>x not defined</code>


<h3> Global scope</h3>

```python
def f():
    print(s)

s = "Welcome to Python" #global scope
f() #function calling
```
If you call the function <code>f()</code>. It will not give exception but prints <code>Welcome to Python</code>.

```python
def f():
    s="Local scope"
    print(s)

s = "Global scope" #global scope
f()
print(s)
```

Output:

```markdown
Local scope
Global scope
```

But if you try to combine both examples which are mentioned above.

```python
def f():
    print(s)
    s = "Local scope"
    print(s)

s = "Global scope"
f()
print(s)
```

You will get <code>UnboundLocalError</code>

```markdown
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "<stdin>", line 2, in f
UnboundLocalError: local variable 's' referenced before assignment
```

As you know python follows LEGB rule, to understand it clearly you need to mention <code>global</code> keyword whenver you want to accesss global varibale in local scope.

```python
def f():
    global s
    print(s)
    s = "Local scope"
    print(s)

s = "Global scope"
f()
print(s)
```
output:

```markdown
Global scope
Local scope
Local scope
```

If you observe the output, it has been replaced golbal varible <code>s</code> value <code>Global scope</code> to <code>Local scope</code>.


```python
def f():
    s = "Enclosed function"
    def g():
        global s
        s = "Local function"
    print('Before calling g:',s)
    g()
    print('After calling g:',s)

f()
print('value of s',s)
```
Output:

```markdown
Before calling g: Enclosed function
After calling g: Enclosed function
Value of s, Local function
```


<code>nonlocal</code> variables are special kind of variables that cannot change from modules scope.

```python
def f():
    s = "enclosing scope"
    def g():
        nonlocal s
        s = "local scope"
    print('before calling g',s)
    g()
    print('after calling g',s)

s = "global scope"
f()
print('main s',s)
```

Output:
```markdown
before calling g enclosing scope
after calling g local scope
main s global scope
```

```python
def f():
    #s = "enclosing scope" comment
    def g():
        nonlocal s
        s = "local scope"
    print('before calling g',s)
    g()
    print('after calling g',s)

s = "global scope"
f()
print('main s',s)
```

Output:

```markdown
SyntaxError: no binding for nonlocal 's' found
```

But if it is global, it will not give any exception

```python
def f():
    #s = "enclosing scope" comment
    def g():
        global s
        s = "local scope"
    print('before calling g',s)
    g()
    print('after calling g',s)

s = "global scope"
f()
print('main s',s)
```

Output:

```markdown
before calling g global scope
after calling g local scope
main s local scope
```
[Home](./index.md)
