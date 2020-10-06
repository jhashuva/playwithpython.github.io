## List/Set/Dict Comprehensions

Before you know about comprehensions. If you want to add a series of elements to list/set/dict we will use appropriate method. For instance we want to add element number from 1 to 5 to a list we could with the append() function like this:

```markdown
>>> l1 = list() #empty list
>>> l1.append(1)
>>> l1.append(2)
>>> l1.append(3)
>>> l1.append(4)
>>> l1.append(5)
>>> print(l1)
[1,2,3,4,5]
```

- We can automate the same thing with for loop.

```markdown
>>> l2 = [] #empty list
>>> for i in range(1,6):
...     l2.append(i)
...
>>> print(l2)
[1,2,3,4,5]
```

- Another way of creating list using range()

```markdown
>>> l3 = list(range(1,6))
>>> l3
[1,2,3,4,5]
```

- All the mentioned techniques above are correct and produce correct result.

- Pythonic way to build a list is by using comprehensions.

- Simplest list comprehension is like this.

syntax:

```markdown
[expression for item in iterable]
```

```markdown
>>> l4 = [i for i in range(1,6)]
>>> l4
[1,2,3,4,5]
```

- same way in the sets

```markdown
>>> s1 = {i for i in range(1,6)}
>>> s1
{1,2,3,4,5}
```

- In dictionary we have to specify key,value pairs.

```markdown
>>> d1={key:key*key for key in range(1,6)}
>>> d1
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

- Comprehensions can include a conditional expression looking something like this

syntax:
```markdown
expression for item in iterable if condition
```
- For list it would looks like this

```markdown
>>> odd_list = [number for number in range(1,6) if number%2!=0]
>>> odd_list
[1,3,5]
```

- In sets

```markdown
>>> odd_set = {number for number in range(1,6) if number%2!=0}
>>> odd_set
{1,3,5}
```
- In dictionary

```markdown
>>> d2 = {number:number*number for number in range(1,5) if number%2!=0}
>>> d2
{1:1, 3:9}
```
```markdown
>>> rows = range(1,4)
>>> cols = range(1,3)
>>> for row in rows:
...     for col in cols:
...         print(row, col)
...
1 1
1 2
2 1
2 2
3 1
3 2
```
- Lets use a comprehension and assign it to the variable cells, making it a list of (row, col) tuples:

```markdown
>>> rows = range(1,4)
>>> cols = range(1,3)
>>> cells = [(row, col) for row in rows for col in cols]
>>> for cell in cells:
...     print(cell)
...
(1, 1)
(1, 2)
(2, 1)
(2, 2)
(3, 1)
(3, 2)
```
[Home](index.md)
