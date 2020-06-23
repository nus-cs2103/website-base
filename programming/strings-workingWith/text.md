### Working with Strings

As you have seen before, you can use `+` and `*` operators to concatenate and replicate strings<br>
%%e.g., `'abc' + '!'*5` evaluates to `'abc!!!!!'`%%.

You can **use indexes and slices to access characters of a string**, just like if a string is a simply a list of characters.

i.e., `'Hi there'` is same as a list:

H   | i | &nbsp; | t | h | e | r | e | !
--- |---|--------|---|---|---|---|---|---
0   | 1 | 2      | 3 | 4 | 5 | 6 | 7 | 8

<box>

{{ icon_example }} The code below shows how to use index and slice notations to get parts of a string.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
s = 'Hi there!'
print(s[0])
print(s[-1])
print(s[3:6])
```
</span>
<span id="output">

```
H
!
the
```
</span>
</include>

</box>

{{ icon_important_big_red }} Strings are immutable. The following code will not work: `s[0] = 'h'`

<include src="exercisePanel.md" boilerplate var-title="Shorten String" var-file="e-shortenString.md" />


You can **use the `in` and `not in` operator to see if one string is a sub-string of another**.

<box>

{{ icon_example }} Examples of checking for the existence of a sub-string:

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
s = 'Hi there!'
print('Hi' in s)
print('hi' in s) # matching is case-sensitive
print('Hello' not in s)
```
</span>
<span id="output">

```
True
False
True
```
</span>
</include>

</box>

<include src="tryYourOwn.md" boilerplate var-program="strings-workingWith" />

<include src="exercisePanel.md" boilerplate var-title="Has All Characters" var-file="e-hasAllCharacters.md" />