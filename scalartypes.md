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

