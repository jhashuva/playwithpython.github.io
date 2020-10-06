## Shallow copy and Deep copy

Before we see about shallow copy and deep copy. We see how to assign any collection data type variable to another.

```python
>>> a = [1,2,3]
>>> id(a)
1958952968712
>>> b=a
>>> b
[1,2,3]
>>> id(b)
1958952968712
```
- If you try to add an element to the b. It reflects in a also

```python
>>> b
[1,2,3]
>>> a
[1,2,3]
>>> b.append(4)
>>> b
[1,2,3,4]
>>> a
[1,2,3,4]
```

Same way in sets

```python
>>> s1 = {1,2,3,4}
>>> id(s1)
2110019791776
>>> s2 = s1
>>> s2
{1,2,3,4}
>>> id(s2)
2110019791776
>>> s2.add(5)
>>> s2
{1,2,3,4,5}
>>> s1
{1,2,3,4,5}
```
- Dictionary also have the same issue

```python
>>> d1 = {'a':1,'b':2,'c':3}
>>> id(d1)
2110019840000
>>> d2 = d1
>>> d2
{'a':1,'b':2,'c':3}
>>> d2.update(d=4)
>>> d2
{'a':1,'b':2,'c':3, 'd':4}
>>> d1
{'a':1,'b':2,'c':3, 'd':4}
```
### Shallow copy

A shallow copy constructs a new compound object and then (to the extent possible) inserts references into it to the objects found in the original.


- with the copy() function we do shallow copying.

```python
>>> list1 = [['a','b'],['c','d']]
>>> id(list1)
2110019822592
>>> list2 = list1.copy()
>>> list2
[['a','b'],['c','d']]
>>> id(list2)
2110019839936
>>> list2[0][1] = 'x'
>>> list2
[['a','x'],['c','d']]
>>> list1
[['a','x'],['c','d']]
```
Same happens to dictionary

```python
>>> d1 = {1:['a','b'],2:['c','d']}
>>> id(d1)
2110017714496
>>> d2 = d1.copy()
>>> d2
{1:['a','b'],2:['c','d']}
>>> id(d2)
2110017714432
>>> d2[1][1]='x'
>>> d2
{1:['a','x'],2:['c','d']}
>>> d1
{1:['a','x'],2:['c','d']}
```

With the help of deepcopy(), we remedy this situation.


### Deep copy

A deep copy constructs a new compound object and then, recursively, inserts copies into it of the objects found in the original.

For this purpose we need to import module called copy

```python
>>> import copy
>>> list1 = [['a','b'],['c','d']]
>>> list2 = copy.deepcopy(list1)
>>> list2[0][1] = 'x'
>>> list2
[['a','x'],['c','d']]
>>> list1
[['a','b'],['c','d']]
```
Same way in dictionaries

```python
>>> import copy
>>> d1 = {1:['a','b'],2:['c','d']}
>>> d2 = copy.deepcopy(d1)
>>> d2
{1:['a','b'],2:['c','d']}
>>> d2[1][1]='x'
>>> d2
{1:['a','x'],2:['c','d']}
>>> d1
{1:['a','b'],2:['c','d']}
```

[Home](index.md)
