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



