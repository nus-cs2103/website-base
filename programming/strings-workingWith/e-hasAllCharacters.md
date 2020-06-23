#### Exercise : Has All Characters

Complete the function given below so that it returns `True` if `text` has all the characters in the list `characters`.

```python
def has_all_characters(text, characters):
  #pass # REPLACE WITH YOUR CODE

```

Example usage:
<include src="inputOutput.md" boilerplate>
<span id="input">

```python
print(has_all_characters('abccde', ['a', 'c']))
print(has_all_characters('ab cde', ['a', 'a', ' ']))
print(has_all_characters('apple', ['a', 'f']))
```
</span>
<span id="output">

```
True
True
False
```
</span>
</include>


<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def has_all_characters(text, characters):
  for c in characters:
    if ...
      return False
  return True
```

</panel>