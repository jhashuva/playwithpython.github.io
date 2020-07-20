## Collections
<div id='index'>
<a href='#strings'>Str</a><br>
<a href='#bytes'>Bytes</a><br>
<a href='#lists'> Lists</a><br>
<a href='#tuples'> Tuples</a><br>
<a href='#sets'> Sets</a><br>
<a href='#dicts'>Dictionaries</a>
</div>


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
Substitute by Using replace()

You use replace() for simple substring substitution.Give it the old substring, the new one,and how many instances of the old substring to replace.
It returns the changed string but does notmodify the original string.If you omit this final count argument, it replaces all instances.

Syntax:
```markdown
string.replace(old_substring, new_substring, count(optional))
```
```markdown
>>> setup = "a duck goes into a bar..."
>>> setup.replace('duck', 'marmoset')
>>> setup.replace('duck', 'marmoset')
'a marmoset goes into a bar...'
>>> setup
'a duck goes into a bar...'
```

Strip with strip()
The strip() functions shown here assume that you want to get rid ofwhitespace characters (' ', '\t', '\n')if you don’t give them an argument.strip() str.
strip() strips both ends, lstrip() only from the left, and rstrip() only from the right.

Syntax :
```markdown
string.strip()
```
```markdown
>>> world = "    earth   "
>>> world.strip()
'earth'
>>> world.strip(' ')
'earth'
>>> world.lstrip()
'earth  '
>>> world.rstrip()
'   earth'
```
If the character were not there, nothing happens:

```markdown
>>> world.strip('!')
'   earth   '
```

Besides no argument (meaning whitespace characters) or a single character, you can also tell strip() to remove any character in a multicharacter string:

```markdown
>>> blurt = "What the...!!?"
>>> blurt.strip('.?!')
'What the'
```
Search and Select

```markdown
>>> poem = '''All that doth flow we cannot liquid name
... Or else would fire and water be the same;
... But that is liquid which is moist and wet
... Fire that property can never get
.... Then 'tis not cold that doth the fire put out
... But 'tis the wet that makes it die, no doubt.'''
>>> poem[:13]
'All that doth'
>>> len(poem)
254
>>> poem.startswith('All')
True
>>> poem.endswith('That\'s all, folks!')
False
```
Let’s find the offset of the first occurrenceof the word the in the poem:
```markdown
>>> word='the'
>>> poem.find(word)
73
>>> poem.index(word)
73
```
And the offset of the last the:

```markdown
>>> word = 'the'
>>> poem.rfind(word)
218
>>> poem.rindex(word)
218
```

How many times does the three-letter sequence 'the' occur?

```markdown
>>> poem.count(word)
3
```
Are all of the characters in the poem either letters or numbers?

```markdown
>>> poem.isalnum()
False
```

Cases:

```markdown
>>> setup = 'a duck goes into a bar...'
```

```markdown
>>> setup.strip('.')
'a duck goes into a bar'
```
Capitalize the first word:

```markdown
>>> setup.capitalize()
'A duck goes into a bar...'
```

Capitalize all the words:

```markdown
>>> setup.title()
'A Duck Goes Into A Bar...'
```

Convert all characters to uppercase:

```markdown
>>> setup.upper()
'A DUCK GOES INTO A BAR...'
```

Convert all characters to lowercase:

```markdown
>>> setup.lower()
'a duck goes into a bar...'
```

Swap uppercase and lowercase:

```markdown
>>> setup.swapcase()
'A DUCK GOES INTO A BAR...'
>>> setup
'a duck goes into a bar...'
```

Formatting :

<table border="1" align='left'>
<tr><td>%s</td><td>string</td></tr>
<tr><td>%d</td><td>decimal integer</td></tr>
<tr><td>%x</td><td>hex integer</td></tr>
<tr><td>%o</td><td>octal integer</td></tr>
<tr><td>%f</td><td>decimal float</td></tr>
<tr><td>%e</td><td>exponential float</td></tr>
<tr><td>%g</td><td>decimal or exponential float</td></tr>
</table>
<br><br>

You can use a %s for any data type, and Python will format it as a string with no extra spaces.

```markdown
>>> '%s' % 42
'42'
>>> '%d' % 42
'42'
>>> '%x' % 42
'2a'
>>> '%o' % 42
'52'
```

An integer and a literal %:

```markdown
>>> '%d%%' % 100
'100%'
```

Let's try some string and integer interpolation:

```markdown
>>> actor = 'Richard Gere'
>>> cat = 'Chester'
>>> weight = 28
>>> "My friend's favorite actor is %s" % actor
"My friend's favorite actor is Richard Gere"
>>> "Our cat %s weighs %d pounds" % (cat, weight)
'Our cat Chester weighs 28 pounds'
```
some more examples

```markdown
>>> thing = 'woodchuck'
>>> '%s' % thing
'woodchuck'
>>> '%12s' % thing
'   woodchuck'
>>> '%+12s' % thing
'   woodchuck'
>>> '%-12s' % thing
'woodchuck   '
>>> '%.3s' % thing
'woo'
>>> '%12.3s' % thing
'         woo'
>>> '%-12.3s' % thing
'woo         '
```

one more with feeling

```markdown
>>> thing = 98.6
>>> '%f' % thing
'98.600000'
>>> '%12f' % thing
'   98.600000'
>>> '%6f' % thing
'98.600000'
>>> '%+12f' % thing
'  +98.600000'
>>> '%-12f' % thing
'98.600000   '
>>> '%.3f' % thing
'98.600'
>>> '%12.3f' % thing
'      98.600'
>>> '%-12.3f' % thing
'98.600      '
```
New style:{} and format()

“New style” formatting has the form format_string.format(data).

```markdown
>>> thing = 'woodchuck'
>>> '{}'.format(thing)
'woodchuck'
```
The arguments to the format() function need to be in the order as the {} placeholders in the format string:
```markdown
>>> thing = 'woodchuck'
>>> place = 'lake'
>>> 'The {} is in the {}.'.format(thing, place)
'The woodchuck is in the lake.'
```

With new-style formatting, you can also specify the arguments by position like this:

```markdown
>>> 'The {1} is in the {0}.'.format(place, thing)
'The woodchuck is in the lake.'
```

The value 0 referred to the first argument, place, and 1 referred to thing.

The arguments to format() can also be named arguments

```markdown
>>> 'The {thing} is in the {place}'.format(thing='duck', place='bathtub')
'The duck is in the bathtub'
```
or a dictionary:
```markdown
>>> d = {'thing': 'duck', 'place': 'bathtub'}
>>> 'The {0[thing]} is in the {0[place]}.'.format(d)
'The duck is in the bathtub.'
```

More Examples:
```markdown
>>> thing = 'wraith'
>>> place = 'window'
>>> 'The {} is at the {}'.format(thing, place)
'The wraith is at the window'
>>> 'The {:10s} is at the {:10s}'.format(thing.upper(), place)
'The WRAITH     is at the window    '
>>> 'The {:<10s} is at the {:<10s}'.format(thing, place)
'The wraith     is at the window    '
>>> 'The {:^10s} is at the {:^10s}'.format(thing, place)
'The   wraith   is at the   window  '
>>> 'The {:>10s} is at the {:>10s}'.format(thing, place)
'The     wraith is at the     window'
>>> 'The {:!^10s} is at the {:!^10s}'.format(thing, place)
'The !!wraith!! is at the !!window!!'
```
Newest Style: f-strings

- f-strings appeared in Python 3.6, and are now the recommended way of formatting strings.
To make an f-string:
- Type the letter f or F directly before the initial quote.
- Include variable names or expressions within curly brackets ({}) to get their values into the string.

```markdown
>>> thing = 'wereduck'
>>> place = 'werepond'
>>> f'The {thing} is in the {place}'
'The wereduck is in the werepond'
>>> f'The {thing.capitalize()} is in the {place.rjust(20)}'
'The Wereduck is in the             werepond'
>>> f'The {thing:>20} is in the {place:.^20}'
'The             wereduck is in the ......werepond......'
```
- Starting in Python 3.8, f-strings gain a new shortcut that’s helpful when you want to print variable names as well as their values.

```markdown
>>> f'{thing =}, {place =}'
"thing ='wereduck', place ='werepond'"
>>> f'{thing[-4:] =}, {place.title() =}'
"thing[-4:] ='duck', place.title() ='Werepond'"
>>> f'{thing = :>4.4}'
'thing = were'
```
- for more details: [python documentation](https://docs.python.org/3/library/stdtypes.html#string-methods)
- These examples are borrowed from the "Introducing Python" 2nd Edition by Bill Lubanovic, O'Reilly media inc.,2019
- Think Python, Second Edition, Allen B. Downey, 2016, O'Reilly
<br>
<br>
<a href='#index'>Got to top</a> &nbsp;&nbsp;&nbsp;[Home](index.md)
<h3 id='bytes'> Bytes</h3>
- Data type for sequence of bytes
- Raw binary data
- Fixed width single byte encoding

```markdown
>>> b'byte data'
b'byte data'
>>> d= b'some bytes'
>>> type(d)
<class 'bytes'>
>>> d.split()
[b'some', b'bytes']
```
Converting between strings and bytes:
![](./collections1.JPG)

```markdown
>>> a = b'byte data'
>>> a.decode()
'byte data'
>>> b = 'hello python'
>>> b.encode()
b'hello python'
```
<a href='#index'>Got to top</a> &nbsp;&nbsp;&nbsp;[Home](index.md)

<h3 id='lists'> Lists</h3>
- sequence of objects
-  Lists are Mutable
- Lists are declared with [] or list()
- Items are seperated with comma(,)

Create empty list

```markdown
>>> myfirst_list = []   # one way of creating empty list
>>> type(myfirst_list)
<class 'list'>
>>> mysecond_list = list() # another way of creating empty list
>>> type(mysecond_list)
<class 'list'>
```
python list() converts string into list

```markdown
>>> list('python')
['p', 'y', 't', 'h', 'o', 'n']
```

Create a list from string split()

```markdown
>>> python_day='12/12/2019'
>>> python_day.split('/')
['12', '12', '2019']
```
list.reverse() : To reverse the elements in the list

```markdown
>>> lang=['c','c++','java','python']
>>> lang.reverse()
>>> lang
['python', 'java', 'c++', 'c']
```

Add an Item to the End with append()

```markdown
>>> lang=['c','c++','java','python']
>>> lang.append('R')
>>> lang
['c', 'c++', 'java', 'python', 'R']
```

Add an Item by Offset with insert()

syntax:

```markdown
insert(index, word)
```
Examples:

```markdown
>>> lang=['c', 'c++', 'java', 'python', 'R']
>>> lang.insert(2,'scala')
>>> lang
['c', 'c++', 'scala', 'java', 'python', 'R']
```

Duplicate All Items with *

syntax:

```markdown
['string']*value
```

Examples:

```markdown
>>> ['python']*3
['python', 'python', 'python']
>>> ['python','java']*3
['python', 'java', 'python', 'java', 'python', 'java']
```
Combine Lists by Using extend() or +

```markdown
>>> lang
['c', 'c++', 'scala', 'java', 'python', 'R']
>>> markups=['html','xml']
>>> lang.extend(markups)
>>> lang
['c', 'c++', 'scala', 'java', 'python', 'R', 'html', 'xml']
>>> server_scripting=['PHP','ASP','JSP']
>>> lang=lang+server_scripting
>>> lang
['c',
 'c++',
 'scala',
 'java',
 'python',
 'R',
 'html',
 'xml',
 'PHP',
 'ASP',
 'JSP']
>>> lang+=server_scripting
>>> lang
['c',
 'c++',
 'scala',
 'java',
 'python',
 'R',
 'html',
 'xml',
 'PHP',
 'ASP',
 'JSP',
 'PHP',
 'ASP',
 'JSP']
 >>> client_scripting=['javascript','actionscript']
 >>> lang.append(client_scripting)
 >>> lang
 ['c',
 'c++',
 'scala',
 'java',
 'python',
 'R',
 'html',
 'xml',
 'PHP',
 'ASP',
 'JSP',
 'PHP',
 'ASP',
 'JSP',
 ['javascript', 'actionscript']]
```
Change an Item by [offset]

```markdown
>>> lang
['c',
 'c++',
 'scala',
 'java',
 'python',
 'R',
 'html',
 'xml',
 'PHP',
 'ASP',
 'JSP',
 'PHP',
 'ASP',
 'JSP',
 ['javascript', 'actionscript']]
 >>> lang[1]='c#'
 >>> lang
 ['c',
 'c#',
 'scala',
 'java',
 'python',
 'R',
 'html',
 'xml',
 'PHP',
 'ASP',
 'JSP',
 'PHP',
 'ASP',
 'JSP',
 ['javascript', 'actionscript']]
 ```

 Change an item with slice

```markdown
>>> numbers=[1,2,3,4]
>>> numbers[1:3]=[8,9]
>>> numbers
[1, 8, 9, 4]
```
Delete an Item by Offset with del

syntax:

```markdown
 del list[offset]
```

Examples:

```markdown
>>> languages=['C','C#','Java','Python']
>>> del languages[-1]
>>> languages
['C', 'C#', 'Java']
>>> del languages[0:2]
>>> languages
['Java']
```
Delete an Item by Value with remove()

syntax:
```markdown
list.remove('element')
```
Examples:

```markdown
>>> languages=['C','C#','Java','Python']
>>> languages.remove('C#')
```

Get an Item Offset and Delete It with pop()

syntax:
```markdown
list.pop(offset)
```
```markdown
>>> languages=['C','C#','Java','Python']
>>> languages.pop()
'Python'
>>> languages.pop(1)
'C#'
>>> languages
['C', 'Java']
```
Delete All Items with clear()
syntax:
```markdown
list.clear()
```
```markdown
>>> languages=['C','C#','Java','Python']
>>> languages.clear()
>>> languages
[]
```

<a href='#index'>Got to top</a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Home](index.md)

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

