## Scalar data types

### integer data type

int: unlimited precision signed integer

```markdown
>>> 10
10
>>> type(10)
<class 'int'>
>>> x = 15
>>>x
15
>>> type(x)
<class 'int'>
>>> 0b1010
10
>>> bin(10)
'0b1010'
>>> 0o10
8
>>> oct(8)
'0o10'
>>> 0x145
325
>>> hex(325)
'0x145'
>>> int(3.5)
3
>>> int(-3.5)
-3
>>> int("496")
496
>>> int("1000",3)
81
```
### float data type
- floating points are supported by float type.
- python floats are implemented IEEE-754 double-precision with 53-bits of binary precision.
- This is equivalent to 15-16 significant digits in decimal.

```markdown
>>> 3.125
3.125
>>> 3e8
300000000.0
>>> 1.616e-35
1.616e-35
>>> x = 3.14
>>> x
3.14
>>> type(x)
<class 'float'>
>>> float(7)
7.0
>>> float("1.618")
1.618
>>> float("nan")
nan
>>> float("inf")
inf
>>> float("-inf")
-inf
>>> 3.0+1
4.0
```

### None data type

- python has special null value called "None".
- None is frequently reprsent the absent of value.

```markdown
>>> None
>>> a=None
>>> a is None
True
>>> type(None)
<class 'NoneType'>
```
### bool data type
- Boolean logical values used in control structures
```markdown
>>> True
True
>>> False
False
>>> bool(0)
False
>>> bool(42)
True
>>> bool(-1)
True
>>> bool(0.0)
False
>>> bool(0.207)
True
>>> bool(-1.117)
True
>>> bool([])
False
>>> bool([1,5,9])
True
>>> bool("")
False
>>> bool("spam")
True
>>> bool("False")
True
>>> bool("True")
True
```
- Bool values commonly produces by python relational operators.
- Relational operators are used to comparing the objects.

| operator | meaning                      |
|----------|------------------------------|
|   ==     | value equality / equivalence |
|   !=     | inequality / inequivalence   |
|   <      | less-than                    |
|   >      | greater-than                 |
|   <=     | less-than or equal to        |
|   >=     | greater-than or equal to     |

```markdown
>>> g=20
>>> g == 20
True
>>> g == 13
False
>>> g!= 20
False
>>> g < 30
True
>>> g <= 20
True
>>> g>30
False
>>> g >= 20
True
```
### control flow :

#### conditional statement :
Branch execution based on the value of an expression.
if :

Syntax:
```markdown
   if expression:
       block
```
```markdown
>>> if True:
...     print("It's true!")
...
It's true!
>>> if False:
...     print('It's false!')
...
>>> if bool('eggs'):
...     print('Yes please!')
...
Yes please!
>>> if "eggs":
...     print("Yes please!")
...
Yes please!
```
else clause:
```markdown
>>> h=42
>>> if h>50:
...     print('Greater than 50')
... else:
...     print('50 or smaller')
50 or smaller
>>> if h > 50 :
...     print('Greater than 50')
... else:
...     if h<20:
...         print('Lessthan 20')
...     else:
...         print('Between 20 and 50')
Between 20 and 50
>>> if h>50:
...     print('Greater than 50')
... elif h<20:
...     print('less than 50')
... else:
...     print('Between 20 and 50')
Between 20 and 50
```
while loops:

syntax:
```markdown
while expression:
    <body>
```

```markdown
>>> c = 5
>>> while c!=0:
...     print(c)
...     c-=1
...
5
4
3
2
1
>>> c=5
>>> while c:
...     print(c)
...     c-=1
...
5
4
3
2
1
```

- while loop often used as infinite loops in python.

```markdown
>>> while True:
...     pass
...
press ctrl+c
KeyboardInterrupt
```

break: Many programming languages support a loop ending in predicate test.

python rerquires to use while True and break

break jumps out of the inner-most executing loop the line immediatley after it.

```markdown
>>> while True:
...     response = input()
...     if int(response)%7 == 0 :
...         break
...
12
24
67
34
28
```

#### Int truthiness

```markdown
>>> bool(5) == True
True
>>> bool(4) == True
True
>>> bool(0) == False
False
```

[Go back](index.md)
