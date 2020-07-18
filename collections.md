## Collections

<a href='#strings'>Str</a><br>
<a href='#lists'> Lists</a><br>
<a href='#tuples'> Tuples</a><br>
<a href='#sets'> Sets</a><br>
<a href='#dicts'>Dictionaries</a>



<h3 id='strings'>Str</h3>
- Str is the short form of string
- Str data type is immutable i.e once you declare it, you cannot able to modify it.

Syntax:
```markdown
>>>"this is string"
'this is string'
>>>'this is also a string'
'this is also a string'
>>>"This is not way of declering the string'
 File "<stdin>", line 1
    "This is not way of declering the string'
                                            ^
SyntaxError: EOL while scanning string literal
>>>'This is also not way of declering the string"
 File "<stdin>", line 1
    'This is also not way of declering the string"
                                                 ^
SyntaxError: EOL while scanning string literal
```
You can check the data type of the string
```markdown
>>>a = "paly with python"
>>>type(a)
<class 'str'>
```
String with new lines:

- Multi line strings: spread the literal across multipule lines.
```markdown
>>>""" This is
... multi line string
... this is end"""
'This is\nmulti line string\nthis is end'
>>> poem = """Just like moons and like suns,
... With the certainity of tides,
... Just like hopes springing high,
... Still I'll raise."""
>>> poem
'Just like moons and like suns,\nWith the certainity of tides,\nJust like hopes springing high,\nStill I'll raise.'
>>> print(poem)
Just like moons and like suns,
With the certainity of tides,
Just like hopes springing high,
Still I'll raise.
```
- Escape sequences : Embed escape sequences in a single-line literal

Python lets you escape the meaning of some characters with in strings to achieve effects that would otherwise be difficult to express.By preceding a character with a backslash (\),
you give it a special meaning.The most common escape sequence is \n,which means to begin a new line.
```markdown
>>> 'This is\nmulti line string\nthis is end'
'This is\nmulti line string\nthis is end'
>>> a = 'You are not your parents\nYou are not your class\nYou are not the clothes you wear\nYou are not the size of your friend circle\nYour sum of your words. choices and actions.'
>>> a
'You are not your parents\nYou are not your class\nYou are not the clothes you wear\nYou are not the size of your friend circle\nYour sum of your words. choices and actions.'
>>> print(a)
You are not your parents
You are not your class
You are not the clothes you wear
You are not the size of your friend circle
Your sum of your words. choices and actions.
```
More escape sequences:
```markdown
>>> palindrome = 'A man,\nA plan,\nA canal:\nPanama.'
>>> print(palindrome)
A man,
A plan,
A canal:
Panama.
>>> print('\tabc')
    abc
>>> print('a\tbc')
a   bc
>>> print('ab\tc')
ab    c
>>> testimony = "\"I did nothing!\" he said. \"Or that other thing.\""
>>> print(testimony)
"I did nothing!" he said. "Or that other thing."
>>> fact = "The world's largest rubber duck was 54'2\" by 65'7\" by 105'"
>>> print(fact)
The world's largest rubber duck was 54'2" by 65'7" by 105'
>>> speech = 'The backslash (\\) can be printed using like this.'
>>> print(speech)
The backslash (\) can be printed using like this.
```
Combining by using +

 we can combine literal strings or string variables using the + operator.

```markdown
>>> "good "+"morning"
'good morning'
>>> name = "Joe"
>>> branch = " computer science and engineering"
>>> print(name+branch)
Joe computer science and engineering
>>> a = 'Duck.'
>>> b = a
>>> c = 'Grey Duck!'
>>> a+b+c
'Duck.Duck.Grey Duck!'
```
Duplicate with *

We use the * operator to duplicate a string.

```markdown
>>> "hi"*3
'hihihi'
>>> "hello "*3
'hello hello hello'
>>> a = 'Na ' * 4 + '\n'
>>> b = 'Hey ' * 3 + '\n'
>>> end = 'Goodbye.'
>>> print(start + start + middle + end)
Na Na Na Na
Na Na Na Na
Hey Hey Hey
Goodbye.
```
Notice that the * has higher precedence than +, so the string is duplicated before the line feed is tacked on.

Get characters with []

- To get a single character from a string, specify its offset inside square brackets after the string’s name.
- The first (leftmost) offset is 0, the next is 1, and so on.

```markdown
>>> letters = 'abcdefghijklmnopqrstuvwxyz'
>>> letters[0]
a
>>> letters[25]
z
```

Get a substring with a slice

syntax:
```markdown
[start_offset:end_offset:step(optional)]
```
```markdown
>>> letters[1:11]
'bcdefghijk'
>>> letters[1:20:2]
'bdfhjlnprt'
>>> letters[::5]
'afkpuz'
>>> letters[21]
'v'
```
Get Length with len()

The len() function counts characters in a string:

Syntax:

```markdown
len(string)
```

```markdown
>>> letters = 'abcdefghijklmnopqrstuvwxyz'
>>> len(letters)
26
>>> empty = ""
>>> len(empty)
0
```
spilt with split()

You can use the built-in string split() function to break a string into a list of smaller strings based on some separator.

syntax:
```markdown
string.split('seperator')
```
```markdown
>>> tasks = 'get gloves,get mask,give cat vitamins,call ambulance'
>>> tasks.split(',')
['get gloves', 'get mask', 'give cat vitamins', 'call ambulance']
>>> tasks.split()
['get', 'gloves,get', 'mask,give', 'cat', 'vitamins,call', 'ambulance']
```
combine by using join()

syntax:
```markdown
seperator.join(list)
```

```markdown
>>> crypto_list = ['Yeti', 'Bigfoot', 'Loch Ness Monster']
>>> crypto_string = ', '.join(crypto_list)
>>> print(crypto_string)
Yeti, Bigfoot, Loch Ness Monster
```

<h3 id='lists'> Lists</h3>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<h3 id='tuples'> Tuples</h3>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<h3 id='sets'> Sets</h3>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<h3 id='dicts'> Dictionaries</h3>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

