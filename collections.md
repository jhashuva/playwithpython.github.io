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
Find an Item's Offset by Value with index()

Syntax:
```markdown
list.index('element')
```

```markdown
>>> languages=['C','C#','Java','Python']
>>> languages.index('C')
0
```
Test for Value with in
Syntax:
```markdown
'element' in list
```

```markdown
>>> languages=['C','C#','Java','Python']
>>> 'Python' in languages
True
>>> 'C++' in languages
False
```
Count Occurrences of Value with count()

Syntax:
```markdown
list.count('element')
```

```markdown
>>> languages.count('C')
1
```
How to convert list to string ?

Syntax:
```markdown
'seperator'.join(list)
```

```markdown
>>> languages=['C','C#','Java','Python']
>>> ','.join(languages)
'C,C#,Java,Python'
```
Reorder Items of the list

Using python function:

```markdown
>>> languages=['Python','C#','Java','C']
>>> sorted(languages)
['C', 'C#', 'Java', 'Python']
>>> languages #original order will never changed
['Python','C#','Java','C']
```

Using list method:
```markdown
>>> languages=['Python','C#','Java','C']
>>> languages.sort()
>>> languages
['C', 'C#', 'Java', 'Python']
>>> languages=['Python','C#','Java','C']
>>> languages.sort(reverse=True) # sort reverse order
>>> languages
['Python', 'Java', 'C#', 'C']
```

Get Length with len()

Syntax:

```markdown
len(list)
```
```markdown
>>> len(languages)
4
```
Assign with =

 When you assign one list to more than one variable, changing the list in one place also changes it in the other.

```markdown
 >>> a=[1,2,3,4]
 >>> id(a)
 2109612147720
 >>> b=a
 >>> id(b)
 2109612147720
 >>> a[0]='hello'
 >>> a
 ['hello', 2, 3, 4]
 >>> b
 ['hello', 2, 3, 4]
 >>> b[1]='hi'
 >>> a
 ['hello', 'hi', 3, 4]
```

Compare lists:

```markdown
>>> a = [1,2,3]
>>> b = [7,8,9]
>>> a == b
False
>>> b>a
True
```

Iterate with for and in

```markdown
>>> languages=['C','C#','JAVA','PYTHON']
>>> for i in languages:
...     print(i)
c
c#
Java
Python
```
break ends the for loop and continue steps to next iteration

```markdown
>>> languages=['C','C#','JAVA','PYTHON','HTML','GO']
>>> for i in languages:
...    if i.lower()=='html':
...        print('HTML is not a programming language like others')
...        break
...    else:
...        print(i)
C
C#
JAVA
PYTHON
HTML is not a programming language like others
```
We can use the optional else if the for Completed without a break

```markdown
>>> languages=['C','C#','JAVA','PYTHON','GO']
>>> for language in languages:
...    if language.lower()=='html':
...        print('HTML is not a programming language like others')
...        break
...    else:
...        print(language)
... else:
...    print('There are no non-programming languages')
C
C#
JAVA
PYTHON
GO
There are no non-programming languages
```
If the initial for never ran, control goes to the else also:

```markdown
>>> cheeses=[]
... for cheese in cheeses:
...     print(cheese)
...     break
... else:
...     print('There is no cheese')
There is no cheese
```
cheeses list was empty in this example, for cheese in cheeses never completed a single loop and its break statement was never executed.

```markdown
>>> days=['Monday','Tuesday','Wednesday']
>>> fruits=['banana','orange','peach']
>>> drinks=['coffee','tea','ice tea']
>>> desserts=['double ka meeta','ice cream','jamoon','pudding']
>>> for day, fruit, drink, dessert in zip(days, fruits, drinks, desserts):
...     print(day, ": drink", drink, "- eat",fruit, "- enjoy", dessert)
Monday : drink coffee - eat banana - enjoy double ka meeta
Tuesday : drink tea - eat orange - enjoy ice cream
Wednesday : drink ice tea - eat peach - enjoy jamoon
```
zip() stops when the shortest sequence is done.

List of lists

```markdown
>>> small_birds=['hamming_bird','finch']
>>> extinct_birds=['dodo','passenger pigeon','Norwegian Blue']
>>> carol_birds=[3,'French hens',2,'turtledoves']
>>> all_birds=[small_birds,extinct_birds,carol_birds]
>>> all_birds
[['hamming_bird', 'finch'],
 ['dodo', 'passenger pigeon', 'Norwegian Blue'],
 [3, 'French hens', 2, 'turtledoves']]
 >>> all_birds[0]
 ['hamming_bird', 'finch']
 >>> all_birds[1]
 ['dodo', 'passenger pigeon', 'Norwegian Blue']
 >>> all_birds[1][0]
 'dodo'
```
<a href='#index'>Got to top</a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Home](index.md)


<h3 id='tuples'> Tuples</h3>
- Tuple is non mutable type
- Tuple will be represented with ().

```markdown
>>> empty_tuple = ()
>>> empty_tuple
()
>>> type(empty_tuple)
tuple
```
- To make a tuple with one or more elements, follow each element with a comma. This works for one-element tuples

```markdown
>>> one_color = 'Green',
>>> one_color
('Green',)
>>> one_color=('Green',)
>>> one_color
('Green',)
>>> multi_color='Green','Red','White'
>>> multi_color
('Green', 'Red', 'White')
```

- Tuple let you assign multiple variables at once:

```markdown
>>> a = list(multi_color)
>>> tuple(a)
('Green', 'Red', 'White')
>>> a,b,c = multi_color
>>> a
Green
>>> b
Red
>>> c
White
```

- This is called tuple unpacking
- You can use tuples to exchange values in one statement without using a temporary variables.

```markdown
>>> password = 'confidential'
>>> icecream = 'choclate'
>>> password, icecream = icecream, password
>>> password
choclate
>>> icecream
confidential
>>> a = password,icecream
>>> a
('choclate', 'confidential')
```
- Create tuple with the tuple()

```markdown
>>> numbers=[1,3,5,7]
>>> tuple(numbers)
(1, 3, 5, 7)
```

Combine Tuples by Using +

- This is similar to combining strings

```markdown
>>> ('Groucho',)+('Chico','harpo')
('Groucho', 'Chico', 'harpo')
```
Duplicate items with *

- This is like repeated use of +:

```markdown
>>> ('yada',)*3
('yada','yada','yada')
```
Compare tuples

- This works much like list comparisions

```markdown
>>> a=(7,2)
>>> b=(7,2,9)
>>> a==b
False
>>> a<=b
True
```

Iterate with for and in

```markdown
>>> items = ('good','bad','ugly')
>>> for word in items:
...     print(word)
...
good
bad
ugly
```
Modify tuple

```markdown
>>> t1=('Fee','Fie','Foe')
>>> id(t1)
2109612850296
>>> t2='top',
>>> t1+=t2
>>> t1
('Fee', 'Fie', 'Foe', 'top')
>>> id(t1)
2109616422168
>>> id(t2)
2109612420936
```

count the elements in touple

```markdown
>>> t1 = ('Fee', 'Fie', 'Foe', 'top')
>>> t1.count('Fee')
1
>>> t1.count('Free')
0
```

Get the index of particular value in the tuple.

```markdown
>>> t1 = ('Fee', 'Fie', 'Foe', 'top')
>>> t1.index('top')
3
>>> t1.index('Free') # exception will araise
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: tuple.index(x): x not in tuple
```
<a href='#index'>Got to top</a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Home](index.md)
<h3 id='sets'> Sets</h3>
![](./Sets1.png)
Here is the above picture:

A = {1,2,3,4,5}

B = {1,2,6,7,8}

A &cup; B = {1,2,3,4,5,6,7,8}

A &cap; B = {1,2}

A - B = {3,4,5}

- A set is like a dictionarywith its values thrown away,leaving only the keys.As with a dictionary, each key must be unique.
- create with set()

```markdown
>>> empty_set = set()
>>> empty_set
set()
```

Convert with set()

- You can create a set from a list, string, tuple, or dictionary, discarding any duplicate values.

```markdown
>>> set('letters')
{'s', 'e', 'l', 't', 'r'}
>>> set( ['Java', 'C', 'C#', 'Python'] )
{'C', 'C#', 'Java', 'Python'}
>>> set(('a','b','c','d'))
{'a', 'b', 'c', 'd'}
>>> set( {'apple': 'red', 'orange': 'orange', 'cherry': 'red'} )
{'apple', 'cherry', 'orange'}
```

Get Length with len()

```markdown
>>> lang=set(['c','c++','Java','Python'])
>>> len(lang)
4
```

Add an item with add()

```markdown
>>> s = set((1,2,3,4))
>>> s.add(4)
>>> s
{1, 2, 3, 4}
```

Delete an item with remove()

```markdown
>>> A = {1,2,3,4,5}
>>> A.remove(1)
>>> A
{2,3,4,5}
>>> A.remove(5)
>>> A
{2,3,4}
>>> A.remove(99)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 99
```

Iterate with for and in

```markdown
>>> furniture = set(('sofa', 'ottoman', 'table'))
>>> for comp in furniture:
...     print(comp)
...
table
sofa
ottoman
```
Combinations and operators

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A.union(B)
{1, 2, 3, 4, 5, 6, 7, 8}
>>> A|B
{1, 2, 3, 4, 5, 6, 7, 8}
```

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A.intersection(B)
{1,2}
>>> A&B
{1,2}
```
intersection_update() will update the A with the result

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A.intersection_update(B)
>>> A
{1,2}
```

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A-B
{3,4,5}
>>> A.difference(B)
{3,4,5}
```
difference_update() will update the set A with the results.

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A.difference_update(B)
>>> A
{3,4,5}
```
![](./Sets2.png)

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A.symmetric_difference(B)
{3, 4, 5, 6, 7, 8}
>>> A^B
{3, 4, 5, 6, 7, 8}
```
- symmetric_difference_update() will update the set with the result.

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A.symmetric_difference_update(B)
>>> A
{3, 4, 5, 6, 7, 8}
```

A &sub; B

![](./Sets3.png)

```markdown
>>> A = {1,2,4}
>>> B = {1,2,3,4,5}
>>> A.issubset(B)
True
>>> A<=B
True
```
A &sup; B

![](./Sets3.png)

```markdown
>>> A = {1,2,4}
>>> B = {1,2,3,4,5}
>>> B.issuperset(A)
True
>>> B>=A
True
```

Disjoint set:

![](./Sets4.png)

```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> C = {9,10}
>>> A.isdisjoint(B)
False
>>> A.isdisjoint(C)
True
```

Delete all elements in the set using clear()

Syntax:

```markdown
set.clear()
```

```markdown
>>> s = {'C'.'C++','JAVA'}
>>> s.clear()
>>> s
set()
```
Copy a set using copy method:

syntax:

```markdown
another_set = set.copy()
```

```markdown
>>> s= {'C'.'C++','JAVA'}
>>> ss = s.copy()
>>> ss
{'Java', 'C++', 'C'}
```
Remove the member of a set using discard()

syntax:

```markdown
set.discard(member)
```

```markdown
>>> A = {1,2,3,4,5}
>>> A.discard(4)
>>> A
{1,2,3,5}
>>> A.discard(99) #remove member which is not in the set
>>> A # will not get any exception
{1,3,5}
```
Delete an element using pop()

- pop() by default delete first element in the set.

```markdown
>>> A = {1,2,3,4,5}
>>> A.pop()
1
>>> A.pop()
2
>>> A
{3,4,5}
>>> A.pop(2)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: pop() takes no arguments (1 given)
```

Update:

- combine two sets into one using update()

syntax:

```markdown
set1.update(set2)
```
```markdown
>>> A = {1,2,3,4,5}
>>> B = {1,2,6,7,8}
>>> A.update(B)
{1, 2, 3, 4, 5, 6, 7, 8}


<a href='#index'>Got to top</a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Home](index.md)
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

