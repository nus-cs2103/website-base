### String Methods

String objects have many methods (the full list is [here](https://docs.python.org/3/library/stdtypes.html#string-methods)).

Here are some string methods related to the nature of the string.
* `upper()`: returns a string with all characters in upper case
* `lower()`: returns a string with all characters in lower case
* `isupper()`: returns `True` if all characters are in upper case
* `islower()`: returns `True` if all characters are in lower case
* `isalpha()`: returns `True` if the string consists only of letters and is not blank.
* `isalnum()`: returns `True` if the string consists only of letters and numbers and is not blank.
* `isdecimal()`: returns `True` if the string consists only of numeric characters and is not blank.
* `isspace()`: returns `True` if the string consists only of spaces, tabs, and new-lines and is not blank.
* `startswith(s)`: returns `True` if the substring `s` appears at the start of the string
* `endswith(s)`: returns `True` if the substring `s` appears at the end of the string

<box>

{{ icon_example }} Examples of string methods mentioned above:

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
print('Hi there!'.upper())
print('Hi there!'.lower())
```
</span>
<span id="output">

```
HI THERE!
hi there!
```
</span>
</include>

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
print('ABC'.isupper(), 'Abc'.isupper())
print('abc'.islower(), 'Abc'.islower())
print('abc'.isalpha(), 'A12'.isalpha())
print('A23'.isalnum(), 'A+1'.isalnum())
print('123'.isdecimal(), 'A12'.isdecimal())
print(' \t\n'.isspace(), 'a b'.isspace())
```
</span>
<span id="output">

```
True False
True False
True False
True False
True False
True False
```
</span>
</include>

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
s = 'Hi there!'
print(s.startswith('Hi'), s.startswith('hi'))
print(s.endswith('!'), s.endswith('?'))
```
</span>
<span id="output">

```
True False
True False
```
</span>
</include>

</box>

<include src="exercisePanel.md" boilerplate var-title="Rectify Case" var-file="e-rectifyCase.md" />
<include src="exercisePanel.md" boilerplate var-title="Is Doctor" var-file="e-isDoctor.md" />

**The `find(s)` method gives index of `s` in the string**, if it is found. It returns `-1` if `s` is not found.

<box>

{{ icon_example }} Examples of the `find()` method:

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
s = 'Monty Python'
print(s.find('Monty'))
print(s.find('Python'))
print(s.find('Spam'))
```
</span>
<span id="output">

```
0
6
-1
```
</span>
</include>

</box>

<include src="exercisePanel.md" boilerplate var-title="Remove From Word" var-file="e-removeFromWord.md" />

**The `join()` method joins a list of string items while using the <tooltip content="the string object upon which the method was called">target string object</tooltip> as a <tooltip content="the string that is placed in between each pair of items">delimiter</tooltip>.**

<box>

{{ icon_example }} Examples of the `join()` method:

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
print(', '.join(['tom', 'dick', 'harry']))
print('-'.join(['one', 'to', 'one']))
```
</span>
<span id="output">

```
tom, dick, harry
one-to-one
```
</span>
</include>

</box>

**The `split()` method is the opposite of `join()`.** It splits a string into a list of strings based on a given delimiter string. If no delimiter is given, any <tooltip content="space, tab, or newline characters">whitespaces</tooltip> in the string are used as delimiters.

<box>

{{ icon_example }} Some examples of using the `split()` method:

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
print('hi, how are you?'.split())
print('A1\t\tA2\nA3'.split())
print('''Todo:
1. eat
2. sleep'''.split('\n')) # split into lines
print('1-to-1-talk'.split('-'))
```
</span>
<span id="output">

```
['hi,', 'how', 'are', 'you?']
['A1', 'A2', 'A3']
['Todo:', '1. eat', '2. sleep']
['1', 'to', '1', 'talk']
```
</span>
</include>

</box>


**There are some string methods to help you to strip trailing/leading spaces.**

<box>

{{ icon_example }} Examples of stripping leading/trailing spaces from a string:

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
s = '  hello  there!  '
print('['+ s.strip() + ']')
print('['+ s.lstrip() + ']') #left side strip
print('['+ s.rstrip() + ']') #right side strip
```
</span>
<span id="output">

```
[hello  there!]
[hello  there!  ]
[  hello  there!]
```
</span>
</include>

</box>

<include src="exercisePanel.md" boilerplate var-title="Get Part" var-file="e-getPart.md" />

**The `replace()` method can replace a character (or a phrase) with another character/phrase**. 

<box>

{{ icon_example }} Some examples of using `replace()` method:

```python
print('face to face'.replace(' ', '-'))  # replace space with a dash
print('1,2,3,4'.replace(',', '\t'))  # replace comma with a tab
print('Yup, Yup, I agree'.replace('Yup', 'Yes'))
```
{{ icon_output }}
```
face-to-face
1	2	3	4
Yes, Yes, I agree
```

</box>

**There are some string methods to help you to align text.**

<box>

{{ icon_example }} Examples of aligning text using string methods:

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
print('Here:'.rjust(20, '>')) # right-justify
print('Price'.ljust(20, '=')) # left-justify
print('Title'.center(16, ':')) # center
```
</span>
<span id="output">

```
>>>>>>>>>>>>>>>Here:
Price===============
:::::Title::::::
```
</span>
</include>

</box>

<include src="tryYourOwn.md" boilerplate var-program="strings-methods" />

<include src="exercisePanel.md" boilerplate var-title="Print Formatted Item" var-file="e-printFormattedItem.md" />
