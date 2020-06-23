#### Exercise : Remove From Word

Complete the `remove_from_word(text, word)` function given below, to behave as follows:
* If `word` is found in `text`, return `text` minus the `word` (its first appearance) and any characters that appears after the `word`
* Return `text` otherwise

```python
def remove_from_word(text, word):
  #pass # REPLACE WITH YOUR CODE

```

Example usage:
<include src="inputOutput.md" boilerplate>
<span id="input">

```python
print('>' + remove_from_word('red-hot-lava', 'red'))
print('>' + remove_from_word('red-hot-lava', 'hot'))
print('>' + remove_from_word('red-hot-lava', 'lava'))
print('>' + remove_from_word('red-hot-lava', 'bat'))
print('>' + remove_from_word('red-hot-lava', '-'))
```
</span>
<span id="output">

```
>
>red-
>red-hot-
>red-hot-lava
>red
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def remove_from_word(text, tail_start_word):
  tail_start_position = text.find(tail_start_word)
  if tail_start_position != -1:
    return ...
  else:
    return ...
```

</panel>