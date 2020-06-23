#### Exercise : Remove Extra Spaces

Complete the functions as described below:
* `remove_extra_spaces(text)`: returns a string that is similar to the given string `text` but with only one space between words if there were multiple spaces before. Also removes leading and trailing spaces.

You may find these built-in string functions useful:
* `split()`: splits a string into a list of words.<br>
  e.g., `'  quick  brown    fox'.split()` → `['quick', 'brown', 'fox']`<br>
  [<a href="https://www.mkyong.com/python/python-how-to-split-a-string/" target="_blank">more about the split() function</a>]
  
* `join(list_of_items)`: joins the items in the `list_of_items` using the given string.<br>
  e.g., `'-'.join(['a', 'b', 'c'])` → `'a-b-c'`

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def remove_extra_spaces(text):
  return

print('[' + remove_extra_spaces('  aaa bbb   ccc  ') + ']')
```
</span>
<span id="output">

```
[aaa bbb ccc]
```
</span>
</include>

<panel type="seamless" header="%%:bulb: Hint%%">

Split the `text` into a list of words and join them back using a space (`' '.join(...)`)

</panel>