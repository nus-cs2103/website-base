### Writing to Files

**Similar to reading from a file, writing to a file too is a three step process. One main difference is the file needs to be opened in the _write mode_.**

<box>

{{ icon_example }} The code below shows how to write to a text file.

```python
file_path = os.path.join('data', 'items.txt')
f = open(file_path, 'w')  # open in write mode
f.write('first line\n')
f.write('second line\n')
f.close()
```
{{ icon_output }} contents of the `items.txt`:
```
first line
second line
```
* {{ icon_tip }} The `'w'` argument indicates that the file should be opened in write mode.
* {{ icon_tip }} Unlike the `print()` function that prints content in a new line every time, the `write` function does not add an automatic line break at the end. You need to add a `\n` at each place you want a line break to appear in the file.

</box>

**To preserve original content and add to it, open the file in _append mode_.** That is because opening a file in write mode and writing to it results in overwriting the content of the file contained before it was opened.

<box>

{{ icon_example }} The code below shows how to append to a file.

```python
f = open(file_path, 'a')  # open in append mode
f.write('third line\n')
f.close()
```
{{ icon_output }} contents of the `items.txt`:
```
first line
second line
third line
```
</box>

<include src="exercisePanel.md" boilerplate var-title="Add Line Numbers" var-file="e-addLineNumbers.md" />